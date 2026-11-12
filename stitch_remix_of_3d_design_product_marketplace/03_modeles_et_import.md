# Modèles, licences et import

## 1. Registre initial

Relevé du 10 novembre 2026. « Résultat indexé » signifie que Search Service a exposé une fiche ou un extrait. Tous les candidats gardent le statut needs_review tant que la marketplace d’origine, la licence et le fichier n’ont pas été contrôlés. Ce registre recense des pistes et des liens.

| ID interne | Piste | Information disponible | Source |
| --- | --- | --- | --- |
| model-name-keychain | Porte-clés prénom paramétrique | Résultat indexé, auteur C4UStudio, fichier SCAD, CC BY-SA annoncé par l’agrégateur. La lecture directe a expiré | [Fiche SliSearch](https://slisearch.com/en/models/a2835fdd-4161-4afc-9e40-ca4f725e8437) |
| model-two-line | Porte-clés à deux lignes | Usage commercial mentionné dans le résultat indexé, détails chez le créateur à confirmer | [Fiche SliSearch](https://slisearch.com/en/models/e453cb73-515b-4ccc-90ed-964e156315b5) |
| model-cable-clip | Clip de câble | CC0 annoncé dans le résultat indexé, fichier et source à contrôler | [Fiche SliSearch](https://slisearch.com/en/models/a8c75b85-e141-43cd-9e0b-ffe699ddbbfe) |
| model-usb-holder | Support de câbles modulaire | CC0 annoncé dans le résultat indexé, géométrie et source à contrôler | [Fiche SliSearch](https://slisearch.com/en/models/0f518b80-01b6-4a13-8826-679aba259493) |
| model-room-signs | Plaques de pièces | Résultat relié à Printables, conditions commerciales à confirmer | [Fiche SliSearch](https://slisearch.com/en/models/e5353a97-544c-44a8-8fc0-9e9856c93ed7) |
| model-standard-keychain | Porte-clés personnalisable | Licence marketplace standard annoncée, permissions à contrôler | [Fiche SliSearch](https://slisearch.com/en/models/dba7c166-9720-435a-81b2-313c1e181b22) |
| model-business-card | Carte de visite imprimable | Usage personnel et non commercial annoncé dans le résultat, réserver à l’étude | [Fiche SliSearch](https://slisearch.com/en/models/dc34943c-c227-4573-8a35-34474ffdf247) |
| model-qr-generator | Générateur QR | Restriction non commerciale annoncée dans le résultat, réserver à l’étude | [Fiche SliSearch](https://slisearch.com/en/models/22660a2f-58c7-45d3-8453-0d69c1b6ce13) |

La piste plaque de bureau en 6e4d0130-1c44-4c2e-84b8-88a17f1f40b0 était indexée, mais la lecture directe a donné 404. La conserver uniquement dans le journal de recherche. [Adresse testée](https://slisearch.com/en/models/6e4d0130-1c44-4c2e-84b8-88a17f1f40b0)

Le filtre licence:commercial aide à trouver des candidats. La décision d’utilisation repose sur les conditions de la source originale et sur les droits des visuels séparément. [Documentation des licences](https://slisearch.com/en/docs/licences)

## 2. Requêtes de départ

Dans Search Service, effectuer des recherches ciblées, puis ouvrir les fiches qui répondent au besoin.

```text
site:slisearch.com/en/models/ "name keychain" "commercial"
site:slisearch.com/en/models/ "desk name" "license"
site:slisearch.com/en/models/ "QR stand" "commercial"
site:slisearch.com/en/models/ "cable" "CC0"
site:slisearch.com/en/models/ "door sign" "license"
```

Dans l’interface SliSearch, ajouter licence:commercial et privilégier un fichier paramétrique modifiable quand la personnalisation est nécessaire.

## 3. Constituer une bibliothèque utilisable

1. Choisir un concept dans le catalogue de démarrage.
2. Retrouver la page d’origine, le créateur et la version du modèle.
3. Lire les permissions pour les impressions commerciales, les modifications et la redistribution numérique. Identifier l’attribution requise.
4. Vérifier que les éléments tiers du modèle et les visuels ont leurs propres autorisations.
5. Conserver le lien et une preuve datée de licence ou d’achat dans le dossier interne du projet.
6. Télécharger le fichier depuis la marketplace autorisée lorsque les conditions le permettent.
7. Calculer SHA-256 sur le fichier, noter sa version et le conserver hors du dossier public du site.
8. Ouvrir le modèle dans Bambu Studio, vérifier sa géométrie et produire un prototype.
9. Photographier le résultat et rédiger une fiche MustDesign3D originale.
10. Faire passer la fiche en catalogue vendable après validation des droits, de la fabrication et du prix.

Les images de marketplace sont des références de recherche. La boutique utilise ses propres photos ou des médias dont le droit de publication est établi.

## 4. Import d’une liste de modèles

Prévoir un import administratif local avec prévisualisation. Une ligne contient au minimum sourceUrl, originalUrl si connu, creator, licenceLabel, observedAt, permissionCommercialPrint, permissionModify, permissionRedistribute, rightsEvidenceRef et reviewStatus.

- Les permissions valent true, false ou null selon les preuves.
- Dédupliquer par source et identifiant externe, puis rapprocher la source primaire. Une ressemblance de titre déclenche une vérification manuelle.
- Présenter les erreurs par ligne et conserver un bilan des lignes importées, mises à jour ou ignorées.
- Garder l’import en recherche jusqu’à validation explicite de chaque modèle.
- L’import traite des métadonnées. L’acquisition de fichiers reste une étape distincte.
- Une réimportation conserve les décisions, preuves et corrections manuelles. Une modification de licence crée une nouvelle observation et demande une revue.
- Un lien inaccessible garde son statut d’échec avec la date. Une reprise ne crée pas de doublon.

La source primaire est une URL externe, et le fichier détenu est un asset interne distinct. Cette séparation permet de suivre la provenance sans publier les fichiers de production.

## 5. État actuel

Aucun fichier de modèle ni média concurrent n’a été acquis pendant cette mise à jour documentaire. Les huit lignes du registre sont des pistes SliSearch, les 227 liens To7fa sont un inventaire public et la fiche 3DGIFI est une référence produit. La bibliothèque complète de SliSearch reste hors couverture du présent relevé.
