# Source: {stable source name}

- Source ID: {stable identifier}.
- Scope and owner: {what this source covers; who can speak for it}.
- Location / access: {resolvable path or reference and authorized access method; no credentials}.
- Granted use: {link to the policy grant covering read, integration, and retention; otherwise not configured}.
- Availability: {available / unavailable / partly accessible / not configured}.

## Evidence and continuity

- Version or range identity: {revision, export date, message IDs, file hash, or another repeatable identity}.
- Context needed: {threads, earlier options, attachments, or dependencies; none if self-contained}.
- Retention / recovery: {what may be retained, where to recover originals, and known limits}.
- Freshness: {validity or recheck rule for this source, if chosen}.

## Coverage

- Last observed range: {what was seen, even if not integrated}.
- Last fully integrated range: {what was actually reconciled with notes, with a saved receipt and successful retrieval readback}.
- Outstanding items: {link to incomplete claims or none}.
- Last useful success: {receipt and result, or never}.

An ingestion log carries detailed coverage. Do not advance completed integration past a gap without preserving that gap for retry. A source revision can require rechecking previously integrated claims.
