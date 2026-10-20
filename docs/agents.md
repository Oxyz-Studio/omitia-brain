# Agents and workspaces

The portable entry point is a file, not an agent-specific command:

> Read START-HERE.md and help me build or extend my company's brain.

An agent needs permission and the ability to read and edit the chosen workspace. Connecting remote sources or running unattended missions additionally requires suitable tools and a persistent execution environment. Support for those capabilities depends on the host.

## Entry points

| Environment | Entry |
| --- | --- |
| Any file-capable agent | Ask it to read [START-HERE.md](../START-HERE.md). |
| A host that reads `AGENTS.md` | [AGENTS.md](../AGENTS.md) routes setup, use, and kit maintenance. |
| Claude Code | [CLAUDE.md](../CLAUDE.md) points to the same canonical guidance. |
| Hosts that support repository skills | [.agents/skills/omitia-brain/SKILL.md](../.agents/skills/omitia-brain/SKILL.md); Claude Code receives a relative symlink at `.claude/skills/omitia-brain`. |
| Omitia Workspace or another shared workspace | Expose the kit and private brain as distinct resources, preserve audience and write permissions, and use the same entry and mission contracts. |

Automatic discovery is a convenience. Verify it in the installed host. If the skill is not discovered, use the explicit file entry; do not silently claim the skill was loaded. On systems that do not preserve symlinks, use `CLAUDE.md` and the explicit skill path, or recreate the relative directory link. Avoid maintaining two skill copies.

The private brain should have its own entry instructions, based on [brain-agents](../templates/brain-agents.md). Add a short host bridge where needed, such as `CLAUDE.md` pointing to the private `AGENTS.md`, rather than copying the rules. For hosts without automatic discovery, the handover prompt should explicitly ask the agent to read the private entry first. That lets another agent enter the company workspace without depending on the first conversation or a specific person's global configuration.

## No agent-specific memory dependency

The important context lives in saved notes, source records, knowledge policy, and ingestion receipts. A runtime's short memory can point to these files. Apply the [compact-memory contract](context.md#keep-runtime-memory-compact) when deciding what to carry across sessions and before relying on a pointer.

Do not assume a new agent inherits a previous session, a user's private connector credentials, a running scheduler, or permissions granted in another environment. Read the persisted policy and confirm actual capabilities only when the requested action needs them.

## Integrating into an existing workspace

Reuse its organization rather than moving all content. Record how its home, source registry, policy, and history map to the kit's concepts. Keep an explicit reference to the kit version or commit used, so its guidance can be reviewed later.

Updates to the public kit are advisory to an existing company brain. Review relevant changes; do not replace company policies or generated notes with fresh template copies.

The skill depends on the kit's guides and missions. Do not copy the skill directory alone into another repository: its relative references would point to missing resources. Keep a full kit checkout available. Where a host supports directory symlinks, expose that same canonical `.agents/skills/omitia-brain` directory through relative links in the other workspace's `.agents/skills` and `.claude/skills`. Resolve the skill's real location before following its reference links. Check that the links and kit path are available to every intended contributor.

If linking is unsuitable, keep a short entry in the private brain that points the agent to the full kit checkout or explicitly supplied guide. This uses the method without installing a detached skill. Avoid maintaining multiple copies of the skill's rules.

## Capability limits

The kit does not provide authentication, access control, connectors, a scheduler, search infrastructure, or a model. It provides conventions for using capabilities already available and for recording what remains unavailable. See [scheduling](scheduling.md) for the difference between a mission file and a working background job, and [validation](validation.md) for the scope of evidence provided with the kit.
