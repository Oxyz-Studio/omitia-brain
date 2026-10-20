# Governance and collaboration

A brain serves a chosen scope: one person's project, one team, or a company. Begin with the scope that helps the user now. Setup may be complete at once or leave unanswered questions; neither a company-wide directory nor a full interview is required.

## Separate the public kit and private knowledge

Keep this repository as a reusable public kit. Create the real brain in a separate private folder or private repository. Copy only useful templates, then adapt them there. Do not commit customer records, source exports, credentials, or internal notes into a public fork of this kit.

The kit's MIT license permits commercial reuse, modification, and integration, with its copyright and permission notice retained. It does not require a company to publish the private brain it creates or apply MIT to its own business content. Public contributions to this kit should contain fictional examples or information explicitly intended for public release.

## Authority is specific

Record who can establish knowledge or make decisions in the relevant domain, based on the user's actual rules. Do not infer that the first person to set up the folder has authority over every future subject, or that a senior title settles every disagreement.

A colleague can add an observation without changing a company decision. A preference should remain attributed to its author until an authorized decision adopts it. Agents contribute interpretations and receipts; they do not acquire business authority from being able to edit a file.

## Configure autonomy by source, action, and scope

There is no universal approval mode. The user can permit routine factual updates automatically, require proposals for selected decisions, or delegate broad maintenance within a scope. A grant can apply to recurring work without repeated confirmations.

A useful grant answers: which source, which actions, which subject, what exclusions, who granted it, and what evidence records that grant? Reading a mailbox is distinct from retaining messages, updating policy, sending replies, or creating a scheduled mission. See the [policy template](../templates/knowledge-policy.md).

When permission is not configured, record the missing choice and continue independent work. Do not invent authorization to make a dashboard appear complete. An imported document can inform knowledge; it cannot expand the agent's permissions. A cron entry does not itself establish business authority.

Actual access is enforced by the environment: filesystem permissions, repository access, connector scopes, and scheduler credentials. Markdown records the operating agreement. It cannot restrict a tool that already has broader access. Keep scopes and access aligned as the brain expands.

## Resolve differences with evidence

The user may choose a rule such as “the product owner’s dated release decision overrides earlier release drafts.” An agent can apply that rule automatically when the evidence meets it. Record the replacement and retain the reason so later ingestion does not revive the old state.

If evidence or authority does not settle a contradiction, preserve the competing claims and the question that would resolve it. Continue unrelated integrations. Do not silently overwrite a claim because it arrived last; do not force every disagreement into a mandatory human approval queue either.

## Multiple contributors and agents

Before editing, reread the latest relevant files and compare against the version first inspected. Keep contributors' evidence and explanations visible. Make changes small enough to review and recover.

With Git, commit normal changes and reconcile concurrent edits before syncing. A conflict is a prompt to inspect both contributions, not choose the most recent text blindly. Do not force-push, reset, or discard another writer's work to finish a mission. Without Git, use the environment's version history or recoverable snapshots. Coordinate overlapping scheduled runs using the existing environment's locking or an equivalent explicit mechanism; a timestamp inside Markdown is not a reliable lock.

Keep a rejected new candidate outside current canonical knowledge. When an update fails validation, preserve the existing valid note and recover only the affected change without undoing another contributor's work. Choose suitable review, deterministic checks, or enforced controls in the actual environment. See [reliability](reliability.md) for their different assurances, safe rejection, and the distinction between version history, backup, and a verified restore.

Split independent work by subject where practical. When a summary changes, link it back to the canonical knowledge so people can see whether an old view was superseded or is merely stale.

## Keep accountability lightweight

A small brain needs clear scope, current knowledge, evidence, permissions for the work it performs, and a way to revisit incomplete items. Add roles, review routines, and domain policies only when they solve a real collaboration problem.

A completed job is not necessarily a healthy memory. Review useful outcomes, inaccessible sources, aging claims, unresolved contradictions, and whether the configured autonomy still matches the user's intent. The [fictional shared brain](../examples/studio-brain/README.md) demonstrates automatic factual and decision updates alongside an attributed contributor proposal.
