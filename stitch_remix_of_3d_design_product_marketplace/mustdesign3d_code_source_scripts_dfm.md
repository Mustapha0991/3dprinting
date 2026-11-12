# FICHIERS DE CODE SOURCE & SCRIPTS D'AUTOMATISATION — MUSTDESIGN3D
*Next.js 15+ App Router, TypeScript Strict, Tailwind CSS & OpenSCAD DFM*

---

## 1. MOTEUR DU PANIER AVEC DÉDUPLICATION STRICTE (`lib/cart-storage.ts`)

```typescript
import { CartLine, Personalization, Product, StoredCart } from './contracts';
import { isQuantity, isRecord, optionKey, validatePersonalization } from './validation';

export const CART_STORAGE_KEY = 'mustdesign3d.cart';

export interface CartRestoreResult {
  lines: CartLine[];
  notices: string[];
  persistent: boolean;
}

/**
 * Restaure le panier depuis le localStorage avec déduplication stricte des compositions identiques,
 * vérification des prix serveur autoritaires et gestion des pannes de stockage.
 */
export function restoreCart(rawJson: string | null, activeProducts: Product[]): CartRestoreResult {
  const result: CartRestoreResult = { lines: [], notices: [], persistent: true };
  if (!rawJson) return result;

  try {
    const parsed: unknown = JSON.parse(rawJson);
    if (!isRecord(parsed) || parsed.schemaVersion !== 1 || !Array.isArray(parsed.lines)) {
      return { lines: [], notices: ['Format de panier réinitialisé pour mise à jour.'], persistent: false };
    }

    for (const rawLine of parsed.lines) {
      if (!isRecord(rawLine)) continue;
      const product = activeProducts.find((p) => p.id === rawLine.productId);
      if (!product || product.pricingMode === 'quote' || product.priceCents === null) continue;

      const validPersonalization = validatePersonalization(product, rawLine.personalization);
      if (!validPersonalization || !isQuantity(rawLine.quantity)) continue;

      // Déduplication stricte par clé d'option canonique
      const existingLine = result.lines.find(
        (l) => optionKey(l.productId, l.personalization) === optionKey(product.id, validPersonalization)
      );

      if (existingLine) {
        existingLine.quantity = Math.min(99, existingLine.quantity + Number(rawLine.quantity));
      } else {
        result.lines.push({
          id: typeof rawLine.id === 'string' ? rawLine.id : crypto.randomUUID(),
          productId: product.id,
          personalization: validPersonalization,
          quantity: Number(rawLine.quantity),
          unitPriceCents: product.priceCents,
        });
      }
    }
    return result;
  } catch (e) {
    return { lines: [], notices: ['Stockage local inaccessible. Panier en mémoire.'], persistent: false };
  }
}
```

---

## 2. COMPOSANT DU VISUALISEUR 2.5D BAMBU LAB (`components/LiveBilingual25DPreview.tsx`)

