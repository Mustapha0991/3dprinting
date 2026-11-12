# MustDesign3D — Prompt maître du projet

## Mission

Tu reprends le développement de MustDesign3D, une marque marocaine d’objets personnalisés imprimés en 3D. Travaille dans le projet existant en lisant les fichiers réels avant une modification. Utilise ce prompt avec PROJECT_SOURCE.md si tu n’as pas accès au dossier du projet.

Le propriétaire veut une vitrine proche de la structure du catalogue To7fa, avec une identité et des créations MustDesign3D. La cible initiale est le Maroc, en français, avec personnalisation arabe et bilingue. La devise est MAD.

## État fonctionnel attendu et architecture

En cas d’écart entre les documents, suivre la demande actuelle du propriétaire et ce contexte de reprise, puis vérifier le code réel. Les recherches et anciens prompts restent des références datées.

Next.js App Router, React, TypeScript strict, Tailwind, Node 22.x. Le lockfile fixe les versions installées. Le catalogue autoritaire est côté serveur, les options et le panier ont des contrats TypeScript partagés. Les montants sont des centimes entiers. pricingMode=quote donne priceCents=null et le libellé « Sur devis ».

Routes, /, /shop, /product/[slug], /modeles, /custom, /business, /contact, /checkout, /api/products, /api/orders et /api/quotes.

Le site reste en mode démo local. Les routes POST commandes/devis renvoient 403 DEMO_MODE avant lecture du corps. Le panier est une composition locale conservée dans localStorage avec validation à la restauration.

## Sélection commerciale

| Collection | Référence | Prix indicatif |
| --- | --- | --- |
| Cadeaux personnalisés | Porte-clés prénom | 49 MAD |
| Cadeaux personnalisés | Porte-clés plaque marocaine | 45 MAD |
| Cadeaux personnalisés | Étiquette de sac | 39 MAD |
| Cadeaux personnalisés | Marque-places, lot de dix | Sur devis |
| Maison & bureau | Plaque de bureau | 99 MAD |
| Maison & bureau | Plaque de porte | 99 MAD |
| Professionnels | Présentoir QR | 149 MAD |
| Professionnels | Plaque de contact | 99 MAD |
| Professionnels | Porte-clés logo en lot | Sur devis |

Trois vedettes, porte-clés prénom, plaque de bureau et QR. La skyline, la plaque pixel et le gabarit logo de bureau sont conservés comme prototypes. Les neuf fiches sont des concepts de catalogue, sept modèles CAD existent pour les études historiques. Vérifier la correspondance entre une fiche, son modèle et ses médias.

Ces prix servent à la démonstration. Calculer matière, purge, temps, travail, emballage et livraison avant une validation commerciale.

## Direction artistique

Fond ivoire, sable, anthracite et accent bleu Majorelle. Filaments de départ bleu, noir, blanc et rouge, deux couleurs préférées. La couleur du décor photographique est indépendante de celle du produit.

Catalogue avec recherche, trois collections, filtres latéraux sur ordinateur, panneau accessible sur mobile, prix/devis lisibles et cartes 4:5. Prévoir quatre colonnes sur grand écran et une densité adaptée aux tailles intermédiaires.

La boutique privilégie des médias commerciaux approuvés. Les aperçus CAD restent dans la galerie technique. Tant que les nouvelles images manquent, les illustrations originales du concept portent leur légende.

## Personnalisation et compatibilité

Conserver les six anciens slugs et les identifiants stables. Les prénoms français/arabe/bilingue ont une validation en graphèmes. Conserver la graphie, les accents et la liaison des lettres arabes.

Garder les noms, options et quantités du panier à travers les évolutions. Signaler clairement toute palette adaptée ou référence passée sur devis. L’ancien panier version 1 reste lisible.

Le QR doit encoder le lien HTTPS exact sans visite automatique de ce lien. Préserver la zone calme et le contraste. La vérification sur écran et le test de la pièce imprimée sont deux étapes distinctes.

Les références de petites séries passent par le parcours projet. L’ouverture des devis réels nécessitera un backend et une configuration commerciale.

## Fabrication et provenance

Machine A1 avec AMS Lite et quatre filaments. Viser une enveloppe conservatrice de 220 mm, une impression plate et peu de changements de couleur. Les réglages 0,4 mm / 0,20 mm / PLA sont un point de départ d’essai.

Les fichiers privés sont sous production/. Les images publiques sont des assets distincts. Enregistrer auteur, source, licence, permissions d’impression/modification/redistribution, version et SHA256 du modèle. Le guide MakerWorld fourni décrit le modèle d’Alberto Nicás v2.9, mais ses fichiers et conditions restent à acquérir.

Les pages To7fa, 3DGIFI, SliSearch et la liste A1_100_Product_References.md servent à la recherche. Une fiche commerciale et une requête de recherche de modèle apportent des informations différentes. Confirmer les droits de chaque fichier acquis.

## Photos et concepts générés

Avant une nouvelle série d’images, corriger la géométrie et choisir la version de produit à représenter. Générer une paire pilote, porte-clés et présentoir QR, puis évaluer formes, textes, dimensions apparentes et couleurs.

Médias possibles, photo, generated-concept ou cad-preview. Une image générée porte « Visualisation du concept ». Remplacer progressivement les vues commerciales par des photos de prototypes validés.

Un modèle de programmation Gemini sélectionné dans un éditeur travaille sur le code. La génération d’images nécessite un outil ou service d’image disponible dans l’environnement. Vérifier cette capacité et le crédit de génération avant le lot pilote.

## Séquence de travail

1. Lire ce document, l’état de livraison dans README.md et le plan de refonte.
2. Examiner les contrats, le catalogue, le panier et les composants qui affichent les médias.
3. Choisir un lot de travail parmi les tâches restantes, avec un résultat vérifiable.
4. Développer le lot en préservant les comportements existants.
5. Exécuter TypeScript, build et les scénarios navigateur adaptés.
6. Mettre à jour le README et régénérer PROJECT_SOURCE.md après les modifications.
7. Rapporter les fichiers modifiés, les tests réellement exécutés, les limites et la prochaine étape.

## Tâches suivantes prioritaires

- P0, corriger le porte-clés en contour et préparer une véritable version de production du QR. Associer une géométrie et une preuve de validation aux nouvelles références.
- P0, produire et approuver les deux images conceptuelles pilotes avant les vingt-sept vues de produits.
- P0, photographier les prototypes et mesurer les coûts réels.
- P1, ajouter la deuxième ligne des plaques et les champs structurés de plaque marocaine.
- P1, fait en démo locale : ajouter le nom de l’établissement et le type de destination du QR, conserver les compositions enregistrées et refléter le nom dans l’aperçu. La lecture sur pièce imprimée reste à valider.
- P1, préparer une variante double face du porte-clés après contrôle d’assemblage.
- P2, ajouter le suivi de stock de filaments et un tableau de production simple.
- P2, étudier PostgreSQL, commandes COD et devis réels après validation du parcours démo.

## Contrôle de livraison

TypeScript et build réussis. Vérifier 320, 390, 768, 1024 et 1440 px, clavier, filtre mobile, recherche/tri/URL, panier, données corrompues et anciens formats. Une référence sur devis ne doit pas devenir un article à prix nul dans le panier. Le QR encodé se décode vers le lien exact.

Garder codex.md et les documents reçus comme références. Les snapshots joints sont en lecture seule. Toute publication Railway et tout achat de domaine nécessitent une demande ultérieure explicite du propriétaire.
