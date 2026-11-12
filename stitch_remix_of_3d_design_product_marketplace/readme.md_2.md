# Paquet de reprise MustDesign3D

Ce dossier rassemble le contexte partageable avec un autre agent ou modèle. Le README reçu en pièce jointe a été lu comme référence en lecture seule.

## Les deux versions prêtes à transmettre

- [Version Gemini](GEMINI_MASTER.md), contexte de projet, plan de travail et instructions pour le code et les images.
- [Version Copilot](COPILOT_MASTER.md), contexte de projet et déroulé orienté fichiers, terminal et vérification dans VS Code.

Chaque version inclut le prompt maître commun et peut être utilisée seule avec le code du projet ou le snapshot.

## Contexte complémentaire

- [Prompt maître commun](MASTER_PROJECT.md), décisions et suggestions classées P0/P1/P2.
- [Brief photo](PHOTO_PROMPTS.md), deux essais pilotes et prompts réutilisables.
- [Source du projet](PROJECT_SOURCE.md), export textuel des sources et manifeste des fichiers.
- [Plan de refonte détaillé](../05-plan-refonte-niches-et-photos.md).

## Préparer un autre agent

1. Choisir GEMINI_MASTER.md ou COPILOT_MASTER.md.
2. Donner le dossier du projet à l’agent ou joindre PROJECT_SOURCE.md.
3. Pour un travail photo, joindre PHOTO_PROMPTS.md et l’image du modèle ou du prototype approuvé.
4. Demander un lot P0 ciblé puis vérifier les sorties.
5. Récupérer le code et les médias, lancer les contrôles et régénérer l’export.

## Actualiser l’export

Depuis la racine, exécuter npm run handoff. Le script exporte les sources textuelles autorisées, le lockfile, les SCAD et les guides de reprise. Les assets binaires sont listés avec SHA256 et restent à transférer séparément pour une reprise complète.

Les variables d’environnement, credentials, node_modules, .next, journaux et données de navigateur sont exclus. Examiner le fichier avant de le joindre à un service externe.

Le script de recette est inclus comme source. Les PDF/DOCX reçus se trouvent hors du projet et peuvent être joints séparément pour un nouveau travail de recherche. Le contexte maître contient les décisions nécessaires à une reprise du code.

## État de cette reprise

Le catalogue est structuré en neuf concepts et trois collections. Les références sur devis sont distinguées des prix fixes. Les couleurs de départ sont bleu, noir, blanc et rouge. Les vues techniques sont séparées des médias commerciaux et le QR est généré depuis le lien HTTPS. Les anciens modèles restent consultables dans /modeles.

Les nouvelles photos de concept restent à produire avec le générateur choisi. La forme finale des nouveaux produits et les fichiers de fabrication associés restent à valider. Le code est livré pour une démonstration locale.
