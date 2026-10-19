---
name: clocking-out
description: "Use when the user says \"Clocking out\", \"End session.\", or otherwise asks to close the session — dispatch to ending-session (close with continuity packaging unless declined) without becoming a second closeout orchestrator."
version: "2026-10-15"
source: "Drive CORE — clocking-out"
generated: "2026-10-18"
---

Generated from Drive CORE on 2026-10-18. Read-only mirror; edits here are overwritten.

CORE — clocking-out
Provider-neutral TCS Skill source · 2026-10-15
Status: source reconciled, provider-specific installation remains distinct.

PORTABILITY
This is a *thin provider-neutral activation layer*, not a second session-close owner. The exact 'End session.' consent gate and the distinct explicit 'Clocking Out' already-authorized packaging semantics survive unchanged. Native Library and installed-Skill references are implementation adapters, never assumed across providers.
Resolve the actual current source owners, execution capabilities, available specialist components and artifact stores at invocation. Never pretend that the named ChatGPT adapter is universally present. Exact user consent, status, chronology, permission and evidence gates are invariant.

FUNCTIONAL CONTRACT

# Clocking Out

**Dispatch to the existing session-close owner; do not become a second closeout orchestrator.** Clocking Out is the explicit user-invoked complementary entry point to `clocking-in`. It means close this session **with continuity packaging**, unless the user explicitly declines that packaging. It does not mean delete the chat, schedule an operation, or initialize a new agent.

## Route the user's exact request first

| User request | Route and authority |
| --- | --- |
| Exactly `End session.` | Delegate to `ending-session` **before any other reads or tools**. Its existing **Yes / No / Other** packaging-consent gate controls. Stop and await the user's answer; do not pre-package. |
| `Yes` after that gate | Continue through `ending-session` with packaging approved. Do not ask again or save twice. |
| `No` after that gate | Close briefly, no continuity file and no further reads/writes. |
| `Other` after that gate | Follow the provided alternate instruction; ask only if that instruction is materially ambiguous. |
| Explicit `Clocking Out` / `Clocking out` | Treat as an instruction to close **and package**, so delegate to `ending-session` as an already-authorized close-and-package request. Do not insert a duplicate consent gate. |
| `Clocking Out, but do not save/package` | Respect the contemporaneous refusal; close through the applicable session-close owner without persistence. |
| Other close request with no package decision | Delegate to the existing `ending-session` clarification/consent flow. |
| Readiness question only (`Are we ready to close?`) | Ask `ending-session` for a proportional readiness assessment; do not package, write or close merely because readiness was asked. |

When a previous Yes or No is part of an ongoing closeout, preserve that choice. Do not restart the confirmation loop after a child Skill loads.

## Compose the established closeout capability

1. **Primary delegation:** Invoke the installed `ending-session` Skill (or the actual provider-owned equivalent). It owns scope, consent, proportionate verification, specialist selection, final receipt and stopping. Pass the explicit packaging authorization/refusal through unchanged. Do not copy or rerun its entire flow here.
2. **Packaging dependency:** Once the session-close owner has packaging approval, have it invoke `conversation-continuity-packaging`. That specialist owns content selection, source-faithful summaries, correct subject-owned destination, deduplication, saving, readback and native opening reference. Do not create an independent competing packet algorithm.
3. **Optional specialist support, only when the closeout owner determines a real need:** `auditable-actions-tracing-and-logging` for significant writes; `company-knowledge-routing` for source ownership; `connective-tissue-safe-handling` for provenance/status conflicts; `space-artifact-processing` for nontrivial Space artifact handling; `getting-dressed` if the work position is missing; `in-session-phasing` for a genuinely substantial closeout. Invoke the smallest relevant subset; do not scan every source for ceremony.
4. **No agent startup during exit:** `agent-bootstrap` is not a closeout dependency. The word "bootstrap" in the design brief means **activate existing specialist capabilities**, not initialize the agent again.
5. **Accept the existing owner's verified result.** Surface accurate completed changes, still-open tasks and the verified continuity reference, or the exact failure/unsaved state. The user decides whether and when to delete a conversation. Never claim automatic deletion or safe retirement after an unverified save.

## Missing coordinator or persistence: conservative fallback

If `ending-session` is not installed or callable, report that fact, rather than claiming it ran. Apply only the minimal, portable behavior necessary to honor the user's request: preserve the exact `End session.` **Yes / No / Other** no-tools-before-answer gate; after explicit packaging permission, use an actually available packaging specialist and verified durable store. If neither exists, describe what was and was not preserved; a draft, in-memory response, or local temporary file is **not** a verified durable handoff. Do not fabricate a file reference or ask the user to delete the chat. If a save or readback fails, do not claim the handoff is durable or the chat is ready for deletion; do not fabricate a file reference. A capability gap is not permission to mutate an unrelated system.

The CORE has no requirement that the provider be ChatGPT or the task owner be Linear. A non-ChatGPT adapter may call that provider's genuine closeout and storage capabilities; do not imply equivalent Skills, Library, Memory, cross-seat access or native links exist without evidence.

## Boundaries and references

- `clocking-in` resumes and executes work. **This Skill does not restart or finish an unrelated task merely to justify ending the chat.** It records unfinished work as unfinished.
- Read [references/chatgpt-adapter.md](references/chatgpt-adapter.md) only for ChatGPT-specific coordinator, Library and link behavior.
- Read [references/acceptance-cases.md](references/acceptance-cases.md) when evaluating or changing the Skill.
- Read [references/provenance.md](references/provenance.md) when source attribution, proposal status or paired-Skill boundaries matter.

PROVENANCE
Reconciled from installed skills://clocking-out, 2026-10-15. Prepared by Archangel Chat at the user's request. Standard: private source (not published)

CANONICAL SUPPORTING RESOURCES — 2026-10-15
Source-faithful references and scripts are preserved as a native Drive text bundle under this Skill's source folder, labeled with their exact original relative paths. Reconstruct provider-native files from those labeled sections when adapting; script listings are not deployed executables. Resource bundle: private source (not published)
