# GUIDE D'IMPLÉMENTATION COMPLET — MUSTDESIGN3D
## Spécifications de Production, Architecture Codex / Next.js 16+, Modèles 3D OpenSCAD & Catalogue Photographique

---

### 1. SYNTHÈSE DU PROJET & DIRECTION DE MARQUE

**MustDesign3D** est un atelier numérique et une marque marocaine de néo-artisanat basée à Casablanca, spécialisée dans les objets nominatifs, la calligraphie arabe en relief et les solutions de présentation pour les commerces et cérémonies.

- **Devise :** Dirham Marocain (`MAD` / `DH`), stocké sous forme de centimes entiers (`priceCents`).
- **Logistique locale :** Cash on Delivery (`COD`), expédition Amana / Aramex, validation de Bon à Tirer (BAT 3D) via WhatsApp.
- **Machine de référence :** Bambu Lab A1 avec AMS Lite (4 filaments simultanés, buse 0.4 mm, couches 0.16–0.20 mm, enveloppe utile 220 × 220 × 220 mm, lit PEI texturé, impression **100% Zero-Support**).
- **Nuancier physique des filaments AMS Lite :**
  - `Bleu Majorelle` : `#233D99`
  - `Noir Basalte` : `#161616`
  - `Blanc Albâtre / Ivoire` : `#FAFAFA`
  - `Terracotta Ocre` : `#C25E3E`
  - *Option festive & prestige :* Or Soyeux (`#D49B42`)

---

### 2. CHARTE GRAPHIQUE & DESIGN SYSTEM TAILWIND

```css
:root {
  --color-surface: #FEF8F4;               /* Ivoire porcelaine / Tadelakt */
  --color-surface-container: #F8F2EE;     /* Sable artisanal clair */
  --color-primary: #233D99;               /* Bleu Majorelle officiel */
  --color-secondary: #161616;             /* Noir basalte mat */
  --color-accent: #C25E3E;                /* Terracotta argile */
  --color-gold: #D49B42;                  /* Or soyeux d'atelier */
  --color-line: #DBD1BF;                  /* Liseré et séparations */
  --color-muted: #6D6C65;                 /* Texte secondaire */
}
```

- **Typographie Titres :** *Noto Serif* / *Georgia* (élégance artisanale et accents néo-marocains).
- **Typographie Interface & Technique :** *Trebuchet MS* / *Segoe UI* / *System Sans-serif* pour une lisibilité maximale sur mobile.
- **Direction du texte :** Support bilingue natif avec balise `<bdi dir="auto">` pour préserver le sens de lecture arabe (RTL) et latin (LTR) côte à côte sans inversion de glyphes.

---

### 3. CATALOGUE DES 9 PRODUITS & MAPPING DES ASSETS VISUELS

Voici le catalogue unifié avec les identifiants stables, les fichiers 3D de fabrication et les photographies commerciales photoréalistes générées :

