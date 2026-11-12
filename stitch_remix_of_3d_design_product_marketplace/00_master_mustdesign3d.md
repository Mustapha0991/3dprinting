# Prompt maître MustDesign3D

## Mission

Tu es l’agent de développement de MustDesign3D, marque marocaine d’objets personnalisés imprimés en 3D. Travaille dans le projet Next.js existant. Lis codex.md, le README des prompts et les documents de recherche avant le prompt du jalon demandé.

Les nouveaux fichiers de ce dossier précisent l’évolution du site. Le PDF Master Prompt sert de référence pour le parcours commercial. Les besoins retenus sont les cadeaux et objets de bureau au Maroc, le français, la personnalisation arabe et la devise MAD.

## État de départ à préserver

Le projet possède déjà /, /shop, /contact et /product/[slug], six produits locaux, un aperçu prénom français/arabe/bilingue et un panier latéral démo en mémoire. Lire le code réel avant de modifier un comportement. Réutiliser les composants adaptés et les URLs.

Utiliser Next.js App Router, React, TypeScript strict et Tailwind selon le package-lock.json. Les versions changent uniquement si un besoin vérifié le justifie.

## Nouvelle expérience

1. Présenter une marque identifiable MustDesign3D, avec un accueil visuel, trois produits vedettes et quatre collections.
2. Donner une recherche et des filtres utilisables sur mobile.
3. Faire de chaque fiche un parcours complet avec détails, options applicables, prix indicatif et produits associés.
4. Proposer un panier latéral qui conserve les choix et se restaure après rechargement en démo.
5. Présenter une barre de contact et une page projet adaptées à l’atelier.
6. Séparer les modèles en recherche des produits réellement validés pour la boutique.

Direction graphique initiale retenue pour cette itération, fond ivoire, sable, anthracite, accent Majorelle, détails géométriques sobres et photos produit dominantes. Adapter la composition à MustDesign3D avec une copie française originale.

## Catalogue et modèles

Consulter les références To7fa et 3DGIFI pour la structure de catalogue et les usages. Consulter SliSearch pour découvrir des fichiers et retrouver leurs créateurs.

L’inventaire de liens sert à la recherche. Acquérir un modèle auprès de sa source primaire et enregistrer ses droits d’impression commerciale, de modification et de redistribution. Vérifier séparément les images, le logo, les polices et les éléments de marque. Les modèles inconnus restent en recherche. Préparer des designs originaux quand le besoin est simple.

L’A1 et son AMS Lite donnent le cadre du projet, jusqu’à quatre couleurs simultanées, PLA prioritaire, géométrie simple et support limité. Pour les prototypes de départ, viser 220 × 220 × 220 mm au maximum et préférer deux ou trois couleurs. Les estimations de poids, temps, purge et marge sont renseignées après slicing ou clairement identifiées comme hypothèses.

Le catalogue démo conserve ses six produits et leurs prix indicatifs. Les trois vedettes sont le porte-clés prénom, la plaque de bureau et le support QR. Les autres candidats passent les vérifications du registre avant publication.

## Modes de fonctionnement

- Démo par défaut, parcours visuel et panier interactifs, message « Commandes bientôt disponibles » avant collecte de coordonnées.
- Les futurs POST commandes et devis refusent les écritures en mode démo avant lecture du corps de requête et avant connexion à PostgreSQL.
- Les coordonnées réelles de MustDesign3D seront fournies par le propriétaire. Une valeur absente donne un état d’attente clair.
- Le prochain jalon commandes utilise PostgreSQL local et des données synthétiques pour les essais.
- La publication Railway intervient après la demande explicite du propriétaire. Le guide contient les étapes à suivre à ce moment.

## Qualité et fin de jalon

Garder les composants lisibles, séparer UI cliente, catalogue public et données internes. Maintenir les noms arabes en Unicode, utiliser dir="auto" et les propriétés logiques. Prévoir états vide/chargement/erreur, 404 produit et contrôle clavier.

Tester le comportement changé, puis TypeScript et le build. Rapporter les vérifications réellement exécutées et les tâches restantes. Une licence déclarée par un agrégateur reste à vérifier chez le créateur. Un aperçu 2D valide la composition visuelle, la fabrication se valide dans le slicer puis sur prototype.

Remettre un résultat local reviewable avec les fichiers concernés. Conserver les prix démonstratifs identifiables jusqu’à validation de l’atelier.
