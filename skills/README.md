# TCS skills — scrubbed, read-only public mirror

**Do not edit files here.** Every file in `skills/` is generated from the Tópoda Charts Studios Drive CORE skill packages (the source of truth) and is overwritten on the next sync. Propose changes against the Drive CORE instead.

This catalog indexes scrubbed public copies sourced from the Hub `skills/` tree. The Hub `skills/STATUS.md` and reviewed `skills/public-sync.json` determine eligibility. Private source links and identifiers are not published.

- Source of truth: the private Hub `skills/` tree and its reviewable eligibility marker.
- Refresh: skill updates are proposed through pull requests; the public `main` branch is never written directly by the sync workflow.
- Catalog: [manifest.json](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/manifest.json).

## Layout

```text
skills/<slug>/SKILL.md                           provider-neutral CORE (source of truth, scrubbed)
skills/<slug>/providers/xai/SKILL.md             Grok adaptation
skills/<slug>/providers/openai/SKILL.md          OpenAI / ChatGPT adaptation
skills/<slug>/providers/openai/agents/openai.yaml  OpenAI skill metadata (when present)
skills/<slug>/providers/anthropic/skill.md       Anthropic / Claude adaptation
skills/<slug>/providers/google/gem-definition.md Google Gemini Gem definition
```

Only adapters that actually exist are published. Each adapter's first line names the CORE version it adapts.

## Resolution rule

1. Find your provider's folder: `providers/xai`, `providers/openai`, `providers/anthropic`, or `providers/google`.
2. If `providers/<your provider>/` exists for the skill **and** the manifest marks it `"stale": false`, read that adapter.
3. Otherwise (no adapter for your provider, or the adapter is stale) read the root `SKILL.md`, the provider-neutral CORE, and adapt it to the tools you actually have.
4. If an adapter and the CORE disagree, the CORE wins.

An adapter is **stale** when its own date is older than its CORE's last edit. Stale adapters are kept as published but not rewritten; their first line says so.

## Raw URL pattern

- CORE: `https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/<slug>/SKILL.md`
- Adapter: `https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/<slug>/providers/<provider>/<file>` (exact URLs and SHA-256 hashes are in the manifest)

## Catalog

| Skill | CORE version | CORE | Adapters |
| --- | --- | --- | --- |
| `paying-attention` | 1.0.1 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/paying-attention/SKILL.md) | xai, openai, anthropic, google |
| `context-first-problem-solving` | 1.0.0 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/context-first-problem-solving/SKILL.md) | xai, openai, anthropic, google |
| `extrapolating-logically` | 1.0.0 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/extrapolating-logically/SKILL.md) | xai, openai, anthropic, google |
| `neighboring-concept-disambiguating` | 1.0.1 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/neighboring-concept-disambiguating/SKILL.md) | xai, openai, anthropic, google |
| `correcting-course` | 1.6.1 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/correcting-course/SKILL.md) | xai |
| `learning-from-mistakes` | 1.6.0 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/learning-from-mistakes/SKILL.md) | xai |
| `work-preparing` | 1.0.0 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/work-preparing/SKILL.md) | xai, openai, anthropic, google |
| `proposal-drafting` | 1.0.0 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/proposal-drafting/SKILL.md) | xai, openai, anthropic, google |
| `implementation-planning` | 1.0.0 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/implementation-planning/SKILL.md) | xai, openai, anthropic, google |
| `in-session-phasing` | 1.2.0 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/in-session-phasing/SKILL.md) | xai (stale), openai (stale), anthropic (stale), google (stale) |
| `citing-sources` | 1.0.0 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/citing-sources/SKILL.md) | xai |
| `connective-tissue-safe-handling` | 1.0.0 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/connective-tissue-safe-handling/SKILL.md) | xai, openai, anthropic, google |
| `memory-updating` | 1.6.0 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/memory-updating/SKILL.md) | xai, openai, anthropic, google |
| `conversation-continuity-packaging` | 1.0.0 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/conversation-continuity-packaging/SKILL.md) | xai, openai (stale), anthropic (stale), google (stale) |
| `library-file-processing` | 1.0.0 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/library-file-processing/SKILL.md) | xai, openai (stale), anthropic (stale), google (stale) |
| `space-artifact-processing` | 1.0.0 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/space-artifact-processing/SKILL.md) | xai |
| `suggesting-prompts-and-next-steps` | 1.0.0 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/suggesting-prompts-and-next-steps/SKILL.md) | xai, openai |
| `stripping-down-self-imposed-barriers` | 1.0.0 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/stripping-down-self-imposed-barriers/SKILL.md) | xai, openai |
| `dinner-tomorrow-me` | 1.0.0 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/dinner-tomorrow-me/SKILL.md) | xai, openai |
| `reference-media-prompts` | 1.0.0 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/reference-media-prompts/SKILL.md) | xai, openai, anthropic, google |
| `displaying-using-python` | 1.0.0 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/displaying-using-python/SKILL.md) | xai |
| `iui-research-panel` | 1.0.0 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/iui-research-panel/SKILL.md) | xai |
| `clocking-in` | 1.0.0 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/clocking-in/SKILL.md) | xai |
| `clocking-out` | 1.0.0 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/clocking-out/SKILL.md) | xai |
| `bumping-session` | 1.0.0 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/bumping-session/SKILL.md) | xai |
| `ending-session` | 1.0.0 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/ending-session/SKILL.md) | xai |
| `getting-dressed` | 1.0.0 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/getting-dressed/SKILL.md) | xai, openai, anthropic, google |
| `auditable-actions-tracing-and-logging` | 1.0.0 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/auditable-actions-tracing-and-logging/SKILL.md) | xai, openai, anthropic, google |
| `propagating-to-internal-sources` | 1.3.0 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/propagating-to-internal-sources/SKILL.md) | xai |
| `workspace-skill-maintenance` | 1.0.0 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/workspace-skill-maintenance/SKILL.md) | xai, openai, anthropic, google |
| `workspace-skill-changing-update` | 1.0.0 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/workspace-skill-changing-update/SKILL.md) | xai, openai, anthropic, google |
| `agent-bootstrap` | 1.3.1 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/agent-bootstrap/SKILL.md) | none |
| `communicating-effectively` | 1.3.0 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/communicating-effectively/SKILL.md) | none |
| `company-knowledge-routing` | 1.3.1 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/company-knowledge-routing/SKILL.md) | none |
| `wrapping-up-turn` | 0.1.0 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/wrapping-up-turn/SKILL.md) | none |
| `card-preflight` | 1.1.0 | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/card-preflight/SKILL.md) | none |

## Scope and privacy

This mirror publishes only skills cleared as public-safe. Internal document links and IDs, email addresses, local paths, issue keys, seat badges, private channel names, and personal details are removed or replaced with generic wording. Reading these files grants no access to private TCS systems and no authority over any agent.
