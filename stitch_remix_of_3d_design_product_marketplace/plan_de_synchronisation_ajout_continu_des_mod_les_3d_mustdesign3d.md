# Plan d'Architecture & Synchronisation Continue des Modèles 3D — MustDesign3D

Ce document fournit le **plan d'intégration automatisé, asynchrone et modulaire** pour maintenir le site web **MustDesign3D** 100% à jour avec les nouveaux modèles 3D et leurs photos sans avoir à recoder le site à chaque ajout.

---

## 1. Principe Général : L'Architecture à "Source de Vérité Unique"

Pour que le site reste synchronisé et fluide sans recompilation manuelle fastidieuse, l'architecture repose sur 3 piliers simples :

```
[Dossier Images & Modèles]               [Fichier Catalogue Data]              [Site Web Next.js 15]
    /public/products/                       /data/products.json                   Boutique, Filtres,
    ├── cube-phone-01.jpg       ───►       ou /lib/catalogue.server.ts   ───►     Configurateurs, Panier
    ├── badge-square-01.jpg                 (ou API / Headless CMS)              & Checkout COD
    └── model-3d.stl / .3mf
```

---

## 2. Option A (La plus simple & rapide) : "Dossier + Fichier JSON Automatique"

C'est la méthode idéale pour votre démarrage sous **VS Code / Next.js** :

### Étape 1 : Structure des dossiers dans votre projet
```txt
mustdesign3d/
├── public/
│   └── products/                  <-- Vous déposez vos photos JPEG/WebP ici
│       ├── square-phone-stand.jpg
│       ├── square-desk-badge.jpg
│       ├── airpods-case-square.jpg
│       └── modular-desk-tray.jpg
├── data/
│   └── products.json              <-- Liste unique de tous vos produits
```

### Étape 2 : Format standardisé pour ajouter un modèle dans `products.json`
Pour chaque nouveau modèle (ex: les modèles carrés simples), il suffit d'ajouter ce bloc dans `products.json` :

```json
{
  "id": "md-square-phone-01",
  "slug": "cube-porte-telephone-cartes",
  "name": "Porte-Téléphone & Cartes Cube Carré",
  "categoryId": "desk-gaming",
  "priceCents": 9900,
  "pricingMode": "fixed",
  "featured": true,
  "shortDescription": "Bloc cube minimaliste avec fente smartphone et cartes de visite.",
  "images": [
    {
      "src": "/products/square-phone-stand.jpg",
      "alt": "Porte-téléphone cube carré noir basalte et bleu majorelle",
      "kind": "photo"
    }
  ],
  "palettes": [
    {
      "id": "noir-majorelle",
      "label": "Noir Basalte & Bleu Majorelle",
      "colors": ["#1e2022", "#233d99"]
    }
  ],
  "dimensionsMm": { "width": 80, "depth": 80, "height": 80 },
  "personalizationSchema": { "kind": "none", "bespoke": false },
  "bambuMetadata": {
    "printTimeMinutes": 35,
    "filamentGrams": 45,
    "nozzleMm": 0.4,
    "layerHeightMm": 0.20,
    "amsColorCount": 2,
    "supports": false
  }
}
```

👉 **Résultat immédiat** : Dès que ce fichier JSON est sauvegardé, la page d'accueil, les catégories, la boutique (`/shop`), la pagination et le panier affichent automatiquement le produit avec sa photo, son prix en MAD et ses pastilles AMS Lite !

---

## 3. Option B (Automatisation Totale via Script CLI) : "Scanner de Dossier"

Pour ne même pas taper le JSON à la main, un script Node.js génère automatiquement le catalogue en lisant le dossier des photos :

### Le script `scripts/sync-catalog.mjs` :
```javascript
import fs from 'node:fs';
import path from 'node:path';

const IMAGES_DIR = './public/products';
const OUTPUT_FILE = './data/products.json';

const files = fs.readdirSync(IMAGES_DIR).filter(f => /\.(jpg|jpeg|png|webp)$/i.test(f));

const catalog = files.map(file => {
  const slug = path.parse(file).name.toLowerCase().replace(/[^a-z0-9]+/g, '-');
  return {
    id: `md-${slug}`,
    slug: slug,
    name: slug.split('-').map(s => s.charAt(0).toUpperCase() + s.slice(1)).join(' '),
    priceCents: 8900, // Prix par défaut modifiable
    images: [{ src: `/products/${file}`, kind: 'photo' }],
    status: 'active'
  };
});

fs.writeFileSync(OUTPUT_FILE, JSON.stringify(catalog, null, 2));
console.log(`✅ Synchronisation terminée : ${catalog.length} modèles prêts !`);
```
**Commande terminal :** `node scripts/sync-catalog.mjs`

---

## 4. Option C (Sans aucun code, depuis votre téléphone) : "Headless CMS ou Google Sheets"

Si vous voulez ajouter des modèles depuis votre atelier ou votre smartphone à Casablanca :
1. **Google Sheets / Notion / Supabase** :
   - Colonnes : `Nom`, `Catégorie`, `Prix (MAD)`, `Photo URL`, `Couleurs AMS`.
2. **Synchronisation automatique** :
   - Next.js interroge l'API ou le webhook avec `revalidate: 60` (Incremental Static Regeneration).
   - Dès que vous prenez une photo avec votre smartphone et l'ajoutez dans votre tableau, le site web se met à jour en 60 secondes sans redéployer le serveur.

---

## 5. Matrice Récapitulative des Données Produits Recommandées

| Champ | Type | Utilité sur le Site Web MustDesign3D |
| :--- | :--- | :--- |
| `id` & `slug` | String | URL unique (`/product/[slug]`) et clé de panier sans doublon |
| `name` | String | Titre bilingue affiché sur la carte produit et le Bon à Tirer |
| `priceCents` | Entier | Montant strict en centimes (ex: `9900` = 99.00 MAD) |
| `pricingMode` | `"fixed"` ou `"quote"` | Déclenche soit "Ajouter au Panier" soit "Devis B2B" |
| `images` | Array | Tableau ordonné des photos réelles (Face, 3/4, Détail) |
| `palettes` | Array | Teintes réelles physiques chargées dans l'AMS Lite |
| `bambuMetadata` | Object | Temps d'impression, grammage et statut 0-support |
