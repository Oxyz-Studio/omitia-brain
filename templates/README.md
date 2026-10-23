# Templates

Copy only the templates needed into a **separate private folder**. Do not put company information in this public kit. Start with `brain-home.md` as `README.md`, `brain-agents.md` as `AGENTS.md`, and `knowledge-policy.md` as `KNOWLEDGE_POLICY.md`. Add `SOURCES.md` as a small source registry and `INGESTION_LOG.md` when the provided material makes them useful. Create other files when there is something useful to record.

The agent can complete setup in one conversation or leave a smaller working brain, depending on the user's answers. A missing connector, unanswered question, or unavailable colleague does not block unrelated work.

| Template | Intended use |
| --- | --- |
| [Brain home](brain-home.md) | Scope, entry points, current usefulness, setup resume point. |
| [Agent instructions](brain-agents.md) | Reading, writing, continuity, and collaboration rules. |
| [Knowledge policy](knowledge-policy.md) | User-selected authority, autonomy, source, and retention rules. |
| [Source](source.md) | One source's access, boundaries, and processing coverage. |
| [Note](note.md) | A durable fact, practice, hypothesis, or reference. |
| [Decision](decision.md) | An actual decision, its authority, reasons, and consequences. |
| [Ingestion log](ingestion-log.md) | Versioned source coverage and unresolved items. |
| [Mission](mission.md) | A natural-language job for the existing agent environment. |
| [Run report](run-report.md) | Evidence of a mission's useful result, limits, and next work. |
| [Context pack](context-pack.md) | Optional task-oriented reading map linked to canonical notes. |
| [Retrieval case](retrieval-case.md) | A representative question with evidence, limits, and failure criteria. |
| [Health status](health-status.md) | Dated observation of expected work, verified coverage, and missing proof. |
| [Brain skill](brain-skill.md) | Optional query skill that lets agents consult the brain from other work. |

Text in `{braces}` is an instruction to adapt, not a fact to assume. Keep unknown information as `unknown` and unmade configuration choices as `not configured`. Do not invent people, permissions, schedules, source access, dates, or decisions to complete a template. Remove unused sections instead of maintaining empty forms.

The filenames and folders are suggestions. Preserve a clear entry point and working links when adapting them. A small brain can use one notes folder, one source record, and one receipt. A larger organization can add domain entry points without changing the principles.

Check how the contributors' agents discover instructions. A short `CLAUDE.md` can point to the private `AGENTS.md` when needed; other hosts may require an explicit prompt to read the entry. See [agent compatibility](../docs/agents.md). Keep the rules in one place. Record the kit version in the `AGENTS.md` method reference; see [linking the brain to the method](../docs/agents.md#link-the-brain-to-the-method).

See the [small fictional brain](../examples/studio-brain/README.md), [knowledge model](../docs/knowledge-model.md), and [governance](../docs/governance.md).
