# Démarrer MustDesign3D

## Reprise Gemini et Copilot

Le [paquet de reprise](handoff/README.md) fournit les deux versions du prompt maître, un plan pour chaque environnement et un brief de génération photo. Le fichier PROJECT_SOURCE.md est régénéré depuis le code avec `npm run handoff`. Le README reçu en pièce jointe est resté en lecture seule.

Le nouveau catalogue de démonstration contient neuf références et trois collections. Les études historiques restent dans la galerie technique. Consulter le README du projet pour l’état actuel du code avant de reprendre un ancien jalon ci-dessous.

Mise à jour du 10 novembre 2026. Ce dossier contient les prompts pour développer la prochaine version de MustDesign3D et le relevé des sources demandé. Le site actuel est une démo locale existante.

## 1. Comprendre les livrables

- [Prompt maître](00-master-mustdesign3d.md) fixe la marque, le périmètre et les règles communes.
- [Recherche et sélection](recherche/01-sources-et-selection.md) compare les trois références et propose dix concepts à étudier.
- [Inventaire To7fa](recherche/02-inventaire-to7fa.md) contient les 227 adresses produit relevées dans le sitemap public.
- [Bibliothèque des modèles](recherche/03-modeles-et-import.md) décrit les candidats SliSearch, leur niveau de vérification et le processus d’acquisition.
- Les trois prompts frontend et les trois prompts backend détaillent les prochains changements du code.

Le relevé est un inventaire de liens. Les fichiers STL, 3MF, SCAD et les images doivent être acquis séparément depuis leurs sources avec les droits correspondants.

## 2. Préparer le poste local

1. Ouvrir le projet dans VS Code.
2. Vérifier les instructions AGENTS.md applicables et lire codex.md, puis 00-master-mustdesign3d.md.
3. Vérifier Node et npm dans PowerShell.

```powershell
Set-Location 'C:\Users\mekka\Desktop\codex\3d-printing-website'
node --version
npm.cmd --version
```

Le package.json demande Node 22.x. Utiliser cette version pour aligner le développement et la future exécution Railway. Le poste avait Node 25 lors de la création de la démo.

4. Installer les versions verrouillées.

```powershell
npm.cmd ci
```

5. Vérifier si un serveur utilise déjà le port de la démo.

```powershell
Get-NetTCPConnection -LocalPort 3137 -State Listen -ErrorAction SilentlyContinue
```

Si la démo répond déjà, l’ouvrir sur http://localhost:3137. Pour lancer une session de développement distincte, utiliser un autre port.

```powershell
npm.cmd run dev -- --port 3138
```

Ouvrir http://localhost:3138. Conserver la fenêtre du terminal ouverte. Ctrl+C arrête cette session.

## 3. Commencer par la recherche

1. Lire les trois pages de référence avec Search Service, puis consulter les sources d’origine des modèles retenus.
2. Utiliser l’inventaire To7fa pour comparer les familles de produits. Choisir dix concepts puis trois priorités parmi le porte-clés, la plaque de bureau et le support QR.
3. Pour SliSearch, rechercher un besoin précis avec le filtre commercial et vérifier ensuite la licence chez le créateur. Utiliser les requêtes du document modèles.
4. Enregistrer auteur, adresse d’origine, date de contrôle et droits dans le registre interne. Garder un statut inconnu tant que la source primaire manque.
5. Évaluer chaque concept pour l’A1, puis trancher dans Bambu Studio après acquisition d’un fichier autorisé.
6. Préparer des textes et des visuels MustDesign3D originaux. Photographier les premiers prototypes.

Les prix concurrents constituent des observations datées. Les prix de vente MustDesign3D nécessitent un calcul de fabrication et de livraison.

## 4. Développer dans cet ordre

