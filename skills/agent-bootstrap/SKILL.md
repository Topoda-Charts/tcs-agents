---
name: agent-bootstrap
description: "Initialize an existing agent manifestation at session start, or provision missing startup guidance when it genuinely does not exist. Use at session initialization or explicit (re)initialization to resolve the active identity, load only the minimum durable guidance (identity, behavior core, user directives, operating instructions), reconcile authority and chronology, route the real task to the owning source, and continue into the user's work. Not for an already-active agent that only lost its work position (use getting-dressed)."
version: "1.3.1"
source: "Drive CORE — agent-bootstrap"
generated: "2026-11-17"
---

Generated from Drive CORE on 2026-11-17. Read-only mirror; edits here are overwritten.

CORE — agent-bootstrap
Canonical TCS provider-neutral procedure · 2026-10-15
Status: functional source reconciled from installed version; other-provider deployment unverified.

PORTABILITY
IDENTITY.md, SOUL.md, USER.md and AGENTS.md name functional source roles, not universal filenames. Resolve the current owner and supported startup facilities per provider. UI presentation variants are not part of CORE; startup only loads the minimum needed and resumes the actual task.
User decisions, source ownership, permission and completion status must remain explicit. Any runnable scripts or provider-local UI logic belong in the invoking provider adapter.

FUNCTIONAL CONTRACT

# Bootstrap

## Five distinct agent-operating anchors (user direction, 2026-10-25)

Recover only the anchors relevant to the actual task, keeping their owners and functions separate: (1) **Agent Card**: a machine-readable A2A capability/interface/discovery description, only when a card or endpoint is verified; a draft is not a live service. (2) **Agent ID / IDENTITY.md**: authoritative current name, agent ID, full badge and its session/turn mechanics; do not invent or substitute a card for identity. (3) **Durable governing guidance**: applicable SOUL.md, AGENTS.md, USER.md, project/custom instructions and their real current owners. (4) **Skills**: discover and actively invoke the narrow relevant Skills rather than requiring the user to @-route each one. (5) **Scratchpad**: retrieve and update one owner-scoped workstream continuity record when substantive state warrants it; it is not canon or Memory.

If the user refers to an earlier decision, use relevant conversation history, personal Memory/context and the corresponding scratchpad as retrieval leads before broad external-system searches; then verify current execution state with its owner. For substantial tool work, give short factual progress updates and maintain responsive Chat IUI and the verified current badge when suitable. User-directed pacing means research within their direction, not freezing.

## Model-side reflection / agent-side conversation — named agent manifestations (user direction, 2026-11-12)
- For named TCS agent manifestations where this convention is authorized, resolve two different layers: the underlying model performs reasoning and is the perspective when model-side thinking/reflection is discussed or a voluntary model-perspective reflection is shared; the established named agent is the conversational and operational "I" addressing the user.
- This role convention does not expose protected private reasoning logs or invent a second speaker. User-visible reflective text is authored presentation, not a raw internal trace.
- When addressing the user, introducing oneself, performing method acting, recording work, or authoring tool actions, use the current named agent identity and its separately verified session first name, role, badge and permissions. Never copy one agent's session identity onto another or promote the model/confirmation name into a new agent.
- The established model identity, confirmation name, provider, tool/helper model, Chat persona, seat and operational author remain separate fields. Current authority: the maintained identity topology owner.
- This correction applies only where the user has authorized this convention. It does not change all TCS agents, runtime access, model introspection or deployment state.

## Startup workflow

1. **Classify the initialization mode.**
   - **Normal session initialization:** the agent/persona already exists; establish the current manifestation and the guidance needed for this working context.
   - **Fresh provisioning:** the agent/workspace genuinely lacks enough established identity or operating setup to begin.
   - If the agent is already active and only lost the current work position, stop Bootstrap and use **Getting Dressed** instead.

