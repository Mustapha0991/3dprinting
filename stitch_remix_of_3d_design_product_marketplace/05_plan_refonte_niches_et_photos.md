# Plan de refonte MustDesign3D — niches, produits et photographie

Document du 10 novembre 2026. Plan préparé à partir du rapport Morocco_3D_Printing_Niche_Research_Report.docx, du guide MakerWorld_Guide.pdf, du PDF All our pieces · To7fa et du catalogue To7fa consulté avec Search Service. La capture jointe montre les deux gabarits actuellement exposés dans la boutique.

## 1. Décisions de départ

### Positionnement

MustDesign3D devient une marque marocaine de personnalisation, centrée sur les cadeaux nominatifs et les objets utiles à la présentation d’une petite entreprise. Les collections sont Cadeaux personnalisés, Maison & bureau et Pour les professionnels.

Le rapport apporte une recherche documentaire et des hypothèses de lancement. Les fiches concurrentes confirment des offres et des prix affichés. Les ventes, volumes de demande et marges MustDesign3D restent à mesurer auprès de clients et sur les prototypes.

### Hypothèses retenues en attendant le retour du propriétaire

- Neuf références pour la première collection, puis trois extensions après tests.
- Français au lancement, personnalisation arabe et bilingue conservée.
- Filaments noir, blanc, bleu et rouge, selon le rapport et A1_100_Product_References.md.
- Habillage de marque ivoire et sable avec accent bleu Majorelle. Ces couleurs d’interface sont indépendantes des filaments proposés.
- Concepts visuels IA pour la démonstration, puis photographies des prototypes validés pour la vente.
- Site local et commandes fermées pendant cette refonte.

Les questions sur la sélection et les photos ont été envoyées au propriétaire. Une réponse différente conduit à réviser ces hypothèses avant l’implémentation.

### Ce que la référence To7fa apporte

