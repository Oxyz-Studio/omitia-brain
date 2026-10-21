# Documents outside the brain

A document can remain in a person's working folder, a shared drive, or a document service. The brain does not need to become the document store. Register only the selected sources and uses that help the current task; do not scan an entire personal folder because one file was supplied.

## Choose what a reference enables

| Mode | What is authorized | What it does not establish |
| --- | --- | --- |
| Reference only | Retain permitted identifying metadata and a locator. | Permission to open, index, copy, or distill the document. |
| Live consultation | Read the selected material for an authorized question. | Permission to retain excerpts, answers, transcripts, or lasting knowledge beyond the granted use. |
| Knowledge integration | Extract and maintain selected durable knowledge with provenance and permitted audiences. | Permission to duplicate the whole source, edit it, change its sharing, or publish more widely. |

These are independent capabilities, not mandatory setup stages. A source can permit several uses, or only a reference. Record them in the [source record](../templates/source.md). A reference-only source is not an ingestion backlog; do not mark its contents integrated merely because its locator was registered. For live consultation, the permitted answer destination and any conversation history are also part of the disclosure and retention decision.

## Make the locator usable without moving the source

Record only what the intended readers may know:

- A source identity and a locator that the configured environment can resolve.
- The authorized access route, owner or responsible role, and relevant host limitations.
- Item identity plus a version or observation marker when reading or tracking changes is enabled.
- The selected use, audience, and retention policy, or a reference to that policy.

A local absolute path may work for one person but not a colleague or an unattended host. Record that limitation; configure an authorized route where sharing is needed. A cloud URL may open in a browser without being readable by the scheduled agent. Never place credentials or secret-bearing access links in notes.

Prefer provider-supported stable item identities where available, while keeping a usable locator. Do not promise that an identity survives every cross-account or cross-container move. Verify the service's behavior during setup. For example, Microsoft documents [ID-based and path-based OneDrive addressing](https://learn.microsoft.com/en-us/graph/onedrive-addressing-driveitems); this kit does not supply a Microsoft connector.

A filesystem shortcut or symbolic link is neither a portable resolver nor a permission boundary. Do not bypass a workspace's deliberate refusal to follow external links. If no authorized route exists, keep the selected capability unavailable and continue independent work.

## Source permissions and knowledge audiences

Apply the [access-boundary contract](governance.md#preserve-access-boundaries-through-derived-knowledge) before discovery, consultation, integration, or answering. A document's title, locator, existence, or source registration may itself be restricted. Do not put a confidential reference in a generally readable home or registry merely because the content is elsewhere.

For a cloud integration, establish how the actual access identity and source permissions are checked. A shared service account's ability to read a file does not authorize every workspace member to receive it. Interactive access and background-job access may differ. Microsoft distinguishes [delegated and application access](https://learn.microsoft.com/en-us/graph/permissions-overview); other providers have their own models. Check current official documentation and the real connector rather than assuming identical behavior.

## Keep references and dependencies current

For reference-only use, check link resolution only when authorized; a metadata check need not read the document body. For enabled consultation or integration, follow [continuity](continuity.md) to identify the version actually read and revalidate affected knowledge when content changes. Discovering a source change does not itself grant integration permission.

Distinguish a rename, moved file, unavailable host, changed rights, deletion, and partial search result. A missing source is not proof that its claims became false. A permission change may nevertheless require restricting retained knowledge and its derivatives. Apply [revocation and retention](governance.md#handle-revocation-without-promising-recall), including the known limits of historical copies.

## Combine with an optional shared workspace

| Responsibility | Possible provider |
| --- | --- |
| Original documents and their working versions | Local folders, Microsoft 365, or another document host. |
| Knowledge model, provenance, continuity, and agent missions | This portable kit, adapted in the private brain. |
| Identities, enforced storage and retrieval boundaries, and audit | The existing environment, Omitia Workspace, or another suitable backend. |

Reuse an existing document host when useful. A company can also choose to keep its documents in its shared workspace. Neither arrangement is required by the kit.

Before claiming a controlled integration, verify both source permissions and destination enforcement, including derived knowledge and revocation. A backend's file permissions do not prove that an external connector imports per-document rights or that summaries inherit them. Keep unsupported capabilities explicit. The kit does not install those mechanisms, require Workspace, or replace private policies with a hosted service's defaults.

See the [fictional access cases](../examples/external-access.md) and [agent integration guidance](agents.md).