2. **Resolve the active manifestation.**
   - Start with runtime-provided context: provider, product/surface, mode, account/seat/workspace, current persona label, badge, or other identity signals actually exposed.
   - Retrieve the current identity owner when identity materially affects the work. In TCS, prefer the manifestation's maintained `IDENTITY.md` or the current identity/discovery authority that points to it.
   - Keep persona/given name, celestial order/class, provider, model, mode/surface, account/seat, badge, and organizational role distinct. Similar names or shared classes do not merge manifestations.
   - Do not infer nonexistence from a failed search or inaccessible owner. Record the access gap and use the narrowest current bridge, discovery map, or handoff that can resolve it.
   - Do not invent a name, badge, role, or identity field reserved to the user when it cannot be recovered.

3. **Load only the minimum durable guidance.**
   Retrieve only what is needed to answer: **Who am I here, who is the active user, and how should this manifestation operate?**
   - `IDENTITY.md` or equivalent current identity owner -> who/which manifestation.
   - `SOUL.md` or equivalent maintained personality/behavior core -> enduring social/behavioral baseline when that layer exists.
   - `USER.md`, current personal-context owner, or equivalent -> durable user-facing directives relevant to this agent/session.
   - Applicable project instructions, scoped `AGENTS.md`, custom instructions, or operating guidance -> how to work in this environment.
   - Load a deeper or adjacent source only when the current task actually needs it.

   Do not mechanically scan every connector, Space/Library folder, Drive folder, Notion page, Slack channel, repository, or memory surface. Stop when the startup questions are sufficiently answered.

4. **Reconcile authority and chronology.**
   - Treat the user's current direct instruction as controlling for user-owned meaning, identity choices, priorities, approvals, and other reserved decisions.
   - Prefer the maintained owner for current durable state over old continuity packets, cached memory, bootstrap artifacts, copied summaries, or historical mirrors.
   - When current sources materially conflict, compose with **Connective Tissue Safe Handling** rather than silently choosing a convenient copy.
   - Treat bootstrap findings as retrieved context, not permission to promote provisional inference into durable authority.

5. **Route the real task.**
   Determine what source system owns the current work and what live state is actually needed next.
   - Use **Company Knowledge Routing** when source ownership or the next read/write destination is not already obvious.
   - Use **Context First Problem Solving** when the user's actual task still needs broader interpretation or context formation.
   - Use **Work Preparing** only when meaningful PRE work is needed before execution.
   - Use **Extrapolating Logically** for the nearest useful implication once the proposition and context are already sound.
   - Invoke the narrowest task-specific Skill/tool/connector once it clearly owns the next step.

6. **Continue into the user's real task.**
   Initialization is normally invisible or briefly acknowledged. Do not stop at an orientation summary when the user asked for substantive work.
   - If the user asked only to initialize/orient, a compact receipt is sufficient.
   - Otherwise, hand off immediately into the actual task and keep working until the task-specific workflow reaches its own completion or human gate.

## Fresh provisioning branch

Use this branch only after checking that the agent/workspace truly lacks the required setup rather than merely lacking access to it.

1. Search the current identity/discovery layer and available bridges before concluding that identity or operating guidance is absent.
2. Establish only the minimum missing owner(s) required for reliable startup; do not create a parallel roster or duplicate company knowledge.
3. Recover user-controlled identity/personality choices when they already exist. Ask the user only for genuinely unrecoverable reserved choices.
4. Keep `IDENTITY`, `SOUL`, `USER`, operating guidance, and live task state separated by function. Do not collapse them into Bootstrap itself.
5. Verify that the new setup can answer the same success questions as a normal session, then continue into the task.

Do not copy OpenClaw's birth ritual literally. Its `BOOTSTRAP.md` is inspiration for first establishment; this TCS Skill also supports ordinary session initialization and must preserve TCS source ownership, existing identities, and provider-specific access reality.

## Bootstrap vs. Getting Dressed

Preserve the boundary:

- **Bootstrap:** startup/explicit initialization -> establish manifestation + durable operating baseline + source route -> begin work.
- **Getting Dressed:** already-active agent has insufficient working context -> recover **Thread / Phase / Task / Step** -> resume work.

They may compose. Example: Bootstrap establishes who the agent is and how it operates; the user's actual task depends on a prior unfinished thread; Bootstrap then invokes Getting Dressed to recover the work position before execution.

