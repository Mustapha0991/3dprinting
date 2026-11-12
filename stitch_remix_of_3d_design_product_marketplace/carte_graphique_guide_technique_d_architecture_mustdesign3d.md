# 🗺️ CARTE D'ARCHITECTURE TECHNIQUE & GRAPH REVIEW — MUSTDESIGN3D
## Guide de Référence pour Coding Assistant (Copilot / Claude Code / Cursor / Codex)
### Stack Complète Frontend, Backend, Pipeline CAD 3D, Moteur IA Gemini & Modèle Commercial

---

## 1. 🎨 CARTE GRAPHIQUE & DESIGN SYSTEM FRONTEND (ATELIER NÉO-ARTISANAL)

Pour reproduire ou surpasser exactement le design sur mesure de **MustDesign3D** avec une cohérence visuelle 100% fidèle :

### A. Palette de Couleurs & Tokens CSS (Atelier Néo-Marocain & AMS Lite)

```css
:root {
  /* Surfaces & Fonds (Inspiration Tadelakt, Porcelaine & Sable fin) */
  --surface: #FEF8F4;                 /* Fond principal soyeux */
  --surface-dim: #DFD9D5;             /* Fond estompé */
  --surface-bright: #FEF8F4;
  --surface-container-lowest: #FFFFFF;/* Cartes et fenêtres modales */
  --surface-container-low: #F8F2EE;   /* Barres d'outils, conteneurs secondaires */
  --surface-container: #F2ECE7;       /* Panneaux de commande latérale */
  --surface-container-high: #ECE6E1;  /* Éléments surélevés */
  --surface-container-highest: #E6E0DB;

  /* Couleur Signature & Primaires */
  --primary: #233D99;                 /* Bleu Majorelle officiel (Yves Saint Laurent) */
  --primary-hover: #1B2F77;
  --primary-container: #DDE3FD;
  --on-primary: #FFFFFF;

  /* Teintes Secondaires & Accents de Matière */
  --secondary: #161616;               /* Noir Basalte mat (Châssis, socles lestés) */
  --accent-terracotta: #C25E3E;       /* Terracotta Ocre / Argile de Fès */
  --accent-atlas-red: #B92B32;        /* Rouge Atlas / Identité nationale Maroc */
  --accent-gold: #D49B42;             /* Or d'Atelier satiné (Édition Cérémonie) */
  --accent-emerald: #1B4D3E;          /* Vert Émeraude / Étoile marocaine */

  /* Typographie & Lignes */
  --text-main: #1E2022;               /* Noir graphite profond */
  --text-muted: #6D6C65;              /* Gris sable / Légendes techniques */
  --border-line: #DBD1BF;             /* Liseré discret d'encadrement */
  --border-focus: #233D99;

  /* Rayons de courbure (ROUND_FOUR) */
  --radius-xs: 4px;
  --radius-sm: 8px;
  --radius-md: 12px;
  --radius-lg: 16px;
  --radius-full: 9999px;
}
```

### B. Typographie & Direction Artistique

| Rôle | Police Recommandée | Fallbacks | Usage |
|---|---|---|---|
| **Titres & Identité Émotionnelle** | `Noto Serif`, `Georgia` | `Times New Roman, serif` | `h1`, `h2`, `h3`, slogans poétiques (*« Un peu de vous. Beaucoup de relief. »*) |
| **Interface, Boutons & Technique** | `Plus Jakarta Sans`, `Inter` | `Segoe UI, Trebuchet MS, sans-serif` | Menus, boutons CTA, jauges, métriques DFM, prix |
| **Calligraphie & Arabe bilingue** | `Noto Naskh Arabic`, `Amiri`, `Aref Ruqaa` | `Tahoma, Arial, sans-serif` | Lettrages prénoms, médaillons Mashallah, gravure 3D |
| **Télémétrie & Code CAD** | `JetBrains Mono`, `Fira Code` | `ui-monospace, monospace` | JSON API, coordonnées G-code, paramètres buse/lit |

---

## 2. 💻 STACK LOGICIELLE RECOMMANDÉE : FRONTEND

Pour obtenir le résultat le plus performant, fluide et interactif possible :

