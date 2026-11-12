# Modèles ajoutés à MustDesign3D

Reprise du 10 novembre 2026. Search Service a été utilisé pour consulter les trois références et rechercher la source primaire d’un candidat SliSearch.

## Intégration locale

La collection présente sept créations de démonstration, avec une page /modeles. Les six premières conservent leurs identifiants, leurs slugs et leurs prix indicatifs. La septième est une plaque pixel Zellige originale de 86 × 86 × 3,6 mm en trois couleurs. Son prix démo de 119 MAD est une hypothèse de présentation à confirmer par l’atelier.

Les sept sources OpenSCAD sont conservées dans production/. Les exports STL de configuration par défaut sont dans production/exports/. Les vues PNG du site ont été générées par OpenSCAD à partir de ces sources. Elles représentent les prototypes par défaut, et le configurateur conserve un aperçu 2D distinct pour les prénoms saisis.

Les assemblages, les graphies et les pièces séparées restent à contrôler dans Bambu Studio et sur une impression d’essai. Les prototypes QR/logo restent des gabarits. La plaque pixel est une décoration monobloc en relief.

## Recherche externe

- To7fa sert à étudier les familles, filtres et options du catalogue. Le relevé de 227 liens reste disponible dans 02-inventaire-to7fa.md. [Catalogue](https://to7fa.ma/produits)
- La fiche 3DGIFI sert de référence pour la présentation d’une création pixel. La plaque Zellige utilise une géométrie originale de trois couleurs et constitue une nouvelle piste MustDesign3D. [Fiche de référence](https://3dgifi.ma/product/pixel-emoji-collection/)
- Le candidat clip de câble repéré dans SliSearch a été relié à la fiche d’origine Cults de Nexo3d. La version indexée de cette fiche annonce CC0. La lecture directe et le téléchargement renvoient 403. Le fichier reste à acquérir chez le créateur et à vérifier avant intégration. [Fiche du créateur](https://cults3d.com/en/3d-model/gadget/universal-cable-clip-simple-cable-organizer-for-desk)

La page générale SliSearch reste inaccessible dans Search Service. Les découvertes ciblées apportent des pistes, et la bibliothèque externe conserve ses statuts de revue. [Guide de recherche et de licences](https://slisearch.com/en/docs/licences)

## Ajouter un prochain modèle

1. Acquérir le fichier depuis sa source autorisée et conserver les preuves d’utilisation.
2. Enregistrer l’auteur, la version et le SHA256 dans production/manifest.json.
3. Exporter en STL et contrôler les unités, dimensions et parties.
4. Générer une image dans public/models/ et déclarer sa provenance.
5. Ajouter le produit dans lib/catalogue.server.ts avec un id et un slug uniques, les dimensions connues et un schéma d’options adapté.
6. Garder status=demo jusqu’à validation du prototype et du prix.
7. Vérifier la fiche, la galerie, la recherche et le comportement du panier.
