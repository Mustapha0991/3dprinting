# Product Requirements Document (PRD) — MustDesign3D
## Plateforme E-Commerce & Studio d'Impression 3D Néo-Artisanale (Maroc)

### 1. Vision & Positionnement Produit
**MustDesign3D** est une marque marocaine novatrice d'objets personnalisés et d'accessoires architecturaux conçus pour le quotidien, imprimés en 3D haute fidélité (FDM) à Casablanca sur une ferme de **Bambu Lab A1 équipées d'AMS Lite (4 couleurs maximum simultanées)**.

Contrairement aux approches industrielles impersonnelles ou aux simples gadgets plastiques, MustDesign3D valorise l'artisanat digital marocain :
- **Design Néo-Artisanal** : Mariage des motifs géométriques traditionnels (zellige, calligraphie arabe Kufi/Diwani, arches mauresques) et du minimalisme épuré Japandi / Nordique.
- **Règle de Fabrication DFM (Design For Manufacturing)** : 
  - 100% sans supports complexes (impression plate sur plateau texturé PEI).
  - Épaisseur optimisée 2.5D (base contrastée + surélévation de texte ou de motif).
  - 2 à 4 couleurs maximum par pièce pour minimiser les purges et les temps d'impression.
  - Matériaux biosourcés : PLA+ certifié sans odeur, résistant et recyclable.
- **Localisation Maroc** : Tarification en Dirhams (MAD), paiement Cash on Delivery (COD), validation du Bon À Tirer (BAT 3D) par WhatsApp avant extrusion, livraison express 24h-48h par Amana Express.

---

### 2. Architecture & Arborescence Complète Connectée (Plan du Site)

Le site s'articule autour d'un parcours client sans couture, chaque page étant interconnectée par des liens d'actions unifiés :

```
                        ┌─────────────────────────────────┐
                        │      PAGE D'ACCUEIL (/)         │
                        │  Hero, Vedettes, Collections    │
                        └───────────────┬─────────────────┘
                                        │
        ┌───────────────────────────────┼──────────────────────────────┐
        ▼                               ▼                              ▼
┌──────────────┐              ┌──────────────────┐           ┌────────────────────┐
│ BOUTIQUE     │              │ COLLECTIONS      │           │ SERVICES SPÉCIAUX  │
│ (/shop)      │              │ DÉDIÉES          │           │                    │
│ ├─ Page 1-4  │              │ ├─ Cadeaux (/gifts)          │ ├─ B2B Pro (/business)
│ ├─ Filtres   │              │ └─ Maison & Bureau           │ ├─ Sur Mesure (/custom)
│ └─ Recherche │              │    (/home-desk)              │ ├─ Studio IA (/ai-studio)
└───────┬──────┘              └─────────┬────────┘           └─────────┬──────────┘
        │                               │                              │
        └───────────────────────┬───────┴──────────────────────────────┘
                                │
                                ▼
                ┌──────────────────────────────────┐
                │   FICHES PRODUITS & CONFIGURATEUR│
                │   (/product/[slug])              │
                │   ├─ Visualiseur 3D interactif   │
                │   ├─ Sélecteur teintes AMS Lite  │
                │   └─ Aperçu prénom live (FR/AR)  │
                └───────────────┬──────────────────┘
                                │
                                ▼
                ┌──────────────────────────────────┐
                │   PANIER D'ACHATS INTERACTIF     │
                │   (/cart ou Drawer latéral)      │
                │   ├─ Déduplication stricte       │
                │   ├─ Persistance localStorage    │
                │   └─ Seuil livraison offerte     │
                └───────────────┬──────────────────┘
                                │
                                ▼
                ┌──────────────────────────────────┐
                │   CHECKOUT CASH ON DELIVERY (COD)│
                │   (/checkout)                    │
                │   ├─ Formulaire villes Maroc     │
                │   ├─ Support Bilingue (RTL Arabe)│
                │   └─ Option BAT WhatsApp 3D      │
                └───────────────┬──────────────────┘
                                │
                                ▼
                ┌──────────────────────────────────┐
                │   SUIVI DE COMMANDE EN DIRECT    │
                │   (/order-tracking)              │
                │   ├─ Statut Ferme Bambu Lab A1   │
                │   └─ Numéro de suivi Amana       │
                └──────────────────────────────────┘
```

---

### 3. Spécifications Fonctionnelles Détaillées

#### A. Moteur de Recherche & Catalogue Dynamique (`/shop`)
- **Filtres par facettes** :
  - Catégorie : *All categories*, *Décor*, *Desk & gaming*, *Keyrings*, *Storage*, *Gifts*, *Lamps*, *Vases*, *Incense holders*, *For businesses*.
  - Nuancier physique AMS Lite : *Noir Basalte*, *Bleu Majorelle*, *Blanc Albâtre*, *Terre Cuite / Or*.
  - Fourchette de prix : *< 50 MAD*, *50 - 100 MAD*, *100 - 200 MAD*, *Sur devis B2B*.
- **Pagination sans duplication** :
  - Navigation propre entre pages 1, 2, 3, 4 et fil d'Ariane persistant.
  - Déduplication côté client et serveur via UUID de configuration.

#### B. Configurateur Produit & Visualiseur 3D (`/product/[slug]`)
- **Aperçu interactif 2.5D / Three.js** :
  - Rendu instantané du texte saisi en alphabet latin et calligraphie arabe avec support de la liaison des caractères arabes (`dir="auto"`).
  - Contrôle 3D orbital à 360° avec zoom et inspection des couches d'extrusion.
- **Sélection des palettes** :
  - Affichage direct des spools disponibles en temps réel.
  - Validation du nombre de caractères (1 à 24 graphèmes) pour éviter tout débordement physique sur le plateau d'impression.

#### C. Checkout & Expédition COD (`/checkout`)
- **Champs adaptés au Maroc** :
  - Numéro WhatsApp obligatoire (format standard marocain `06 / 07 / +212`).
  - Menu déroulant des 15 principales métropoles marocaines + option Amana rural.
  - Option active par défaut : *"Recevoir le BAT photo par WhatsApp avant extrusion"*.
- **Règles financières** :
  - Monnaie officielle : **MAD (Dirhams)**.
  - Seuil de livraison offerte fixé à **200 MAD**.
  - Forfait Amana standard de **35 MAD** pour les commandes inférieures à 200 MAD.

---

### 4. Stack Technique & Composants Recommandés
- **Frontend** : Next.js 15+ (App Router), React 19, TypeScript strict, Tailwind CSS.
- **Rendu 3D** : Three.js (r128+), React Three Fiber (facultatif) ou vanilla Three.js WebGL canvas.
- **État & Persistance** : React Context API (`CartContext`), validation de schéma via Zod, persistance locale `localStorage` tolérante aux pannes de quota.
- **Backend & Base de données** : API Routes Next.js (`/api/products`, `/api/orders`, `/api/quotes`), base PostgreSQL (Prisma ORM) pour le suivi de production en atelier.