| # | Réf Produit | Slug URL | Catégorie | Prix (MAD) | Modèle 3D OpenSCAD | Image Commerciale Générée | Dimensions Réelles (mm) |
|---|---|---|---|---|---|---|---|
| **01** | `md-keychain-01` | `porte-cles-prenom` | Cadeaux | **49 MAD** | `production/porte-cles-prenom.scad` | `{{DATA:IMAGE:IMAGE_12}}` (Youssef / يوسف sur chêne) | 75 × 28 × 3.6 mm |
| **02** | `md-desk-01` | `plaque-bureau` | Maison & Bureau | **99 MAD** | `production/plaque-bureau.scad` | `{{DATA:IMAGE:IMAGE_9}}` (Dr. Amine Tazi sur noyer) | 160 × 45 × 55 mm |
| **03** | `md-qr-01` | `support-qr` | Professionnels | **149 MAD** | `production/support-qr.scad` | `{{DATA:IMAGE:IMAGE_11}}` (Brûlerie L'Ocre sur marbre) | 90 × 55 × 125 mm |
| **04** | `md-door-01` | `plaque-porte` | Maison & Bureau | **99 MAD** | `production/plaque-porte.scad` | `{{DATA:IMAGE:IMAGE_8}}` (Dar Yasmine sur tadelakt) | 150 × 65 × 4.0 mm |
| **05** | `md-plate-01` | `porte-cles-plaque-marocaine` | Cadeaux | **45 MAD** | `production/porte-cles-plaque-marocaine.scad` | `{{DATA:IMAGE:IMAGE_6}}` (Matricule 12345 \| أ \| 6) | 70 × 20 × 4.0 mm |
| **06** | `md-pixel-01` | `plaque-pixel-zellige` | Décoration | **119 MAD** | `production/plaque-pixel-zellige.scad` | `{{DATA:IMAGE:IMAGE_7}}` (Mosaïque Zellige bleu/blanc) | 86 × 86 × 3.6 mm |
| **07** | `md-place-01` | `marque-places-personnalises` | Cadeaux & Fêtes | *Sur devis* | `production/marque-places.scad` | `{{DATA:IMAGE:IMAGE_10}}` (Lina & Mehdi / médaillon) | 85 × 40 × 3.0 mm |
| **08** | `md-bag-01` | `etiquette-sac` | Cadeaux | **39 MAD** | `production/etiquette-sac.scad` | Rejoint la palette `Bleu · Blanc` | 85 × 32 × 3.0 mm |
| **09** | `md-contact-01` | `plaque-contact` | Professionnels | **99 MAD** | `production/plaque-contact.scad` | Rejoint la palette `Noir · Blanc` | 140 × 80 × 4.0 mm |

---

### 4. INSTRUCTIONS D'INTÉGRATION DANS LE CODE SOURCE (`PROJECT_SOURCE.md`)

Pour mettre à jour votre code Next.js local avec les nouvelles photos et configurations :

#### A. Actualiser le Catalogue Serveur (`lib/catalogue.server.ts`)
Remplacer les chemins d'images de repli CAD par les images commerciales haute fidélité générées :

```typescript
// Mapping des images commerciales dans lib/catalogue.server.ts
const commercialImages: Record<string, { src: string; alt: string }> = {
  'porte-cles-prenom': {
    src: '{{DATA:IMAGE:IMAGE_12}}',
    alt: 'Porte-clés prénom bilingue Youssef en relief 3D et Bleu Majorelle'
  },
  'plaque-bureau': {
    src: '{{DATA:IMAGE:IMAGE_9}}',
    alt: 'Plaque de bureau nominative bilingue Dr. Amine Tazi Architecte en noir et or'
  },
  'support-qr': {
    src: '{{DATA:IMAGE:IMAGE_11}}',
    alt: 'Présentoir QR code comptoir Brûlerie L’Ocre avec socle terracotta'
  },
  'plaque-porte': {
    src: '{{DATA:IMAGE:IMAGE_8}}',
    alt: 'Plaque de porte d’entrée Dar Yasmine sur tadelakt marocain'
  },
  'porte-cles-plaque-marocaine': {
    src: '{{DATA:IMAGE:IMAGE_6}}',
    alt: 'Porte-clés plaque d’immatriculation marocaine en relief'
  },
  'plaque-pixel-zellige': {
    src: '{{DATA:IMAGE:IMAGE_7}}',
    alt: 'Plaque décorative zellige géométrique en relief FDM'
  },
  'marque-places-personnalises': {
    src: '{{DATA:IMAGE:IMAGE_10}}',
    alt: 'Marque-places mariage Lina & Mehdi et médaillon dragées zellige'
  }
};
```

#### B. Composant Produit (`app/product-media.tsx`)
Le composant `ProductMedia` prend en charge l'affichage en priorité des photos commerciales `kind: 'photo'` ou `kind: 'generated-concept'`, avec fallback gracieux vers le SVG `ProductArt` si l'image est indisponible :

```tsx
export function ProductMedia({ product }: { product: Product }) {
  const [failed, setFailed] = useState(false);
  const image = product.images.find(item => item.kind === 'photo' || item.kind === 'generated-concept');
  if (!image || failed) return <ProductArt product={product} />;
  return (
    <figure className="product-art commercial-media">
      <img src={image.src} alt={image.alt} className="w-full aspect-[4/5] object-cover rounded-md" onError={() => setFailed(true)} />
      {image.kind === 'generated-concept' && <figcaption className="text-xs text-center text-muted mt-1">Visualisation du concept</figcaption>}
    </figure>
  );
}
```

---

### 5. DÉPLOIEMENT & SÉCURITÉ DES ÉCRITURES (MODE DÉMO)

- Les routes `POST /api/orders` et `POST /api/quotes` renvoient un code HTTP `403 Forbidden` (`code: 'DEMO_MODE'`) sans lire le body HTTP ni contacter PostgreSQL.
- Le panier est persisté dans `localStorage` avec la clé `mustdesign3d.cart` et supporte l'édition en place (`?edit=[id]`), le contrôle de stock à 99 unités max, et le recalcul autoritaire des prix depuis le serveur.
- Aucun numéro personnel ni e-mail de démonstration n'est codé en dur : les variables d'environnement `NEXT_PUBLIC_CONTACT_WHATSAPP` et `NEXT_PUBLIC_CONTACT_PHONE` injectent les coordonnées réelles lors du build final.

---

### 6. ÉTAPES POUR L'AGENT CODEX DANS VS CODE

1. **Vérifier l'environnement :** `node -v` (Node 22 recommandé) et `npm ci`.
2. **Tester le build :** `npm run typecheck` puis `npm run build`.
3. **Lancer la recette :** `node .goals/mustdesign3d-local/verification/smoke.cjs`.
4. **Mettre à jour le fichier d'export :** Exécuter `npm run handoff` pour régénérer `PROJECT_SOURCE.md`.