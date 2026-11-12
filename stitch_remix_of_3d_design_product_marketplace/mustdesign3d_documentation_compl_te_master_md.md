# MUSTDESIGN3D — ARCHIVE MAÎTRE COMPLÈTE & DOSSIER DE PRODUCTION (ALL-IN-ONE)
*Date : Novembre 2026 | Localisation : Casablanca, Maroc | Équipement : Bambu Lab A1 + AMS Lite (4 Couleurs)*
*Devise : MAD (Dirhams Marocains) | Paiement : Cash on Delivery (COD) + BAT WhatsApp (+212 661 00 00 00)*

---

## TABLE DES MATIÈRES
1. [Vision, Positionnement & Règle DFM Bambu Lab A1](#1-vision-positionnement--règle-dfm)
2. [Catalogue Complet des 36 Modèles Physiques & Specs DFM](#2-catalogue-complet-des-36-modèles-physiques--specs-dfm)
3. [Architecture Logicielle Next.js 15+ App Router & Arborescence](#3-architecture-logicielle-nextjs-15-app-router)
4. [Schéma de Données Prisma Production (`schema.prisma`)](#4-schéma-de-données-prisma-production)
5. [Code Source des Composants Clés (Store Panier, ProductCard, Checkout COD)](#5-code-source-des-composants-clés)
6. [Composants d'Affichage & Micro-Interactions (Toast, Aperçu 2.5D, Drawer Panier)](#6-composants-daffichage--micro-interactions)
7. [Configuration d'Environnement de Production (`.env.production`)](#7-configuration-denvironnement-de-production)
8. [Guide de Synchronisation & Ajout Continu sans Recompilation](#8-guide-de-synchronisation--ajout-continu)
9. [Scripts de Fabrication OpenSCAD & Fichiers de Production 3MF](#9-scripts-de-fabrication-openscad)

---

## 1. VISION, POSITIONNEMENT & RÈGLE DFM

### A. Positionnement de Marque
**MustDesign3D** est la première marque marocaine d'objets du quotidien et d'accessoires personnalisés en impression 3D néo-artisanale, fusionnant le patrimoine géométrique marocain (zellige, calligraphie arabe Diwani/Kufi, arches mauresques) avec le design minimaliste contemporain (Japandi / Nordique).

### B. Règle d'Ingénierie DFM (Design For Manufacturing)
Chaque produit du catalogue respecte scrupuleusement les contraintes physiques de la **Bambu Lab A1** couplée à l'**AMS Lite** :
1. **0 Support Sacrificiel (100% Sans Support)** : Conception avec base plate pour plateau texturé PEI doré et chanfreins auto-portants à 45°. Zéro déchet d'échenillage.
2. **Impression 2.5D & Économie de Purge** : Séparation des couleurs par couches géométriques (fond contrasté + lettrage/relief en surélévation de 1 à 2 mm) réduisant les changements d'outils à 1-3 par cycle.
3. **Nuancier Physique 4 Couleurs Simultanées** :
   - *Noir Basalte* (Bambu PLA Basic #1e2022)
   - *Bleu Majorelle* (Bambu PLA Basic #233d99)
   - *Blanc Albâtre / Ivoire* (Bambu PLA Basic #fafafa)
   - *Terre Cuite d'Atlas / Or Artisanal* (Bambu PLA Silk/Basic #b94832 / #d49b42)
4. **Matériaux** : PLA+ biosourcé haute résistance certifié sans odeur, résistant aux UV et indéformable en intérieur.

---

## 2. CATALOGUE COMPLET DES 36 MODÈLES PHYSIQUES & SPECS DFM

| Niche | SKU | Nom du Produit & Calligraphie | Prix (MAD) | Temps | Poids | Couleurs AMS |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Cadeaux** | MD-KCH-01 | Porte-Clés Prénom Bilingue (FR & Arabe) | 49.00 MAD | 22 min | 14 g | Bleu Majorelle, Blanc Albâtre |
| **Cadeaux** | MD-KCH-02 | Porte-Clés Plaque d'Immatriculation Maroc | 45.00 MAD | 18 min | 11 g | Blanc Albâtre, Noir Basalte |
| **Cadeaux** | MD-BOX-01 | Écrin Hexagonal Fiançailles « حب / Love » | 189.00 MAD | 55 min | 52 g | Or Soyeux, Bleu Majorelle |
| **Cadeaux** | MD-BMK-01 | Marque-Page Papeterie Luxe « اقرأ / Iqra » | 49.00 MAD | 16 min | 8 g | Or Artisanal, Bleu Majorelle |
| **Cadeaux** | MD-KCH-03 | Porte-Clés Maillot Maroc « Lions de l'Atlas » | 45.00 MAD | 20 min | 12 g | Rouge National, Vert Étoile, Blanc |
| **Cadeaux** | MD-TAG-01 | Étiquette de Bagage & Valise Nomade | 39.00 MAD | 19 min | 15 g | Noir Basalte, Blanc Albâtre |
| **Cadeaux** | MD-KCH-04 | Porte-Clés Initiale Calligraphiée Zellige | 39.00 MAD | 17 min | 10 g | Terre Cuite, Or Soyeux |
| **Cadeaux** | MD-PET-01 | Médaille Animaux Chat & Chien Maroc | 35.00 MAD | 12 min | 4 g | Noir Basalte, Blanc Albâtre |
| **Bureau** | MD-DSK-01 | Bloc Cube Porte-Téléphone & Cartes Carré | 99.00 MAD | 48 min | 62 g | Noir Basalte, Bleu Majorelle |
| **Bureau** | MD-DSK-02 | Plaque de Bureau Carrée & Badge Nominatif | 99.00 MAD | 38 min | 48 g | Ivoire, Noir Basalte, Terre Cuite |
| **Bureau** | MD-DSK-03 | Set Vide-Poches & Rangement Modulaire Carré | 89.00 MAD | 32 min | 42 g | Terre Cuite, Noir Basalte |
| **Bureau** | MD-DSK-04 | Boîtier Carré Magnétique Zellige AirPods | 79.00 MAD | 36 min | 38 g | Bleu Majorelle, Blanc Albâtre |
| **Bureau** | MD-DSK-05 | Support de Casque Audio Arche Mauresque | 139.00 MAD | 85 min | 110 g | Noir Basalte, Terre Cuite |
| **Bureau** | MD-DSK-06 | Station Bureau Géométrique Multi-Slots | 129.00 MAD | 70 min | 95 g | Noir, Bleu Majorelle, Ivoire |
| **Bureau** | MD-DSK-07 | Plaque de Porte Ovale « Bienvenue / مرحباً » | 99.00 MAD | 28 min | 30 g | Ivoire, Or Artisanal, Noir |
| **Bureau** | MD-DSK-08 | Lot 4 Clips Reste-Câbles Adhésifs Zellige | 49.00 MAD | 15 min | 16 g | Noir Basalte, Terre Cuite |
| **Bureau** | MD-DSK-09 | Pot à Crayons & Pinceaux Côtelé Japandi | 85.00 MAD | 52 min | 58 g | Ivoire Albâtre Mat |
| **Déco** | MD-DEC-01 | Set de 4 Sous-Verres Étoile Zellige | 79.00 MAD | 40 min | 64 g | Terre Cuite, Ivoire Albâtre |
| **Déco** | MD-DEC-02 | Porte-Encens Chevalier Noir (Shadow Knight) | 129.00 MAD | 68 min | 82 g | Noir Basalte, Or Artisanal |
| **Déco** | MD-DEC-03 | Veilleuse Champignon Côtelée Ambiance LED | 249.00 MAD | 110 min | 140 g | Abat-jour Ivoire, Pied Terracotta |
| **Déco** | MD-DEC-04 | Vase Soliflore Facetté « Shizu / 静 » | 69.00 MAD | 34 min | 36 g | Terre Cuite d'Atlas |
| **Déco** | MD-DEC-05 | Tableau Carte du Maroc en Relief Multicouche | 199.00 MAD | 75 min | 88 g | Bleu Majorelle, Or, Blanc Albâtre |
| **Déco** | MD-DEC-06 | Cache-Pot Géométrique Polygonal + Soucoupe | 89.00 MAD | 50 min | 65 g | Noir Basalte, Base Terracotta |
| **Déco** | MD-DEC-07 | Patère Murale Géométrique Épure (5 kg) | 35.00 MAD | 24 min | 28 g | Noir Basalte |
| **Déco** | MD-DEC-08 | Plaque Pixel Zellige 8 Branches (86 mm) | 119.00 MAD | 25 min | 22 g | Ivoire, Bleu Majorelle, Or |
| **B2B** | MD-B2B-01 | Présentoir QR Code Comptoir & Avis Google | 149.00 MAD | 38 min | 42 g | Fond Blanc, QR Noir Profond |
| **B2B** | MD-B2B-02 | Plaque de Comptoir @Réseaux Sociaux | 99.00 MAD | 30 min | 36 g | Noir Basalte, Blanc Albâtre |
| **B2B** | MD-B2B-03 | Logo d'Entreprise Extrudé 3D sur Socle | Sur devis | 60 min | 75 g | Charte vectorielle client |
| **B2B** | MD-B2B-04 | Lot Porte-Clés Logo Entreprise (20-500 pcs) | Sur devis | 18 min | 10 g | Teintes corporate sur mesure |
| **B2B** | MD-B2B-05 | Badges Visiteurs & Staff Réutilisables Relief | Dès 29 MAD | 14 min | 9 g | Noir Basalte, Blanc Albâtre |
| **B2B** | MD-B2B-06 | Chevalet de Table Numéro & Menu Restaurant | 59.00 MAD | 28 min | 34 g | Noir Basalte, Numéro Or |
| **Événements** | MD-EVT-01 | Lot Marque-Places Nominatifs Chevalet | Sur devis | 15 min | 10 g | Or Soyeux, Ivoire Albâtre |
| **Événements** | MD-EVT-02 | Médaillons Boîtes de Dragées (Lot de 50) | 149.00 MAD | 45 min | 35 g | Or Soyeux, Blanc Albâtre |
| **Événements** | MD-EVT-03 | Cake Topper Gâteau « ألف مبروك / Mabrouk » | 79.00 MAD | 30 min | 26 g | Or Soyeux Brillant |
| **Événements** | MD-EVT-04 | Support Casque Gamer Plaque Gamertag | 169.00 MAD | 90 min | 120 g | Rouge Sport, Noir Basalte |
| **Événements** | MD-EVT-05 | Lettre Naissance Relief Déco Chambre (18 cm) | 139.00 MAD | 65 min | 85 g | Ivoire, Bleu Pastel ou Terracotta |

---

## 3. ARCHITECTURE LOGICIELLE NEXT.JS 15+ APP ROUTER

```text
mustdesign3d/
├── app/
│   ├── layout.tsx                # Structure globale, fonts Noto Serif/Inter, contextes Cart
│   ├── page.tsx                  # Accueil haute conversion (Hero, Bestsellers, Atelier, FAQ)
│   ├── shop/
│   │   └── page.tsx              # Catalogue 36 produits, pagination 1-4, filtres gauche
│   ├── product/
│   │   └── [slug]/page.tsx       # Fiche produit, visualiseur 3D, options AMS Lite
│   ├── cart/
│   │   └── page.tsx              # Panier complet dédupliqué & tiroir latéral
│   ├── checkout/
│   │   └── page.tsx              # Formulaire COD Maroc (villes, numéros +212, BAT WhatsApp)
│   ├── order-tracking/
│   │   └── page.tsx              # Statut d'extrusion en direct & suivi Amana
│   ├── business/
│   │   └── page.tsx              # Offres B2B, logos extrudés & devis séries
│   ├── custom/
│   │   └── page.tsx              # Studio sur mesure & devis fichiers STL
│   └── api/
│       ├── products/route.ts     # Catalogue public DTO
│       ├── orders/route.ts       # Enregistrement commande COD & dispatch WhatsApp
│       └── quotes/route.ts       # Demandes de devis B2B
├── components/
│   ├── catalogue/                # CatalogueNavigation, CatalogueSidebarCategories, Pagination
│   ├── product/                  # ProductCard, LiveBilingual25DPreview, Viewer3D Three.js
│   ├── cart/                     # InteractiveCartDrawer, CartLineItem
│   └── ui/                       # ToastNotificationCenter, Button, Badge
├── data/
│   ├── catalog-36-products.ts    # Base de données TypeScript autoritaire
│   └── products.json             # Fichier JSON asynchrone modifiable sans recompilation
├── lib/
│   ├── contracts.ts              # Interfaces TypeScript strictes (Product, CartLine, Order)
│   ├── cart-storage.ts           # Logique de déduplication localStorage & résilience
│   └── brand.ts                  # Métadonnées, coordonnées Maroc, devises
└── prisma/
    └── schema.prisma             # Schéma relationnel PostgreSQL / Railway
```

---

## 4. SCHÉMA DE DONNÉES PRISMA PRODUCTION

```prisma
datasource db {
  provider = "postgresql"
  url      = env("DATABASE_URL")
}

generator client {
  provider = "prisma-client-js"
}

enum Role {
  ADMIN
  OPERATOR
  VIEWER
}

enum OrderStatus {
  PENDING
  CONFIRMED
  DESIGN_REVIEW
  PRINTING
  QUALITY_CHECK
  PACKED
  SHIPPING
  DELIVERED
  COMPLETED
  CANCELLED
}

enum PaymentMethod {
  COD
  BANK_TRANSFER
}

model Product {
  id                    String              @id @default(cuid())
  sku                   String              @unique
  slug                  String              @unique
  name                  String
  shortDescription      String
  description           String
  categoryId            String
  priceCents            Int?                // En centimes de MAD (4900 = 49.00 MAD)
  currency              String              @default("MAD")
  customizable          Boolean             @default(false)
  featured              Boolean             @default(false)

  // Spécifications DFM Bambu Lab A1
  estimatedWeightGrams  Int?
  estimatedPrintMinutes Int?
  dimensionWidthMm      Float?
  dimensionDepthMm      Float?
  dimensionHeightMm     Float?
  maxAmsColors          Int                 @default(4)
  nozzleSizeMm          Float               @default(0.4)
  layerHeightMm         Float               @default(0.20)
  supportsRequired      Boolean             @default(false)

  orderItems            OrderItem[]
  createdAt             DateTime            @default(now())
  updatedAt             DateTime            @updatedAt
}

model Filament {
  id              String   @id @default(cuid())
  name            String   // Ex: "Bleu Majorelle"
  material        String   @default("PLA")
  hexColor        String   // Ex: "#233d99"
  remainingGrams  Int?     @default(1000)
  amsSlot         Int?     // 1, 2, 3 ou 4
  available       Boolean  @default(true)
}

model Order {
  id                  String       @id @default(cuid())
  reference           String       @unique // Ex: MD3D-2026-000124
  customerName        String
  customerPhone       String       // Format marocain +2126XXXXXXXX
  shippingCity        String
  shippingAddress     String
  note                String?
  status              OrderStatus  @default(PENDING)
  paymentMethod       PaymentMethod @default(COD)
  subtotalCents       Int
  shippingFeeCents    Int          @default(3500)
  totalCents          Int
  requestWhatsAppBat  Boolean      @default(true)
  items               OrderItem[]
  createdAt           DateTime     @default(now())
  updatedAt           DateTime     @updatedAt
}

model OrderItem {
  id                  String   @id @default(cuid())
  orderId             String
  order               Order    @relation(fields: [orderId], references: [id], onDelete: Cascade)
  productId           String
  product             Product  @relation(fields: [productId], references: [id])
  productNameSnapshot String
  unitPriceCents      Int
  quantity            Int      @default(1)
  lineTotalCents      Int
  personalization     Json?    // { frenchName: "Youssef", arabicName: "يوسف", palette: "bleu-ivoire" }
}
```

---

## 5. RÈGLES COMMERCIALES & LOCALISATION MAROC

1. **Devise & Tarification** :
   - Tous les montants sont stockés en centimes d'entiers (`4900` = 49.00 MAD) pour éliminer les erreurs de floating-point.
   - Les articles sur devis (`MD-B2B-03`, `MD-EVT-01`) ont `priceCents = null` et affichent le libellé « Sur devis B2B ».
2. **Livraison Express Amana** :
   - Seuil de gratuité automatique dès **200.00 MAD** de commande.
   - Forfait standard fixe de **35.00 MAD** en dessous de ce seuil.
   - Délai contractuel : 24h à 48h ouvrables sur Casablanca, Rabat, Marrakech, Tanger, Fès, Agadir, etc.
3. **Workflow Bon à Tirer (BAT) WhatsApp** :
   - Case cochée par défaut au checkout : *"Recevoir gratuitement le BAT 3D par WhatsApp avant extrusion"*.
   - Déclenche la génération d'un message pré-rempli vers le service client atelier (+212 661 00 00 00) avec la référence commande et le récapitulatif des personnalisations.