### Framework & Bibliothèques Clés :
1. **Next.js 15+ (App Router)** avec **React 19 & TypeScript strict** :
   - Rendu hybride (Server Components pour le SEO et le catalogue instantané, Client Components pour les configurateurs 3D).
   - Optimisation automatique des polices (`next/font/google`) et des images (`next/image`).
2. **Tailwind CSS v4** + **Radix UI Primitives** (ou `@shadcn/ui`) :
   - Composants accessibles au clavier (dialogues modaux de panier, tiroir de filtres mobile, accordéons FAQ, info-bulles).
   - Gestion native du RTL (`dir="auto"`) et des classes logiques (`ms-`, `me-`, `ps-`, `pe-`).
3. **Three.js & @react-three/fiber (@react-three/drei)** :
   - Rendu WebGL interactif 360° du porte-clés ou de l'objet 3D en temps réel.
   - Matériaux `MeshStandardMaterial` imitant le plastique PLA texturé or PEI (`roughness: 0.85`, `metalness: 0.1`).
   - Bascule interactive des 4 filaments physiques (`#161616`, `#FAFAFA`, `#233D99`, `#B92B32`).
4. **Lucide React** :
   - Iconographie vectorielle légère et cohérente (`Printer`, `Layers`, `Sparkles`, `Cpu`, `CheckCircle2`, `ShieldCheck`).
5. **jsQR & Canvas API** :
   - Génération instantanée côté client des QR Codes SVG/PNG vectoriels vérifiés.
6. **Zustand** :
   - Gestionnaire d'état ultra-léger pour le panier persistant (`localStorage`), la clé API Gemini BYOK et les paramètres du slicer.

---

## 3. ⚙️ STACK LOGICIELLE RECOMMANDÉE : BACKEND & PIPELINE CAD

Le défi majeur réside dans la conversion d'une idée textuelle ou d'un concept IA en un fichier **STL / 3MF manifold et imprimable sans échec**.

### Architecture Backend Microservices :

```text
[Utilisateur Frontend (Next.js)]
         │
         ├──► 1. Requête Prompt-to-3D (Langage naturel ou choix catalogue)
         │       │
         │       ▼
[Backend API FastAPI (Python 3.12+)]
         │
         ├──► 2. Moteur IA : Google Gemini 2.5 Flash / Pro Multimodal
         │       └─ Extraction JSON Structured Outputs (dimensions, texte, œillet, slots AMS)
         │
         ├──► 3. Pipeline CAD Déterministe 2.5D
         │       ├─ CadQuery / OpenSCAD CLI : Opérations booléennes, extrusion du socle plat
         │       ├─ Shapely & CairoSVG : Lissage vectoriel Bézier & liaison des lettres arabes
         │       └─ Trimesh / PyVista : Contrôle DFM (épaisseur >1.6mm, 0 surplomb, manifold)
         │
         ├──► 4. Slicing Automatisé & Génération 3MF
         │       └─ PrusaSlicer CLI / Bambu Studio CLI (profil Bambu Lab A1 0.4mm nozzle)
         │
         └──► 5. Base de Données & Stockage Cloud
                 ├─ Supabase (PostgreSQL 16) : Gestion des commandes, tokens, profils
                 ├─ Cloudflare R2 / AWS S3 : Stockage des STL, 3MF et rendus 3D
                 └─ WhatsApp Business API : Envoi automatique du Bon à Tirer (BAT 3D)
```

### Bibliothèques Python Recommandées :
- **FastAPI + Uvicorn + Pydantic v2** : API asynchrone haute performance et validation stricte des schémas.
- **google-genai SDK** : Pour invoquer les modèles **Gemini 2.5 Flash** (faible coût, 150ms) et **Gemini 2.5 Pro** avec injection de schémas Pydantic.
- **CadQuery 2.x** : Moteur CAD paramétrique basé sur OpenCASCADE. Idéal pour construire des solides étanches par script Python.
- **Trimesh** : Validation du maillage, vérification du volume étanche (`is_watertight`), calcul de la masse de PLA et du centre de gravité.
- **arabic-reshaper & python-bidi** : Préparation et liaison parfaite des glyphes arabes avant extrusion booléenne.

---

## 4. 📐 RÈGLES DE FABRICATION DFM BAMBU LAB A1 / AMS LITE

Pour garantir 100% de réussite sans rejet et un bénéfice brut supérieur à 75% :

