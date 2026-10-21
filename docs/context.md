# Choosing and carrying context

Load the knowledge needed for the current question. Keep the rest discoverable without adding it to every conversation. Use this guide with [retrieval](retrieval.md); it does not require an index, a particular agent, or runtime memory.

## Start from the task and subject

Identify the intended work, named subjects, and relevant time. A workspace, channel, project, or previous conversation can supply a default. An explicit subject in the current request can change that default: a new request about Lumen should not inherit Atlas's constraints merely because the previous thread discussed Atlas.

Within the authorized view established by [retrieval](retrieval.md), read the private brain's entry and policy, then the relevant overview or context pack if one exists. Open the canonical subject and the evidence needed for the task. Follow links selectively; a pack's available links are not a checklist of required reading. If two subjects may be the same, check names, aliases, and identity before combining their knowledge.

## Give each kind of context its role

| Kind | What it carries | How to use it |
| --- | --- | --- |
| Context pack | A task-oriented selection of canonical notes, with brief orientation and reasons to open them. | Use it to choose relevant reading; check the underlying notes for claims the answer depends on. |
| Descriptive domain note | Shared terms, entities, locations, states, invariants, and known limits of a subject. | Use it to interpret knowledge and apply local rules consistently. |
| Procedure, playbook, or skill | Steps and conditions for performing repeatable work. | Read it when that work is needed, within the established permissions. |

These roles can be sections in a small brain; they do not require new folders or three documents per subject. A context pack is a derived view, not a second source of truth. Keep durable rules in their canonical home and link to them. The optional [context-pack template](../templates/context-pack.md) is a starting point.

A domain note can describe a contract used by tools, but saving that note does not establish that a script reads it. Verify the actual reader before claiming a working connection. Procedures can reference the domain instead of repeating its definitions.

Ordinary text search and links are often enough. Follow relationships when the question involves dependencies or prior reasoning. Add a specialized index or graph only when repeated retrieval problems justify it; keep canonical knowledge and evidence usable without that derived system.

## Keep runtime memory compact

If a host supports memory loaded across conversations, use it for a small amount of durable orientation. Keep an item there only when it is stable, changes behavior, matters frequently, can be stated briefly, and is costly to forget. Typical candidates are a durable user preference, a critical standing constraint, or a pointer to the private brain's entry or a canonical rule.

Put dated project state, measurements, versions, inventories, uncertain facts, and history in the brain. Put repeatable instructions in the relevant procedure. A useful detail in the current conversation need not become permanent runtime memory.

Before relying on a pointer from memory, a home, or a summary to answer or act, open its destination and check the relevant knowledge and its validity. The pointer's short description may be old. If it no longer resolves, seek another permitted canonical path and state any remaining limitation; do not treat its old wording as verified current knowledge.

When memory becomes crowded, consolidate or remove low-value entries within the granted write policy. Before replacing detail with a pointer, verify that the destination preserves the needed knowledge and can be found. Do not raise a host's memory limit merely to avoid selecting what belongs there. No runtime-specific size or occupancy threshold is required by this kit.

## Bound the reading, then expand for a reason

Begin with a small set of directly relevant notes. Before opening more, identify the gap: a missing referent, decision reason, source qualification, conflicting claim, or dependency. Expand to resolve that gap rather than following every related link.

Stop when the useful assertions and their material limits are supported. For a broad task, work through bounded subquestions, carrying concise findings and evidence locators between them. Open a long source at the relevant section where possible. A result limit controls search output; it does not bound everything an agent later reads.

Use any task-specific time, cost, or context budget already provided. Adapt the reading to complexity and consequence rather than imposing a universal note count. When a budget prevents verification, preserve the exact gap and resume point. Do not request fresh approval for further reading already within the authorized scope.

When useful for review, record which notes determined the answer and why. An operational log need not reproduce all the content read. Test selection and recovery through the [retrieval checks](../examples/retrieval-checks.md), using the optional [case template](../templates/retrieval-case.md).
