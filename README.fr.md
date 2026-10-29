# Omitia Brain

**Construire une mémoire d'entreprise utile aux personnes et aux agents.**

Omitia Brain est un kit ouvert en Markdown pour enregistrer les connaissances métier, retrouver le contexte et le maintenir utile. Il fonctionne avec un agent capable de lire et modifier des fichiers ; Obsidian, les connecteurs et les tâches planifiées sont facultatifs. Ce dépôt contient la méthode, les modèles et les missions. Le brain de votre entreprise reste dans un espace privé séparé.

[English](README.md) · [Démarrer](DEMARRER.md) · [Principes](docs/principles.md) · [Exemple fictif](examples/studio-brain/README.md)

## Construire son brain

1. Téléchargez ou clonez ce dépôt et ouvrez-le avec votre agent.
2. Donnez-lui cette consigne :

   > Lis START-HERE.md et aide-moi à construire ou enrichir le brain de mon entreprise. Accompagne-moi en français. Utilise ce que je peux fournir maintenant, préserve l'existant et identifie la destination privée avant d'écrire.

3. Apportez un brief, des documents, un projet existant ou des outils connectés. Commencez par un sujet ou construisez un premier brain complet ; les questions sans réponse ne doivent pas bloquer le travail utile.

L'agent enregistre les connaissances étayées et montre comment les retrouver. Les prochains contributeurs reprennent depuis les instructions et conventions du brain.

Le démarrage propose explicitement une skill de consultation partagée, les historiques de tous les agents de travail sur les machines autorisées, leur reprise, l'ingestion continue et l'entretien, ainsi que le scan des dossiers de travail choisis. Le périmètre et les choix acceptés, différés ou refusés sont enregistrés ; une proposition n'installe aucune capacité. Voir la [découverte du travail](docs/work-discovery.md).

Le brain privé enregistre le [commit du kit utilisé](docs/agents.md#link-the-brain-to-the-method), consultable localement ou depuis l'origine enregistrée. Gardez une copie locale pour l'usage hors ligne ou la skill.

## Commandes de la skill

| Action | Claude Code | Codex CLI / IDE |
| --- | --- | --- |
| Créer ou reprendre | `/omitia-brain init` | `$omitia-brain init` |
| Voir ce qu'il reste à faire | `/omitia-brain status` | `$omitia-brain status` |
| Vérifier sans modifier le brain | `/omitia-brain check` | `$omitia-brain check` |
| Intégrer une source ou un historique borné | `/omitia-brain ingest <source>` | `$omitia-brain ingest <source>` |
| Inventorier les sources de travail autorisées | `/omitia-brain discover <périmètre>` | `$omitia-brain discover <périmètre>` |
| Corriger et entretenir dans le périmètre | `/omitia-brain maintain <périmètre>` | `$omitia-brain maintain <périmètre>` |

Utilisez la skill du dépôt découverte par votre agent, ou sélectionnez `omitia-brain` dans votre interface puis demandez l'action. Ajoutez le chemin privé si nécessaire. `init` préserve l'existant ; `status` est l'orientation courte, en lecture seule, qu'un agent fait en entrant dans un brain : ce qu'il reste à installer ou à rattraper sur cet hôte ; `check` expose preuves, inconnues et prochaines actions sans réparation ni reconstruction d'index. `discover` inventorie les métadonnées et propose des sources ou des lots, sans ingestion, installation ni création de jobs. `ingest` et `maintain` suivent la politique et les autorisations du brain. Les [commandes](docs/commands.md) comprennent aussi les consignes par fichier pour les autres agents.

## Réutiliser les principes

| Besoin | Références |
| --- | --- |
| Architecture et connaissance | [Principes](docs/principles.md), [assertions, provenance et dates](docs/knowledge-model.md) |
| Sens métier et calculs récurrents | [Définitions métier](docs/context.md#define-terms-that-affect-the-task), [relations](docs/knowledge-model.md#relationships-express-a-specific-claim), [métriques](docs/metrics.md) |
| Références et adaptations | [Bibliographie commentée](docs/design-references.md) |
| Recherche et contexte utile | [Recherche](docs/retrieval.md), [packs et mémoire compacte](docs/context.md) |
| Contributeurs, autorité et accès | [Gouvernance](docs/governance.md), [documents externes et restrictions](docs/external-references.md) |
| Sources et travail incomplet | [Sources](docs/sources.md), [continuité](docs/continuity.md) |
| Travail continu | [Ingestion](docs/ingestion-design.md), [planification](docs/scheduling.md), [fiabilité](docs/reliability.md) |
| Intégration aux agents | [Agents et espaces de travail](docs/agents.md) |
| Preuves et limites | [Couverture des mécanismes](docs/mechanism-review.md), [validation](docs/validation.md) |

La référence est en anglais ; l'accompagnement et les notes suivent votre langue. Les principes sont utilisables sans adopter une arborescence fixe.

## Garder la mémoire utile

Commencez par les [apports directs](recipes/direct-contributions.md), les [documents locaux](recipes/local-documents.md) ou les [conversations d'agents](recipes/agent-conversations.md). Le [guide des sources](docs/sources.md) oriente aussi vers les mails, documents partagés, messageries et outils métier.

Quand un accord existant couvre le travail courant, l'agent [garde les résultats utiles](docs/proactive-capture.md) sans nouvelle demande de sauvegarde : analyses sourcées et procédures vérifiées dans leur périmètre. L'ingestion autorisée des conversations rattrape les apports manqués et réutilise les sauvegardes antérieures sans les dupliquer.

Les [missions](missions/README.md) décrivent le résultat, le périmètre et les preuves attendues. Elles utilisent votre agent à la demande ou votre planificateur après définition des sources, de l'identité, des autorisations, de la cadence et des limites. Un fichier de mission seul ne travaille pas en arrière-plan. Les autorisations déjà accordées sont réutilisées.

Quand l'historique persiste et qu'un agent peut travailler sans intervention, la découverte planifiée est la voie principale d'ingestion ; manquer un hook ne doit pas cacher l'activité éligible. Un historique éphémère nécessite une capture autorisée ou une limite de reprise explicite. La [supervision](missions/supervise.md) observe la couverture réelle ; historique, sauvegarde et [restauration démontrée](missions/recover.md) restent distincts. Ces mécanismes peuvent rester manuels ou non configurés pour un petit brain.

Le kit fournit une méthode, sans moteur de recherche hébergé ni connecteurs préconfigurés. Vérifiez les [limites de validation](docs/validation.md) pour votre environnement.

Pour contribuer : [guide](CONTRIBUTING.md) et [changements](CHANGELOG.md). Les exemples sont fictifs ; les données d'entreprise restent privées. La [licence MIT](LICENSE) permet l'usage commercial.