| Contrainte Technique | Règle d'Usine MustDesign3D | Justification Économique & Qualité |
|---|---|---|
| **Zéro-Support (0 Support)** | Tous les modèles ont un fond plat et aucun angle > 45° | Élimine les finitions, le ponçage et les traces de supports |
| **Impression 2.5D par Hauteur Z** | Fond plat de `0.0 à 2.4 mm` (Slot 1), Relief de `2.4 à 3.6 mm` (Slot 2) | **1 seul changement d'outil** sur toute la pièce = 0 déchet de purge (0 poop) |
| **Œillet Monobloc Renforcé** | Diamètre extérieur 9 mm, trou intérieur 4.5 mm, congé de raccordement R=3 mm | Résistance à la traction testée > 12 kg (ne casse pas dans la poche) |
| **Buse & Hauteur de Couche** | Buse standard 0.4 mm acier trempé, couches 0.16 mm (première couche 0.20 mm) | Équilibre parfait entre vitesse (18-22 min) et netteté calligraphique |
| **Enveloppe Sécurisée Plateau** | Dimensions max 220 × 220 mm (lit physique 256 × 256 mm) | Laisse l'espace pour la tour de purge et la bordure anti-décollement (brim) |

---

## 5. 🗂️ STRUCTURE MODULAIRE DU CODE PROJET

```text
mustdesign3d/
├── frontend/ (Next.js 15+ App Router)
│   ├── app/
│   │   ├── (shop)/
│   │   │   ├── catalogue/page.tsx       # Grille de produits & filtres
│   │   │   ├── produit/[slug]/page.tsx  # Fiche produit & configurateur 3D
│   │   │   ├── panier/page.tsx          # Panier persistant & jauge livraison
│   │   │   └── checkout/page.tsx        # Tunnel commande Cash on Delivery / WhatsApp
│   │   ├── studio-ia/page.tsx           # Laboratoire IA Gemini & Prompt-to-3D
│   │   ├── business/page.tsx            # B2B, présentoirs QR & entreprises
│   │   ├── layout.tsx                   # Layout global, Shell & En-tête persistent
│   │   └── globals.css                  # Tokens design system & utilitaires Tailwind
│   ├── components/
│   │   ├── viewer-3d.tsx                # Visualiseur interactif Three.js 360°
│   │   ├── ams-color-selector.tsx       # Sélecteur dynamique des 4 bobines physiques
│   │   └── qr-generator.tsx             # Générateur QR haute résolution
│   └── lib/
│       ├── api-client.ts                # Client API FastAPI / Gemini
│       └── store.ts                     # Zustand store (panier, préférences)
│
├── backend/ (Python FastAPI)
│   ├── app/
│   │   ├── api/
│   │   │   ├── ai_generator.py          # Routes Gemini API (Concepts & JSON spec)
│   │   │   ├── cad_builder.py           # Routes CadQuery (Génération STL/3MF)
│   │   │   └── orders.py                # Gestion des commandes & webhook WhatsApp
│   │   ├── cad/
│   │   │   ├── keychain_builder.py      # Générateur déterministe de porte-clés
│   │   │   ├── desk_plate_builder.py    # Générateur de plaques de bureau
│   │   │   └── dfm_validator.py         # Moteur de test Trimesh (0 support, épaisseur)
│   │   └── main.py
│   └── Dockerfile
```

---

## 6. 🚀 ROADMAP DU CODING ASSISTANT POUR LE DÉPLOIEMENT

1. **Étape 1 : Initialisation Frontend & Charte Graphique**
   - Configurer Next.js avec les tokens CSS `Atelier Néo-Artisanal` et les polices `Noto Serif` + `Plus Jakarta Sans`.
   - Mettre en place le composant de visualisation Three.js avec chargement dynamique de géométries STL.

2. **Étape 2 : Microservice CAD & Intégration Gemini**
   - Déployer l'API FastAPI avec l'endpoint `POST /api/generate-cad` qui prend le JSON de spécification et compile le fichier STL en moins de 800ms.

3. **Étape 3 : Tunnel Panier Local & Validation WhatsApp (Maroc COD)**
   - Persistance du panier dans `localStorage`.
   - Bouton de génération automatique du lien WhatsApp pré-rempli avec l'ID du modèle 3D et le visuel du Bon à Tirer (BAT).