| Étape | Prompt | Résultat vérifiable |
| --- | --- | --- |
| 1 | [Backend 01](backend/01-contrats-et-donnees.md) | Contrats partagés, identifiants stables et séparation catalogue/recherche |
| 2 | [Frontend 01](frontend/01-fondations-et-accueil.md) | Accueil MustDesign3D, contact et navigation mobile |
| 3 | [Frontend 02](frontend/02-catalogue-et-personnalisation.md) | Catalogue, fiches et options personnalisables |
| 4 | [Frontend 03](frontend/03-panier-et-parcours-client.md) | Panier persistant localement et parcours démo |
| 5 | [Backend 02](backend/02-commandes-et-devis.md) | Lecture API et verrou serveur des écritures démo |
| 6 | [Backend 03, recette locale](backend/03-railway-et-recette.md) | Build et parcours vérifiés localement |
| Après validation | Backend 01 puis 02, jalon commandes | PostgreSQL local, migrations et commandes avec données de test |
| Après demande explicite | Backend 03, publication | Déploiement Railway et contrôle de l’usage |

Exécuter un prompt à la fois. Après chaque étape, demander un résumé des fichiers modifiés, des tests exécutés et des limites restantes. Conserver codex.md et les URLs produit existantes.

## 5. Employer les skills et outils adaptés

| Besoin | Skill ou outil | Usage |
| --- | --- | --- |
| Trouver des produits et vérifier les références | Search Service | Liens publics, faits datés, sources primaires, journal des échecs |
| Revoir les contrats et migrations PostgreSQL | postgresql-code-review | Contraintes, clés étrangères, transactions, JSONB et accès serveur |
| Réviser le moteur PostgreSQL lors du jalon commandes | postgresql-optimization, si disponible | Requêtes mesurées et index associés aux accès réels |
| Préparer un nouveau projet TypeScript isolé | typescript-setup, si disponible | Réserver à un nouveau projet ou à une configuration manquante |
| Tester le site | Navigateur ou Playwright disponible | Mobile, clavier, RTL, personnalisation et panier |

Le skill postgresql-code-review a été lu pendant la préparation de ces prompts. Les autres sont des choix pour leurs étapes respectives. Avant d’en utiliser un, le retrouver dans le catalogue actif et lire son SKILL.md. Si le skill manque, poursuivre avec la documentation officielle et signaler ce remplacement.

Les anciens skills d’artefacts proposent un bundling HTML autonome. La cible de ce projet reste Next.js. Leurs règles de lisibilité et de composition peuvent guider les visuels lorsqu’ils sont disponibles.

## 6. Vérifier avant de demander la publication

```powershell
npm.cmd run typecheck
npm.cmd run build
```

- Accueil, boutique, contact et six fiches existantes accessibles.
- Recherche, catégories et état vide cohérents.
- Prénom français, arabe et bilingue conservés jusqu’au panier.
- Prix indicatifs calculés en centimes de MAD.
- À 320, 390 et 1440 px, contenu lisible et sans débordement horizontal.
- Navigation clavier, fermeture du panier avec Échap et retour du focus fonctionnels.
- Chaque ajout au catalogue possède une provenance et un statut de vérification.
- Démo publique ou locale démo sans saisie de coordonnées ni écriture de commande.

## 7. État de cette mise à jour documentaire

Le jalon démo des six prompts est maintenant implémenté localement : contrats partagés, six produits/prix conservés, visuels originaux, personnalisation par produit, panier structuré/persistant/éditable, pages projet/professionnels/récapitulatif et API catalogue avec verrou des écritures. Six sources OpenSCAD originales privées et leur manifeste sont fournis, sans acquisition de modèle concurrent ni validation de fabrication revendiquée.

Le [README du projet](../README.md) détaille le démarrage, la configuration et les limites réelles. PostgreSQL, migrations, traitement des commandes/devis réels, acquisition de modèles tiers et publication Railway restent des jalons ultérieurs. Aucun service cloud n’a été utilisé pour cette itération.

La reprise suivante ajoute une septième création originale, la plaque pixel Zellige, une galerie /modeles et des vues générées par OpenSCAD pour les sept prototypes. Les exports STL sont disponibles dans production/exports/. Le prix de 119 MAD de la plaque est une hypothèse de démo. La [note de sélection et d’intégration](recherche/04-selection-et-integration.md) contient les résultats Search Service et la procédure d’ajout d’un prochain modèle.
