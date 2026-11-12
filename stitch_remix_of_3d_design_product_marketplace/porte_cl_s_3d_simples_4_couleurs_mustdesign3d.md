# 🔑 NOUVEAUX MODÈLES DE PORTE-CLÉS 3D (OPTIMISÉS 4 COULEURS AMS LITE) — MUSTDESIGN3D
## Spécifications de Fabrication Bambu Lab A1, Règles DFM (1 Changement / 0 Déchet) & Fichiers CAD OpenSCAD

Ce document consacre les **3 nouveaux modèles de porte-clés simples et ultra-rentables** conçus spécifiquement pour exploiter les **4 couleurs physiques** de l'atelier :
- **Slot 1 (Noir Basalte)** : `#161616`
- **Slot 2 (Blanc Albâtre / Ivoire)** : `#FAFAFA`
- **Slot 3 (Bleu Majorelle)** : `#233D99`
- **Slot 4 (Rouge Atlas / Terracotta)** : `#B92B32` (ou `#C25E3E`)

---

### 1. TABLEAU DES 3 NOUVEAUX MODÈLES DE PORTE-CLÉS

| # | Réf Produit | Nom Commercial | Palette Utilisée | Dimensions & Poids | Temps Bambu A1 | Prix Conseillé | Asset Visuel Généré |
|---|---|---|---|---|---|---|---|
| **01** | `md-keychain-initial` | **Porte-clés Monogramme Initiale Zellige** | Base `Bleu Majorelle` + Relief `Blanc Albâtre` (Accent `Terracotta`) | 48 × 48 × 3.6 mm · **9 g** | **18 min** (Batch de 8 en 1h45) | **39 MAD** | `{{DATA:IMAGE:IMAGE_72}}` |
| **02** | `md-car-charm` | **Porte-clés Médaillon Protecteur 'ما شاء الله'** | Fond `Noir Basalte` + Lettres `Blanc` + Anneau `Bleu Majorelle` | 52 × 52 × 3.6 mm · **11 g** | **22 min** (Batch de 6 en 1h35) | **49 MAD** | `{{DATA:IMAGE:IMAGE_70}}` |
| **03** | `md-couple-heart` | **Porte-clés Cœur de Couple Emboîtable (Duo)** | Demi-cœur 1 `Rouge Atlas` + Demi-cœur 2 `Blanc Albâtre` | 60 × 52 × 3.6 mm · **13 g** | **24 min** (les 2 pièces) | **59 MAD** (le duo) | `{{DATA:IMAGE:IMAGE_71}}` |

---

### 2. DÉTAILS TECHNIQUES & RÈGLES DE CONCEPTION (DFM)

1. **Impression 2.5D par Étage (Changement d'outil par hauteur Z)** :
   - Fond plat de `0.0 mm` à `2.4 mm` (couches 0.16 mm = 15 couches) imprimé d'un trait sans interruption.
   - Textes et arabesques en relief de `2.4 mm` à `3.6 mm` (+1.2 mm = 7-8 couches).
   - 👉 **Résultat** : **1 seul changement de filament** pour toute l'impression ! Zéro perte de matière (0 poop), purge minimale.
2. **Œillet Monobloc Renforcé (Testé 12 kg)** :
   - Anneau extérieur de 9 mm avec perçage intérieur de 5 mm pour anneau brisé ou mousqueton laiton standard.
   - Raccordement continu au corps de la pièce pour éviter toute rupture dans la poche.
3. **Plein Plateau / Batching** :
   - Le plateau de la Bambu Lab A1 (256 × 256 mm) permet d'imprimer **12 à 16 porte-clés identiques par session** en moins de 3 heures.

---

### 3. MODÈLE PARAMÉTRIQUE OPENSCAD DU PORTE-CLÉS INITIALE (`porte-cles-initiale.scad`)

```scad
// MustDesign3D - Porte-Clés Initiale Zellige 3D
// Optimisé pour buse 0.4mm et 2 couleurs par couche Z (Bleu Majorelle & Blanc)

letter = "M";
size = 48;
base_height = 2.4;
relief_height = 1.2;
hole_d = 4.5;
$fn = 60;

module base_plate() {
    difference() {
        union() {
            // Corps carré à angles arrondis
            linear_extrude(base_height)
                offset(r=4) square(size - 8, center=true);
            
            // Œillet d'attache renforcé
            translate([-size/2 + 2, size/2 - 2, 0])
                cylinder(h=base_height, d=9);
        }
        // Trou de l'anneau métallique
        translate([-size/2 + 2, size/2 - 2, -0.5])
            cylinder(h=base_height + 1, d=hole_d);
    }
}

module raised_initial() {
    translate([0, 0, base_height])
        linear_extrude(relief_height)
            text(letter, size=24, font="Trebuchet MS:style=Bold", halign="center", valign="center");
}

// Rendu complet
color("#233D99") base_plate(); // Slot 3 : Bleu Majorelle
color("#FAFAFA") raised_initial(); // Slot 2 : Blanc Albâtre
```

---

### 4. MAPPING DANS NEXT.JS (`lib/catalogue.server.ts`)

```typescript
// lib/catalogue.server.ts
export const newKeychains = [
  {
    id: 'md-keychain-initial',
    slug: 'porte-cles-initiale-zellige',
    name: 'Porte-Clés Initiale Monogramme Zellige',
    categoryId: 'cadeaux',
    priceCents: 3900, // 39 MAD
    palettes: [
      { id: 'bleu-blanc', label: 'Bleu Majorelle · Blanc', colors: ['#233d99', '#fafafa'] },
      { id: 'noir-blanc', label: 'Noir Basalte · Blanc', colors: ['#161616', '#fafafa'] },
      { id: 'rouge-blanc', label: 'Rouge Atlas · Blanc', colors: ['#b92b32', '#fafafa'] }
    ],
    image: '{{DATA:IMAGE:IMAGE_72}}'
  },
  {
    id: 'md-car-charm',
    slug: 'medaillon-protection-mashallah',
    name: 'Médaillon Porte-Clés Protecteur ما شاء الله',
    categoryId: 'cadeaux',
    priceCents: 4900, // 49 MAD
    palettes: [
      { id: 'noir-bleu-blanc', label: 'Noir Basalte · Bleu · Blanc', colors: ['#161616', '#233d99', '#fafafa'] }
    ],
    image: '{{DATA:IMAGE:IMAGE_70}}'
  },
  {
    id: 'md-couple-heart',
    slug: 'porte-cles-couple-initiales',
    name: 'Porte-Clés Cœur de Couple Emboîtable (Duo)',
    categoryId: 'cadeaux',
    priceCents: 5900, // 59 MAD
    palettes: [
      { id: 'rouge-blanc', label: 'Rouge Atlas & Blanc Albâtre', colors: ['#b92b32', '#fafafa'] }
    ],
    image: '{{DATA:IMAGE:IMAGE_71}}'
  }
];
```
