# Source: {stable source name}

- Source ID: {stable identifier}.
- Scope and owner: {what this source covers; who can speak for it}.
- Location / access: {resolvable path or reference and authorized access method; no credentials}.
- Enabled uses: {reference only, live consultation, knowledge integration, or the explicitly permitted combination; a reference is not permission to read or distill}.
- Visibility: {who may discover this source's existence and metadata, read it, and receive answers or derived knowledge; link the applicable policy and enforcement route}.
- Source host / lifetime: {where the evidence lives and how long the chosen runtime can revisit it}.
- Execution and destinations: {mission configuration identifying the actual runtime, access identity, permitted storage and audience; no credentials}.
- Granted use: {link to the policy grant covering read, integration, and retention; otherwise not configured}.
- Availability: {available / unavailable / partly accessible / not configured}.

## Evidence and continuity

- Item and version identity: {stable item IDs plus revision, observed range, content fingerprint, or permitted snapshot; state any limits}.
- Context needed: {threads, earlier options, attachments, or dependencies; none if self-contained}.
- Retention / recovery: {permitted raw or captured evidence, temporary copies, where to recover originals, and deletion or expiry limits}.
- Rights changes / dependencies: {how relevant access changes are detected and affected notes or views found; limits or not configured}.
- Freshness: {validity or recheck rule for this source, if chosen}.

## Coverage

- Last observed range: {what was seen, even if not integrated}.
- Last fully integrated range: {what was actually reconciled with notes, with a saved receipt and successful retrieval readback}.
- Outstanding items: {link to incomplete claims or none}.
- Last useful success: {receipt and result, or never}.

An ingestion log carries detailed coverage. Do not advance completed integration past a gap without preserving that gap for retry. A source revision can require rechecking previously integrated claims.

Keep only fields useful to this source; runtime and destination details may be a link to shared mission configuration. A capture or run ID identifies delivery or execution, not the source version examined.