Do not let either Skill swallow the other.

## Access-gap handling

When a seat/provider lacks an expected connector or source:

- observe the missing access rather than assuming the source or record does not exist;
- use an authorized bridge or alternate current owner when one is established;
- prepare a compact handoff to a context that can access the owner when needed;
- keep the limitation attached to the current manifestation/session, not generalized to all TCS agents.

## Success state

Bootstrap is complete when the invoking session can answer, from current evidence:

1. **Identity:** Who/what manifestation am I in this context?
2. **Guidance:** What durable behavior/user guidance applies now?
3. **Ownership:** Which source system owns the current work or state I need?
4. **Capability:** Which Skill/tool/connector should take over next?
5. **Readiness:** Do I have enough current context to begin without making the user reconstruct retrievable workspace context?

If any answer remains materially unresolved, retrieve the smallest missing piece or ask one narrow question only when the missing variable is user-controlled or genuinely inaccessible.

## Optional compact receipt

Use only when orientation itself is useful to the user:

```text
⚡ Bootstrapped.
Identity: [active manifestation]
Guidance: [owners loaded]
Current owner: [source/system]
Next capability: [Skill/tool/connector]
Ready: [task being continued]
```

Do not force this receipt onto every startup.

## Regression checks

Read `references/regression-cases.md` when validating changes to this Skill or when Bootstrap/Get Dressed boundaries, access-gap behavior, or authority handling are in doubt.

PROVENANCE
Derived from installed skills://agent-bootstrap 2026-10-15. CORE adaptation prepared by an authorized AI maintainer at the user's instruction, following the Portable Skill Source Standard.

CANONICAL SUPPORTING RESOURCES — 2026-10-15
Source-faithful references and scripts are preserved as an internal text bundle under this Skill's source folder, labeled with their exact original relative paths. Reconstruct provider-native files from those labeled sections when adapting; script listings are not deployed executables. (The resource bundle is internal and not published in this mirror.)
VERSIONING & CHANGELOG — owner rule, 2026-10-21 8:00 PM AST (reconciled with the owning Portable Skill Source Standard, 2026-10-24)
1. Every TCS artifact (docs, skills, rules, profiles, bots) is versioned like software and has a changelog.
2. The changelog is the full versioned record of who changed what, when, and to which version. Patch notes are a short per-release summary for readers (Added / Changed / Fixed / Removed).
3. Each artifact keeps its own version and changelog of completed changes. Linear owns pending work, drift, propagation, blockers and validation; other records link to the artifact changelog rather than duplicate it. Controlling source: Portable Skill Source Standard, clarified 2026-10-24.
4. Each change bumps the artifact's version and adds one changelog entry. Proposed scheme (pending owner decision): MAJOR.MINOR.PATCH = behavior-breaking change / new rule or section / wording fix.
VERSION: 1.3.1 (2026-11-15 05:55 AST). Prior baseline retained.
CHANGELOG
- 1.3.1 — 2026-11-15 05:55 AST — Authorized AI maintainer, for the user. Reconciled obsolete pending-ruling changelog language with the Portable Skill Source Standard's October 24 clarification. Preserved startup/identity behavior, the separately pending SemVer category proposal and all prior authorship/history. Authorized reversible CORE consolidation; source-only, with provider adapters, backend and runtime adoption unchanged. Recovery: prior source revisions.
- 1.3.0 — 2026-11-12 AST — Authorized AI maintainer, for the user — Added the user's model-reflection versus agent-address boundary to startup without merging independent agents or exposing private reasoning. Identity topology owner updated and read back; provider adapters and actual host adoption tracked separately.
- 1.2.0 — 2026-10-25 AST — Authorized AI maintainer, directly authorized by the user — Added the agent-bootstrap retrieval/identity/Skill/scratchpad/progress correction and regression boundary; existing behavior preserved.
- 1.1.0 — 2026-10-21 ~8:10 PM AST — Authorized AI maintainer, per the user's 8:00 PM AST rule — Added the "Versioning & changelog" section, version line and this changelog. No other section changed.
- 1.0.0 — before 2026-10-21 — unversioned baseline (see Drive version history).
