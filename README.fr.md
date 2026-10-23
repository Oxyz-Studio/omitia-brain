# Omitia Brain

**Construire une mémoire d'entreprise utile aux personnes et aux agents.**

Omitia Brain est un kit ouvert fondé sur des fichiers Markdown pour organiser les connaissances d'une entreprise, retrouver le bon contexte et le maintenir à jour. Il fonctionne avec un agent capable de lire et modifier des fichiers locaux. Obsidian, les connecteurs et les tâches planifiées sont facultatifs.

Ce dépôt contient la méthode, les modèles et les missions en langage naturel. Le brain privé de votre entreprise reste dans un espace séparé, sous votre contrôle.

[English](README.md) · [Démarrer avec votre agent](DEMARRER.md) · [Comprendre les principes](docs/principles.md) · [Voir un exemple fictif](examples/studio-brain/README.md)

## Construire son brain

1. Téléchargez ou clonez ce dépôt et ouvrez le dossier avec votre agent.
2. Donnez-lui cette consigne :

   > Lis START-HERE.md et aide-moi à construire ou enrichir le brain de mon entreprise. Accompagne-moi en français. Adapte-toi à ce que je peux fournir maintenant et indique où seront rangés les fichiers privés avant de les écrire.

3. Apportez ce qui est disponible : une explication, des documents, un projet existant ou des outils connectés. Le démarrage peut être complet immédiatement, limité à un périmètre, ou repris plus tard.

Il n'est pas nécessaire de terminer un questionnaire pour obtenir un premier résultat utile. L'agent exploite les éléments disponibles, distingue les inconnues et reprend les informations existantes. Un collègue peut ensuite ouvrir le dossier de l'entreprise avec son agent pour y contribuer.

Si vous avez déjà un brain, demandez à l'agent de l'enrichir en respectant ses conventions plutôt que de le reconstruire.

Le brain privé enregistre la version du kit qu'il utilise. Les agents lisent cette version figée depuis votre copie locale ou depuis ce dépôt public : la copie locale devient facultative après le démarrage, mais reste utile hors ligne et pour la skill. Pour que vos agents consultent le brain pendant que vous travaillez ailleurs, demandez une skill de consultation du brain. Voir la [compatibilité agents](docs/agents.md#link-the-brain-to-the-method).

## Réutiliser les principes

Un CTO peut consulter la documentation sans suivre le démarrage guidé ni adopter l'arborescence proposée :

- [Principes et architecture](docs/principles.md).
- [Modèle de connaissance, provenance et dates](docs/knowledge-model.md).
- [Sélection du contexte, résumés et mémoire compacte](docs/context.md).
- [Autonomie et contributions](docs/governance.md).
- [Continuité entre ingestions et récupération du contexte](docs/continuity.md).
- [Recherche et historique](docs/retrieval.md).
- [Sources](docs/sources.md), [planification](docs/scheduling.md) et [compatibilité agents](docs/agents.md).
- [Documents conservés dans leurs dossiers ou services et partage contrôlé](docs/external-references.md) : références, consultation ou intégration, avec respect des droits jusque dans les résumés.
- [Fiabilité, supervision et restauration](docs/reliability.md) et [couverture des mécanismes](docs/mechanism-review.md).

La documentation de référence est en anglais. L'accompagnement et le contenu de votre brain suivent votre langue.

## Garder la mémoire utile

Les [missions](missions/README.md) décrivent des objectifs, un périmètre, des permissions et des résultats vérifiables. L'agent choisit les outils pour les exécuter ; le kit n'impose aucun script d'ingestion.

Les documents locaux, les apports directs et les conversations avec les agents disposent de parcours complets. Des recettes permettent d'adapter l'ingestion aux mails, aux espaces documentaires, aux messageries et aux outils métier disponibles.

Vous choisissez l'autonomie selon les sources et les actions. Les permissions déjà accordées évitent les validations répétitives. Pour exécuter une mission en arrière-plan, il faut un agent et un environnement de planification disponibles ; un fichier Markdown seul ne s'exécute pas.

Lorsque l'historique reste accessible et qu'un agent peut travailler en arrière-plan, l'ingestion planifiée est le mécanisme principal. Les hooks sont des accélérateurs ou des moyens de capture facultatifs ; leur absence ne doit pas empêcher le job de découvrir de nouveaux éléments. Si l'historique disparaît avant l'ingestion, une capture autorisée est nécessaire. Voir la [conception des ingestions](docs/ingestion-design.md).

Les missions de supervision recherchent aussi les travaux manqués et les contrôles devenus silencieux. La méthode distingue historique, sauvegarde et restauration réellement vérifiée. Ces mécanismes restent proportionnés aux besoins ; ils ne sont pas des prérequis administratifs pour commencer.

Les limites et le périmètre des vérifications sont explicités dans [Validation](docs/validation.md). Les recettes de connecteurs ne sont pas des intégrations préinstallées.

Le kit est sous [licence MIT](LICENSE), utilisable commercialement. Votre brain peut rester privé.