```tsx
'use client';

import React from 'react';

interface PreviewProps {
  frenchName: string;
  arabicName: string;
  colors: string[]; // [Base, Texte, Accent]
  dimensionsMm?: { width: number; depth: number; height: number };
}

export const LiveBilingual25DPreview: React.FC<PreviewProps> = ({
  frenchName,
  arabicName,
  colors = ['#1e2022', '#233d99', '#fafafa'],
  dimensionsMm = { width: 80, depth: 80, height: 12 },
}) => {
  const [baseColor, textColor, accentColor = textColor] = colors;

  return (
    <div className="relative w-full aspect-square max-w-sm mx-auto bg-gradient-to-b from-[#f8f2ee] to-[#ece7dc] rounded-3xl p-6 border border-[#dfd9d5] flex flex-col items-center justify-between shadow-inner overflow-hidden">
      {/* Texture PEI en filigrane */}
      <div
        className="absolute inset-0 opacity-15 pointer-events-none"
        style={{
          backgroundImage: 'radial-gradient(#1e2022 0.75px, transparent 0.75px)',
          backgroundSize: '8px 8px',
        }}
      />

      {/* Header Calibration DFM */}
      <div className="w-full flex items-center justify-between text-[10px] font-mono text-[#5a5f63] z-10 border-b border-[#dfd9d5]/60 pb-2">
        <span className="flex items-center gap-1.5 font-bold">
          <span className="w-2 h-2 rounded-full bg-emerald-500 animate-pulse" />
          BAMBU LAB A1 • AMS LITE
        </span>
        <span>{dimensionsMm.width}×{dimensionsMm.depth}×{dimensionsMm.height} mm</span>
      </div>

      {/* Rendu 2.5D de la pièce extrudée */}
      <div className="relative my-auto transition-transform duration-300 hover:scale-105">
        <div className="absolute -bottom-3 left-1/2 -translate-x-1/2 w-40 h-6 bg-black/20 rounded-full blur-md" />
        <div
          className="relative w-44 h-44 rounded-2xl shadow-xl flex flex-col items-center justify-center p-3 border-b-4 border-black/30"
          style={{ backgroundColor: baseColor }}
        >
          {/* Liseré géométrique d'arête */}
          <div
            className="absolute inset-2 rounded-xl border border-dashed opacity-40 pointer-events-none"
            style={{ borderColor: accentColor }}
          />

          {/* Arabe RTL avec liaison Unicode */}
          <div
            dir="auto"
            lang="ar"
            className="font-serif font-black text-2xl tracking-wide text-center px-1"
            style={{
              color: textColor,
              textShadow: `1px 1px 0px ${baseColor}, 2px 2px 0px rgba(0,0,0,0.3)`,
            }}
          >
            {arabicName || 'الدار البيضاء'}
          </div>

          {/* Motif zellige séparateur */}
          <div className="flex items-center gap-2 my-1.5 opacity-70">
            <span className="w-4 h-0.5 rounded" style={{ backgroundColor: accentColor }} />
            <span className="text-[9px]" style={{ color: accentColor }}>✦</span>
            <span className="w-4 h-0.5 rounded" style={{ backgroundColor: accentColor }} />
          </div>

          {/* Nom latin en surépaisseur */}
          <div
            className="font-sans font-bold text-xs tracking-widest uppercase text-center px-1"
            style={{
              color: textColor,
              textShadow: '1px 1px 0px rgba(0,0,0,0.2)',
            }}
          >
            {frenchName || 'MUSTDESIGN 3D'}
          </div>
        </div>
      </div>

      {/* Footer Résolution */}
      <div className="w-full flex items-center justify-between text-[10px] text-[#5a5f63] z-10 pt-2 border-t border-[#dfd9d5]/60">
        <span>Buse 0.4 mm • Couche 0.20 mm</span>
        <span className="font-semibold text-emerald-800">100% Sans Support</span>
      </div>
    </div>
  );
};
```

---

## 3. SCRIPT OPENSCAD PARAMÉTRIQUE DU PORTE-CLÉS PRÉNOM (`production/porte-cles-prenom.scad`)

```scad
// ==============================================================================
// MustDesign3D — Porte-Clés Prénom Bilingue 2.5D DFM (Bambu Lab A1 + AMS Lite)
// ==============================================================================
part = "assembly"; // "assembly", "base", "lettering"
width = 75;
depth = 28;
base_height = 2.6;
relief_height = 1.0;
hole_diameter = 5.0;
french_name = "YOUSSEF";
arabic_name = "يوسف";
font_name = "Liberation Sans:style=Bold";
text_size = 8.5;
base_color = "#1e2022";
text_color = "#fafafa";
$fn = 64;

assert(width >= 60 && width <= 85);
assert(base_height + relief_height <= 4.0);

module rounded_plate() {
  hull() {
    translate([-width/2+6, -depth/2+6]) circle(r=6);
    translate([ width/2-6, -depth/2+6]) circle(r=6);
    translate([-width/2+6,  depth/2-6]) circle(r=6);
    translate([ width/2-6,  depth/2-6]) circle(r=6);
  }
}

module base() {
  color(base_color) difference() {
    linear_extrude(base_height) rounded_plate();
    // Anneau de porte-clés renforcé
    translate([-width/2+7, 0, -1]) cylinder(h=base_height+2, d=hole_diameter);
  }
}

module lettering() {
  color(text_color) translate([4, 0, base_height]) linear_extrude(relief_height) {
    if (arabic_name != "") {
      translate([0, 5]) text(french_name, size=text_size*0.8, font=font_name, halign="center", valign="center");
      translate([0, -5]) text(arabic_name, size=text_size*1.1, font=font_name, halign="center", valign="center");
    } else {
      text(french_name, size=text_size, font=font_name, halign="center", valign="center");
    }
  }
}

if (part == "base" || part == "assembly") base();
if (part == "lettering" || part == "assembly") lettering();
```
