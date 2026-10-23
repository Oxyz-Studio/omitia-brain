# Documents outside the brain

Documents can stay in working folders, shared drives, or document services. Register useful sources and uses; one supplied file does not authorize scanning its entire personal folder.

## Choose what a reference enables

| Mode | What is authorized | What it does not establish |
| --- | --- | --- |
| Reference only | Retain permitted identifying metadata and a locator. | Permission to open, index, copy, or distill the document. |
| Live consultation | Read the selected material for an authorized question. | Permission to retain excerpts, answers, transcripts, or lasting knowledge beyond the granted use. |
| Knowledge integration | Extract and maintain selected durable knowledge with provenance and permitted audiences. | Permission to duplicate the whole source, edit it, change its sharing, or publish more widely. |

Record the permitted capabilities in the [source record](../templates/source.md); they are independent, not setup stages. A reference-only source is neither an ingestion backlog nor integrated content. Consultation grants must cover answer destinations and any conversation history under disclosure and retention policy.

## Make the locator usable without moving the source

Record only what the intended readers may know:

- A source identity and a locator that the configured environment can resolve.
- The authorized access route, owner or responsible role, and relevant host limitations.
- Item identity plus a version or observation marker when reading or tracking changes is enabled.
- The selected use, audience, and retention policy, or a reference to that policy.

A local path may fail for a colleague or unattended host; a browser-readable cloud URL may fail for a scheduled agent. Record these limits and configure authorized routes where needed. Never put credentials or secret-bearing links in notes.

Keep a usable locator alongside provider-supported stable IDs. Verify move behavior during setup; IDs may not survive moves between accounts or containers. For example, see [OneDrive addressing](https://learn.microsoft.com/en-us/graph/onedrive-addressing-driveitems); the kit supplies no Microsoft connector.

A shortcut or symlink supplies neither portable resolution nor access control. Respect workspace restrictions on external links. Without an authorized route, leave that capability unavailable and continue independent work.

## Source permissions and knowledge audiences

Apply the [access contract](governance.md#preserve-access-boundaries-through-derived-knowledge) before discovery, consultation, integration, or answering. Titles, locators, existence, and registrations can be restricted even when content stays elsewhere. Keep confidential references out of generally readable homes and registries.

Verify how the connector checks identities and source rights. A shared service account cannot confer its access on every member; interactive and background access may differ. Check the actual connector and current provider documentation, such as Microsoft's [delegated and application access](https://learn.microsoft.com/en-us/graph/permissions-overview).

## Keep references and dependencies current

Check reference-only link resolution only when authorized; metadata checks need not read document bodies. For consultation or integration, [continuity](continuity.md) identifies the version read and affected knowledge to revalidate. Detecting a change grants no integration permission.

Distinguish renames, moves, unavailable hosts, rights changes, deletion, and partial results. Absence does not disprove claims; changed rights may restrict retained knowledge and derivatives. Apply [revocation and retention](governance.md#handle-revocation-without-promising-recall), including historical-copy limits.

## Combine with an optional shared workspace

| Responsibility | Possible provider |
| --- | --- |
| Original documents and their working versions | Local folders, Microsoft 365, or another document host. |
| Knowledge model, provenance, continuity, and agent missions | This portable kit, adapted in the private brain. |
| Identities, enforced storage and retrieval boundaries, and audit | The existing environment, Omitia Workspace, or another suitable backend. |

Use an existing document host or shared workspace as appropriate; neither is required.

Verify source rights and destination enforcement, including derivatives and revocation. Backend file permissions do not prove that a connector imports per-document rights or summaries inherit them. State unsupported capabilities. The kit neither installs these controls nor requires Workspace; private policy still governs.

See the [fictional access cases](../examples/external-access.md) and [agent integration guidance](agents.md).
