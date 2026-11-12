# 🎨 NUANCIER OFFICIEL 4 COULEURS (AMS LITE) — MUSTDESIGN3D
## Guide de Production Bambu Lab A1, Règles DFM (Zero-Support), Mapping UI & Combinaisons Commerciales Rentables

Ce document consacre les **4 bobines de filaments physiques fixes** installées sur l'AMS Lite de votre imprimante 3D **Bambu Lab A1** pour l'atelier **MustDesign3D** (Casablanca, Maroc).

---

### 1. LES 4 COULEURS PHYSIQUES DE L'ATELIER (SLOTS AMS LITE 1 à 4)

| Slot AMS | Nom Commercial | Code Hex Officiel | Matière & Finition | Rôle dans l'Objet 3D | Exemple Produit Phare |
|---|---|---|---|---|---|
| **Slot 1** | **Noir Basalte** | `#161616` | PLA Mat haute densité | Socles lestés, contours contrastés, QR codes, plaques de bureau | Plaque Bureau Architecte (`md-desk-01`), QR Stand (`md-qr-01`) |
| **Slot 2** | **Blanc Albâtre / Ivoire** | `#FAFAFA` | PLA Satiné porcelaine / Tadelakt | Lettrages relief, fonds de QR lisibles, fond de plaque, chiffres | Textes calligraphiés, flocage maillot, plaque de porte |
| **Slot 3** | **Bleu Majorelle** | `#233D99` | PLA Mat profond emblématique | Couleur signature du Maroc, aplats nobles, bordures zellige | Porte-clés prénom Youssef (`md-keychain-01`), sous-verres |
| **Slot 4** | **Rouge Atlas** *(ou Terracotta Ocre)* | `#B92B32` | PLA Mat intense | Teinte nationale, accents chaleureux, symboles de fête | Porte-clés Maillot Maroc (`md-jersey-keychain`), plaques |

*(Note atelier : Le Slot 4 peut accueillir en variante festive le filament **Or Soyeux d'Atelier** `#D49B42` ou **Terracotta Ocre** `#C25E3E` pour les collections mariage et Ramadan).*

---

### 2. PRINCIPES D'OPTIMISATION DE FABRICATION DFM (DESIGN FOR MANUFACTURING)

Pour garantir une **rentabilité maximale par heure d'impression** et éliminer les gaspillages de purge :

1. **Règle du 2.5D par Plan (Changement de couleur par hauteur Z)** :
   - Le fond plat s'imprime en **Couleur 1** (ex: Bleu Majorelle ou Noir Basalte) sur le plateau texturé or PEI.
   - Le texte ou motif en relief (+1.0 à +1.4 mm) s'imprime en **Couleur 2** (ex: Blanc Albâtre).
   - 👉 **Résultat** : **1 seul changement d'outil** pour toute l'impression = 0 gaspillage de purge, temps d'impression divisé par 3 !
2. **100% Zéro-Support (Zero-Support Design)** :
   - Aucun surplomb supérieur à 45°.
   - Toutes les pièces ont une base plane parfaitement stable.
3. **Composants Monochromes Clipsables / Emboîtables** :
   - Pour les objets en 3 ou 4 couleurs (comme le présentoir QR ou le set de sous-verres), imprimer le socle en Noir Basalte en batch de 10, et le panneau bicolore séparément. L'assemblage se fait par rainure ajustée (jeu 0.4 mm).

---

### 3. LES COMBINAISONS MAÎTRESSES POUR LE CATALOGUE E-COMMERCE

| Combinaison | Couleurs Associées | Ambiance & Cible | Produits Recommandés |
|---|---|---|---|
| **Classique Majorelle** | `Bleu Majorelle (#233D99)` + `Blanc Albâtre (#FAFAFA)` | Cadeaux nominatifs, artisanat moderne chic | Porte-clés prénom, porte-clés initiale, marque-places |
| **Lions de l'Atlas** | `Rouge Atlas (#B92B32)` + `Blanc Albâtre (#FAFAFA)` + accent `Noir Basalte` | Supporters de football, fierté marocaine | Porte-clés maillot Maroc (Hakimi #10), porte-clés matricule |
| **Comptoir & Prestige** | `Noir Basalte (#161616)` + `Blanc Albâtre (#FAFAFA)` | Bureaux d'avocats, architectes, cafés & restaurants | Présentoir QR Google Avis, plaque de bureau nominative |
| **Néo-Marocain 3 Teintes** | `Bleu Majorelle` + `Blanc Albâtre` + `Rouge/Terracotta` | Décoration intérieure, art de la table | Set de sous-verres Zellige octogonal, plaque pixel art |

---

### 4. INTÉGRATION NEXT.JS & PALETTES DU SITE (`lib/catalogue.server.ts`)

Les 4 teintes sont directement mappées dans le code source du projet pour que le client puisse choisir exactement ces filaments dans les configurateurs :

```typescript
// lib/catalogue.server.ts
export const filamentColors = [
  { id: 'white', label: 'Blanc Albâtre', hex: '#fafafa' },
  { id: 'black', label: 'Noir Basalte', hex: '#161616' },
  { id: 'blue',  label: 'Bleu Majorelle', hex: '#233d99' },
  { id: 'red',   label: 'Rouge Atlas', hex: '#b92b32' }
] as const;

export const workshopPalettes: Palette[] = [
  { id: 'bleu-blanc',  label: 'Bleu Majorelle · Blanc Albâtre', colors: ['#233d99', '#fafafa'] },
  { id: 'noir-blanc',  label: 'Noir Basalte · Blanc Albâtre', colors: ['#161616', '#fafafa'] },
  { id: 'blanc-noir',  label: 'Blanc Albâtre · Noir Basalte (Spécial QR)', colors: ['#fafafa', '#161616'] },
  { id: 'rouge-blanc', label: 'Rouge Atlas · Blanc Albâtre (Édition Maroc)', colors: ['#b92b32', '#fafafa'] }
];
```