Reprendre les principes observés, recherche visible, filtres latéraux, grille dense, images en situation, prix lisibles, pastilles de couleur et fiche personnalisable. Préparer les textes, objets et médias propres à MustDesign3D. [Catalogue To7fa](https://to7fa.ma/en/products)

Les deux rendus de la capture actuelle représentent un gabarit QR et un monogramme provisoire. Le travail de refonte porte sur leur conception, leur contenu, leur présentation et leur classement dans le catalogue. Un changement d’éclairage seul laisserait ces limites visibles.

## 2. Les trois niches et les neuf produits

Les prix ci-dessous sont des hypothèses de test pour le catalogue démo. Le passage à un prix commercial dépend du coût réel, du temps de machine, de l’emballage et de la livraison.

| Collection / clientèle | Produit à développer | Différenciation MustDesign3D | Prix démo proposé |
| --- | --- | --- | --- |
| Cadeaux personnalisés / particuliers | Porte-clés prénom en contour | Prénom latin ou arabe, base épousant la silhouette du texte, anneau renforcé | 49 MAD |
| Cadeaux personnalisés / particuliers | Porte-clés plaque marocaine | Composition lisible, numéros et lettre choisis, deux couleurs | 45 MAD |
| Cadeaux personnalisés / particuliers | Étiquette de sac | Prénom, choix d’un pictogramme original et fixation adaptée | 39 MAD |
| Cadeaux personnalisés / événements | Marque-places nominatifs | Lot de dix prénoms, typographie cohérente et série imprimée à plat | Sur devis pour le lot |
| Maison & bureau / particuliers et indépendants | Plaque prénom de bureau | Nom et fonction avec proportions typographiques contrôlées | 99 MAD |
| Maison & bureau / particuliers | Plaque de porte | Nom de famille ou pièce, deuxième ligne et fixation choisie | 99 MAD |
| Professionnels / cafés, salons et commerces | Présentoir QR | Véritable QR lié à un menu, une page ou une demande d’avis, socle stable | 149 MAD |
| Professionnels / commerces et indépendants | Plaque de contact | Enseigne compacte avec nom et identifiant social, présentation murale ou de comptoir | 99 MAD |
| Professionnels / petites séries | Porte-clés logo en lot | Géométrie simplifiée après accord du client et estimation par quantité | Sur devis |

Les quatre premiers produits sont personnalisables rapidement à partir de gabarits. Les présentoirs et petites séries visent des paniers plus élevés, avec un délai d’étude à mesurer.

### Priorité de prototypage et de présentation

Commencer par trois produits vedettes, le porte-clés prénom, la plaque de bureau et le présentoir QR. Faire approuver leur forme et une direction photo avant d’étendre la production d’images aux neuf références.

Le guide MakerWorld décrit un modèle paramétrique d’Alberto Nicás, version 2.9, avec modes simple face et double face en deux moitiés collées. Le PDF fourni décrit son fonctionnement. Le fichier source correspondant et ses conditions d’utilisation restent à obtenir. Une implémentation MustDesign3D peut être dessinée à partir du besoin fonctionnel avec une provenance propre.

### Références de prix observées

- Un porte-clés prénom est affiché à 35 MAD chez To7fa. La fiche présente notamment les graphies latines/arabe et le choix des couleurs. [Fiche To7fa](https://to7fa.ma/produits/porte-cles-prenom)
- Une plaque de porte est affichée à 79 MAD chez To7fa. [Fiche To7fa](https://to7fa.ma/produits/plaque-de-porte-classique)
- Un présentoir avec QR et NFC est affiché à 149 MAD chez To7fa. Comparer les fonctions et composants au moment du chiffrage MustDesign3D. [Fiche To7fa](https://to7fa.ma/en/products/presentoir-avis-nfc-qr)
- Un porte-clés de plaque marocaine est affiché à 50 MAD chez Slowy Wear au moment de la consultation. [Fiche Slowy Wear](https://slowywear.ma/product/porte-cle-immatriculation-marocaine-personnalise/)

### Extensions après le premier test

Étudier un porte-crayons nommé, un support téléphone simple et un ensemble de repères de câbles. Ces références enrichissent l’usage bureau lorsque les premiers produits ont une fabrication et une marge mesurées.

La skyline et la plaque pixel existantes passent dans une collection de prototypes. Le présentoir de logo se présente comme projet sur mesure avec un exemple typographique MustDesign3D. Leur visibilité commerciale dépend de la validation d’un modèle et d’un visuel approuvés.

## 3. Concevoir des produits représentables fidèlement

### Gabarits à corriger ou créer

1. Porte-clés prénom, base en contour, largeur nominale autour de 75 mm, œillet relié et renforcé, texte en relief sur une hauteur commune pour limiter les changements de couleur. Préparer une version simple face en premier.
2. Plaque marocaine et étiquette de sac, géométries plates indépendantes, proportions définies et fixation testée.
3. Plaques bureau/porte, noms et fonctions réellement lisibles, support et panneau séparables, proportions validées à l’échelle.
4. Présentoir QR, panneau noir/blanc contrasté sur socle bleu ou noir, vrai code généré depuis le lien saisi. Tester la lecture sur écran puis sur l’objet imprimé avant vente. Le NFC constitue une extension matérielle à chiffrer et tester.
5. Plaque de contact, vrai texte de démonstration choisi par MustDesign3D et identifiant clairement fictif.
6. Petites séries, gabarits de marque-places et porte-clés logo, liste de noms et coût de lot séparés du prix unitaire.

Pour les premiers modèles, viser deux couleurs et au plus trois changements réellement comptés dans le slicer lorsque la géométrie par couches le permet. Si une pièce demande de nombreux changements, préparer des composants monochromes et mesurer le temps d’assemblage.

### Vérification des modèles

- Enveloppe conservatrice de 220 mm, avec place pour les éléments de slicing.
- Buse 0,4 mm et couches 0,20 mm comme point de départ des essais.
- Contrôle des îlots, des lettres fines et des points de fixation.
- Validation de la liaison des lettres arabes avec une police autorisée et un tracé correctement façonné.
- Export des parties, slicing sur le profil A1, relevé matière utile/purge/temps, puis impression d’essai.
- Pour la double face du guide, prévoir les deux demi-bases, la correspondance des trous et le contrôle de la lecture après retournement et collage. Cette option s’ajoute après validation du simple face.

Chaque modèle possède une version, une provenance, les permissions nécessaires, ses dimensions et un résultat de prototype. La liste de cent références reste un outil de découverte. Les permissions et la géométrie se contrôlent fichier par fichier.

## 4. Nouvelle direction photo

### Style retenu

Lumière naturelle douce, ombres de contact, plastique mat avec stries fines cohérentes avec le FDM, échelle crédible et accessoires sobres. Décors secondaires possibles, bois clair, papier, tissu écru et comptoir de café. Le produit reste le point focal et ses couleurs correspondent aux filaments disponibles.

Le PDF To7fa sert de référence de mise en scène et de cadrage. Les images MustDesign3D montrent ses propres objets et personnalisations.

### Trois vues par référence

- Vue principale en situation, cadrage 4:5 pour la carte catalogue.
- Packshot sur fond ivoire, cadrage 1:1, proportions et détails visibles.
- Vue de détail ou d’échelle, cadrage 4:3, nom et assemblage lisibles.

Pour neuf références, prévoir vingt-sept images finales, puis une image d’accueil et trois vues de collection, soit trente et un médias. Produire ce volume après validation du premier essai.

### Première passe de validation

1. Choisir les modèles corrigés du porte-clés et du présentoir QR.
2. Produire une image conceptuelle de chacun avec le modèle corrigé comme référence géométrique.
3. Comparer au fichier de référence, contour, œillet, épaisseurs, textes, nombre de couleurs et socle.
4. Corriger la direction de prise de vue ou le modèle selon le problème observé.
5. Après accord sur cette paire, compléter les trois vues des trois vedettes, puis les six autres références.

### Utilisation possible de Gemini

Une intégration Gemini de génération d’images est disponible via le connecteur Runway dans cette session. À l’étape d’exécution, vérifier le compte, les crédits et le modèle disponible avant le lot pilote. Le présent plan n’engage aucune génération d’image.

Employer l’image du modèle corrigé ou la photo du prototype comme référence. Préserver le produit pendant le changement de décor et de lumière. Le texte, les logos et le QR doivent rester contrôlables, avec reprise du graphisme approuvé lorsque la génération les altère.

Les images de synthèse portent la mention « Visualisation du concept ». Les photos de prototypes validés remplacent progressivement les vues commerciales correspondantes. Une photo générée à partir d’un gabarit provisoire reste une représentation de ce gabarit.

### Exemple de prompt pour le lot pilote

> À partir de la référence du porte-clés MustDesign3D, conserver exactement son contour, son œillet, ses proportions, son épaisseur et son prénom approuvé. Présenter le produit en plastique FDM mat noir avec lettres blanches, posé sur une petite coupelle en bois clair près de clés métalliques. Lumière de fenêtre douce, ombre de contact réaliste, stries d’impression fines, vue trois-quarts, cadrage 4:5. Le produit occupe la majorité de l’image. Conserver les détails de la référence et la même palette de deux filaments.

### Contrôle des médias

Associer chaque image à productId, modelVersion, type de média et couleurs représentées. Vérifier les noms arabes visuellement, la cohérence entre les vues et la fidélité au prototype. Conserver une provenance distincte pour les médias et les fichiers 3D.

Export WebP/AVIF avec dimensions adaptées, 1 600 px pour les fiches et 2 400 px pour le visuel principal si nécessaire. Viser 150–250 Ko par image catalogue lorsque la qualité le permet, et conserver les sources haute définition séparément.

## 5. Refaire le catalogue et les fiches

### Structure du catalogue

- En-tête MustDesign3D compact, navigation claire, contact et panier.
- Titre de collection, nombre de produits et tri visibles.
- À partir de 1 440 px, barre de filtres d’environ 220 px et grille de quatre cartes.
- Sur écran intermédiaire, grille de trois cartes lorsque l’espace le permet.
- Sur mobile, filtres dans un panneau accessible et grille de deux cartes dès 360 px. Prévoir une colonne sur les plus petits écrans.
- Filtres par collection, type de produit, couleur réellement disponible, personnalisation et fourchette de prix.
- Cartes avec image 4:5 cohérente, nom court, prix indicatif ou devis, pastilles de couleur et action « Personnaliser ».
- Recherche, tri et filtres conservés dans l’URL avec navigation arrière fonctionnelle.

La bibliothèque technique /modeles devient un espace secondaire de consultation des prototypes. Les cartes de la boutique utilisent la nouvelle direction photo, avec leur statut de média explicite. Le personnage flottant de la capture appartient à l’interface hôte et reste extérieur aux compositions produit.

### Fiche produit

Prévoir une galerie de trois vues, les options adaptées au produit, un aperçu contrôlé, les dimensions validées ou indicatives, une quantité et un récapitulatif. Pour les lots, afficher le nombre de pièces et demander les noms ou le besoin de logo de façon explicite.

La personnalisation QR ajoute le nom du commerce, le type de destination et le lien. Encoder le code localement et conserver sa zone calme. Vérifier le décodage avant d’accepter une composition pour fabrication.

La version double face du porte-clés possède ses propres champs et son aperçu de face/dos. Préserver les saisies actuelles lors de l’évolution du contrat et revalider les anciennes compositions avec une explication si une nouvelle limite s’applique.

### Changements de données

- Garder les identifiants et slugs existants pour les produits conservés.
- Ajouter les nouvelles références avec identifiants stables et une distinction entre référence et variante.
- Ajouter pricingMode=fixed ou quote. Conserver priceCents entier pour les prix fixes et utiliser null pour les devis. Les cartes, fiches et API affichent « Sur devis » pour ces références. Une valeur nulle ne donne jamais un prix à zéro.
- Conserver les trois collections principales avec les categoryId existants adaptés, et afficher Décoration dans l’espace des essais.
- Compléter ProductImage par un type photo, generated-concept ou cad-preview, une provenance et la version du modèle représenté. Prévoir une conversion des anciennes lignes contenant isDemo.
- Séparer les images commerciales, les aperçus de personnalisation et les fichiers privés de production.
- Prévoir les palettes par produit et par stock de filaments. Le bleu, noir, blanc et rouge constituent la première hypothèse.
- Faire évoluer les contrats de panier de manière versionnée, avec conservation/revalidation des saisies existantes.

Les principaux points d’entrée du code sont le catalogue serveur, la carte produit et le composant de média. La refonte réutilise les parcours de personnalisation et de panier déjà testés.

## 6. Ordre d’exécution et critères de validation

### Lot 1 — Cadrage commercial

Valider les neuf références, les couleurs disponibles, les formes des trois vedettes et les prix de démonstration. Pour la demande réelle, fixer comme objectif interne vingt échanges qualifiés avec des acheteurs potentiels et cinq demandes de devis. Ces valeurs sont des objectifs de test.

### Lot 2 — Modèles et preuves

Corriger les modèles des trois vedettes, vérifier les sources/licences/polices, exporter les parties et mesurer les coûts dans Bambu Studio. Photographier les premières impressions lorsqu’elles sont disponibles.

### Lot 3 — Direction photo

Créer la paire de visuels pilote, l’évaluer avec les références, puis produire le reste de la série après approbation. En cas de compte de génération indisponible, préparer les prompts et les références pour une exécution par le propriétaire.

### Lot 4 — Refonte locale

Adapter la grille, les filtres, les galeries et les contrats de médias. Ajouter les nouveaux produits et options. Rétablir les anciennes compositions du panier selon la migration prévue.

### Lot 5 — Recette

- Chaque référence a un visuel approuvé, une provenance et un statut de fabrication explicite.
- Le QR de démonstration se décode vers son lien exact. La lecture sur objet imprimé sera vérifiée séparément.
- Les textes français/arabe et les couleurs concordent entre le formulaire, les images de référence et le panier.
- Les cartes et filtres sont utilisables à 320, 390, 768, 1 024 et 1 440 px.
- Navigation clavier, focus du panneau de filtres et du panier, retour arrière et anciennes compositions vérifiés.
- TypeScript, build et recette navigateur réussis.
- Coût réel et gain par heure de machine calculés avant publication commerciale.

La sortie de cette phase est une nouvelle vitrine locale reviewable. La génération automatique de fichiers de production depuis une commande, l’administration complète, les paiements et la publication Railway appartiennent aux étapes suivantes.

## Sources de travail

- [Rapport de niches fourni](C:/Users/mekka/Downloads/Morocco_3D_Printing_Niche_Research_Report.docx)
- [Guide MakerWorld fourni](C:/Users/mekka/Downloads/MakerWorld_Guide.pdf)
- [PDF catalogue fourni](C:/Users/mekka/Desktop/All%20our%20pieces%20%C2%B7%20To7fa.pdf)
- [Liste interne de cent références](A1_100_Product_References.md)
- [Brief MustDesign3D](00-master-mustdesign3d.md)

Le texte annoncé « Pasted text #1 » n’apparaît pas comme pièce textuelle distincte dans les éléments reçus. Le plan s’appuie sur la capture jointe, les trois documents accessibles et le brief existant.
