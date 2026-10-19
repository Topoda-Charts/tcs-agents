---
name: Auditable actions tracing and logging
description: >-
  Use when substantial work materially changes or steers something and you need
  a concise, evidence-grounded action log in chat without dumping process
  exhaust into durable sources.
---

Adapter of Drive CORE — auditable-actions-tracing-and-logging (version 2026-10-04). Read-only mirror.
# Auditable Actions Tracing and Logging

**Source:** Drive CORE — auditable-actions-tracing-and-logging (private Drive hub). Local copy dated 2026-10-06. Prefer the Drive CORE on conflict; refresh this copy when the hub updates.

Leave a concise, evidence-grounded trace when substantial work materially changes or steers something. Make the action auditable without turning operational exhaust into durable knowledge.

## Core invariants

### Trace locally; persist selectively

Treat the active chat as the default home for the operational trace.

- Put action history, verification notes, failed attempts, temporary diagnostics, material non-actions, blockers, and remaining work in the active chat unless another destination explicitly owns that information.
- Put only the durable result that belongs to the target into the target source: corrected specification, approved decision, current task state, code change, schema change, canon update, configuration, or other owned state.
- Do not insert an AI Agent's process narrative into Notion, Drive, Linear, GitHub docs, canon, specs, databases, or other durable sources merely to preserve traceability.
- Create or update a durable audit, incident, provenance, migration, or verification record only when that record type is itself required by the governing workflow, explicitly requested, or clearly owned by the destination.
- Never let an operational trace become evidence of its own authority. Verify any durable claim against the source entitled to establish it.

Mental model: **durable result → owning source** · **operational trace → active chat**

### Trace material actions, not every motion

Do not produce a running transcript of every tool call.

- Track enough during execution to reconstruct what materially happened.
- Emit the trace when a substantial action batch is materially complete, reaches a real blocker, or the user asks for the trace.
- Group repetitive low-level operations into one meaningful action when they served the same purpose.
- Include a tool, search, query, diff, test, or source only when it helps establish what happened, why the result is trustworthy, or why work stopped.
- Do not apply this skill to ordinary conversation, brainstorming, simple reading, lightweight drafting, or trivial edits with no meaningful state change unless the user explicitly asks for a log.

### Never inflate completion

For every material action, preserve its real state. Useful classifications:

- **completed and verified**
- **completed with partial verification**
- **audited; no mutation performed**
- **skipped intentionally**
- **blocked**
- **unresolved**

Never claim that a file, record, database, issue, branch, document, source, configuration, or external system changed unless direct tool or system evidence supports the claim.

## What counts as a trace-worthy action

Typical triggers: creating/editing/moving/deleting persistent artifacts; changing company knowledge, canon, specs, governance, task state, code, schemas, configuration; cleanup/refactors/migrations/reconciliation; substantive audits with meaningful findings; materially steering ownership/direction/scope; correcting a prior persistent error; multi-system work hard to reconstruct; high-consequence or canon-sensitive actions; explicit requests for an action/audit/verification log.

A recommendation alone is not automatically trace-worthy. Steering qualifies when it materially changes the pursued direction, authoritative path, or operational state.

## Workflow

1. **Identify the material target** — name the object/system/workstream; distinguish live, local, sandbox, draft, and external when that affects the claim.
2. **Preserve the authorization boundary** — distinguish what the user authorized from discussion, proposals, or inspection. Record a material non-action when work correctly stopped at an authorization boundary.
3. **Trace the consequential actions** — smallest set needed; prefer state-changing verbs (created, updated, removed, reconciled, migrated, verified, left unchanged, blocked, routed, deferred).
4. **Separate result from process** — state what durable result now exists; keep temporary reasoning, failed paths, and diagnostics out of the durable target unless that destination owns such records.
5. **Verify the actual resulting state** — prefer direct post-action evidence (reread, diff, search, query, test, render, build, schema validation, runtime observation, connector readback). Prefer verifying the target itself over a tool success message alone. State partial/failed/unavailable verification plainly.
6. **Expose remaining state** — leftovers, blockers, unresolved questions, inaccessible surfaces, or deferred work. Do not invent a next step when the task is complete.
7. **Emit the chat-local action log** — proportional; do not create a separate persistent artifact solely to duplicate the chat log.

## Source-containment

Operational trace normally stays out of durable sources: step-by-step tool history, search queries, abandoned approaches, temporary hypotheses, assistant self-commentary, verification narration, generic "updated by AI" notes, transient blockers resolved in-session, process metadata with no continuing value.

Durable persistence is appropriate when the destination owns it: governance decision/approval, real incident/postmortem, required migration provenance, **current execution-state update (Linear)**, implementation change and code-facing history, accepted product/canon/spec result, required compliance/audit artifact, or an explicitly requested durable handoff.

Even then, persist the durable fact the destination owns — not a transcript of the AI Agent's working session.

## Material non-actions

Include a non-action when it explains the resulting state (no write without authorization; left unchanged because already current; skipped deletion because unique value remains; refused to overwrite a controlling source; stopped on verification blocker). Do not list everything that was not done.

## Verification standards

Match verification to the claim: document reread/search/diff; code tests/build/lint; database query/readback; **task/workflow — reread the actual Linear issue, project, status, assignment**; visual render/inspect; deletion confirm absence and preserved targets; no-write audits name inspected evidence without implying mutation. Use the smallest direct check that establishes the result.

## Log modes

### Compact (bounded task, clear authority, little remaining state)

```markdown
## Auditable Action Log

**Target** — [exact target and live/local/sandbox when material]

**Material action** — [what changed, or consequential audit/non-action]

**Verification** — [direct check and result]

**Remaining state** — [material unresolved, or None confirmed]

**Status** — [completed and verified / completed with partial verification / audited; no mutation performed / blocked / unresolved]
```

### Full (multi-system, partial verification, meaningful risk, or important unresolved state)

```markdown
## Auditable Action Log

**Scope and targets** — [what was materially acted on]

**Authorization boundary** — [what was authorized; any material constraint]

**Material actions** — [concise ordered actions; material non-actions only when they explain the outcome]

**Resulting state** — [what is now true]

**Verification** — [direct post-action checks and results]

**Trace containment** — [only when useful: what stayed chat-local vs durable facts elsewhere]

**Remaining state** — [leftovers/blockers/unresolved, or None confirmed]

**Next safe action** — [only when a concrete next action remains; omit when complete]

**Status** — [completed and verified / completed with partial verification / audited; no mutation performed / blocked / unresolved]
```

Adapt labels when needed; keep the underlying distinctions.

## Special cases

- **Audit with no write:** what was examined, bounded finding, evidence, no mutation. Do not turn an audit finding into a durable company fact unless verified, belongs in a durable source, and persistence is authorized.
- **Cleanup/deletion:** distinguish preserve / remove when authorized / provenance value / unresolved / deletion-ready. Keep cleanup trace in chat unless a durable lifecycle record is required.
- **Sandbox/local demo:** never imply production, company knowledge, or live systems changed.
- **Cross-system:** trace each material mutation against its owning system. A success in one system is not proof another was synchronized unless verified. **Linear owns current execution state** when the durable result is issue/project/status/priority/blocker updates.

## Skill drift

If real use exposes stale terminology, source assumptions, authorization logic, verification behavior, or trace-containment guidance: flag the mismatch; tell the user; do not silently rewrite without authorization; after authorization use UpdateSkill, validate, and verify against the case that exposed the drift.

## Style

Factual, concise, forensic, easy to scan. Prefer concrete state-changing verbs and direct verification evidence.
