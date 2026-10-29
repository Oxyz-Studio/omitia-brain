# Démarrer avec votre agent

Ouvrez ce dossier avec votre agent et dites-lui :

> Lis START-HERE.md et accompagne-moi en français pour construire ou enrichir le brain de mon entreprise. Utilise ce que je peux fournir maintenant. Préserve ce qui existe déjà et indique où seront écrits les fichiers privés.

[START-HERE.md](START-HERE.md) est la procédure de référence. Vous pouvez apporter un brief complet, quelques documents ou un seul besoin, puis reprendre plus tard ; aucun questionnaire ni connecteur n'est obligatoire.

Si la skill `omitia-brain` est découverte :

| Action | Claude Code | Codex CLI / IDE |
| --- | --- | --- |
| Créer ou reprendre | `/omitia-brain init` | `$omitia-brain init` |
| Voir ce qu'il reste à faire | `/omitia-brain status` | `$omitia-brain status` |
| Vérifier sans modifier | `/omitia-brain check` | `$omitia-brain check` |
| Intégrer une source ou un historique borné | `/omitia-brain ingest <source>` | `$omitia-brain ingest <source>` |
| Inventorier les sources autorisées | `/omitia-brain discover <périmètre>` | `$omitia-brain discover <périmètre>` |
| Corriger et entretenir | `/omitia-brain maintain <périmètre>` | `$omitia-brain maintain <périmètre>` |

Ajoutez le chemin du brain privé si nécessaire. Dans une interface à sélecteur de skills, choisissez `omitia-brain` puis demandez l'action. Un agent qui entre dans un brain fait d'abord un `status` court : skill de consultation absente sur cet hôte, sessions jamais ingérées, entretien en retard, sans rien modifier ni bloquer votre demande. `discover` reste un inventaire de métadonnées sans ingestion, installation ni création de jobs ; `ingest` et `maintain` suivent la politique et les autorisations du brain. Voir les [commandes](docs/commands.md).

L'agent enregistre les connaissances et leurs sources dans votre espace privé, séparé du kit, puis vérifie qu'on les retrouve. Il propose la consultation partagée entre vos agents, les historiques de travail accessibles, leur reprise, l'ingestion continue et l'entretien, ainsi que les dossiers de travail choisis : le périmètre et les choix sont explicites, sans installation automatique. Les missions utilisent votre environnement existant et les autorisations déjà accordées.

Pour les options et les principes : [README français](README.fr.md), [modèles](templates/README.md), [missions](missions/README.md) et [exemple fictif](examples/studio-brain/README.md).
