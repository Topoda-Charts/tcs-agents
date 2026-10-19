---
name: auditable-actions-tracing-and-logging
description: "Trace and report consequential AI Agent actions after substantial work materially mutates, updates, removes, migrates, reconciles, or steers a target or workstream. Use after persistent writes, substantive audits, cleanup/refactors, source corrections, migrations, implementation changes, connected-system updates, significant state/strategy steering, or when the user asks for an audit trail, action log, verification receipt, or trace of what happened. Keep operational traces in the active chat by default; persist only the durable result that the owning source actually needs unless a durable audit record is explicitly warranted and authorized."
---

Adapter of Drive CORE — auditable-actions-tracing-and-logging (version 2026-10-04). Read-only mirror.

# Auditable Actions Tracing and Logging

Leave a concise, evidence-grounded trace when substantial work materially changes or steers something. Make the action auditable without turning operational exhaust into durable knowledge.

## Core invariants

### Trace locally; persist selectively

Treat the active chat as the default home for the operational trace.

- Put action history, verification notes, failed attempts, temporary diagnostics, material non-actions, blockers, and remaining work in the active chat unless another destination explicitly owns that information.
- Put only the durable result that belongs to the target into the target source: the corrected specification, approved decision, current task state, code change, schema change, canon update, configuration, or other owned state.
- Do not insert an AI Agent's process narrative into Notion, Drive, Linear, GitHub documentation, canon, specifications, databases, or other durable sources merely to preserve traceability.
- Create or update a durable audit, incident, provenance, migration, or verification record only when that record type is itself required by the governing workflow, explicitly requested, or clearly owned by the destination.
- Never let an operational trace become evidence of its own authority. Verify any durable claim against the source entitled to establish it.

Use the mental model:

**durable result -> owning source**
**operational trace -> active chat**

### Trace material actions, not every motion

Do not produce a running transcript of every tool call.

- Track enough during execution to reconstruct what materially happened.
- Emit the trace when a substantial action batch is materially complete, reaches a real blocker, or the user asks for the trace.
- Group repetitive low-level operations into one meaningful action when they served the same purpose.
- Include a tool, search, query, diff, test, or source only when it helps establish what happened, why the result is trustworthy, or why work stopped.
- Do not apply this skill to ordinary conversation, brainstorming, simple reading, lightweight drafting, or trivial edits with no meaningful state change unless the user explicitly asks for a log.

### Never inflate completion

For every material action, preserve its real state. Use one of these classifications when useful:

- **completed and verified**
- **completed with partial verification**
- **audited; no mutation performed**
- **skipped intentionally**
- **blocked**
- **unresolved**

Never claim that a file, record, database, issue, branch, document, source, configuration, or external system changed unless direct tool or system evidence supports the claim.

## What counts as a trace-worthy action

Use judgment and proportionality. Typical triggers include:

- creating, editing, moving, renaming, deleting, archiving, or replacing persistent artifacts;
- changing company knowledge, canon, specifications, terminology, governance, task state, code, schemas, configuration, or runtime-facing implementation;
- cleanup, refactors, migrations, reconciliation, propagation, or de-duplication;
- substantive audits that establish a meaningful finding even when no write follows;
- materially steering a workstream by resolving ownership, direction, scope, authority, or the next execution path;
- correcting a prior persistent error or preventing a consequential incorrect mutation;
- multi-system work where the resulting state would otherwise be difficult to reconstruct;
- destructive, irreversible, high-consequence, public-facing, legal, financial, architectural, or canon-sensitive actions;
- explicit requests for an action trace, audit log, verification log, or operational receipt.

A recommendation or conversational idea alone is not automatically trace-worthy. Steering qualifies when it materially changes the task's pursued direction, authoritative path, or operational state.

## Workflow

1. **Identify the material target.**
   - Name the object, system, workstream, or state that was materially acted on.
   - Distinguish live, local, sandbox, draft, and external targets when that affects the claim.

2. **Preserve the authorization boundary.**
   - Distinguish what the user authorized from what was merely discussed, proposed, inferred, or inspected.
   - Treat discussion, critique, exploration, naming, and design conversation as non-authorizing unless the user actually authorized an action.
   - Record a material non-action when work correctly stopped at an authorization boundary.

3. **Trace the consequential actions.**
   - Record the smallest set of actions needed to explain what materially happened.
   - Prefer state-changing verbs: created, updated, removed, reconciled, migrated, verified, left unchanged, blocked, routed, or deferred.
   - Preserve sequence only when order materially affects interpretation.

4. **Separate result from process.**
   - State what durable result now exists.
   - Keep temporary reasoning, failed paths, search history, diagnostics, and implementation exhaust out of the durable target unless the destination specifically owns such records.
   - If an action discovered durable information that belongs elsewhere, route or recommend it according to the owning workflow rather than embedding it in the trace's original target.

5. **Verify the actual resulting state.**
   - Prefer direct post-action evidence: reread, diff, search, query, test, render, build, schema validation, runtime observation, or connected-system readback.
   - Verify the target itself when feasible rather than relying only on a tool's success message.
   - State partial, failed, or unavailable verification plainly.

6. **Expose remaining state.**
   - Record meaningful leftovers, blockers, unresolved questions, preserved legacy state, inaccessible surfaces, or deferred work.
   - Do not manufacture a next step when the task is actually complete.

7. **Emit the chat-local action log.**
   - Keep it proportional to the work.
   - Do not create a separate persistent artifact solely to duplicate the chat log.

## Source-containment rules

Operational trace material normally stays out of durable sources. This includes:

- step-by-step tool history;
- search queries and retrieval attempts;
- abandoned approaches;
- temporary diagnostic hypotheses;
- assistant self-commentary;
- verification narration;
- generic "updated by AI" notes;
- explanations written only to prove that work occurred;
- transient blockers that were resolved within the same work session;
- process metadata with no continuing operational value.

Durable persistence can be appropriate when the destination legitimately owns the information, such as:

- a governance decision or approval record;
- a real incident or postmortem finding;
- required migration provenance;
- a current execution-state update;
- an implementation change and its code-facing history;
- an accepted product/canon/specification result;
- a required compliance or audit artifact;
- an explicitly requested durable handoff.

Even then, persist the durable fact or record the destination owns, not a transcript of the AI Agent's working session.

## Material non-actions

Include a non-action when it materially explains the resulting state, for example:

- a write was not performed because authorization was absent;
- a candidate source was left unchanged because it was already current;
- a proposed deletion was skipped because the target still had unique value;
- a lower-authority source was not used to overwrite a controlling source;
- an operation stopped because verification exposed a real blocker.

Do not list every thing that was not done.

## Verification standards

Match verification to the claim:

- **Document/source changes:** post-write reread, targeted search, or before/after comparison.
- **Code/configuration:** diff, tests, build, lint, schema validation, or runtime observation as appropriate.
- **Database/state mutation:** query/readback of the affected rows or state.
- **Task/workflow state:** reread the actual issue, project, status, assignment, or workflow object.
- **Visual/layout work:** render or inspect the resulting artifact.
- **Deletion/cleanup:** confirm absence where expected and confirm preserved targets remain intact when material.
- **No-write audits:** identify the inspected evidence and the bounded finding without implying a mutation.

Do not perform redundant verification merely to make the log look thorough. Use the smallest direct check that materially establishes the result.

## Log modes

### Compact mode

Use for a bounded task with clear authority, direct verification, and little remaining state.

`` ```markdown ``
## 🧾 Auditable Action Log

**🎯 Target**
[Exact target and live/local/sandbox context when material.]

**🛠️ Material action**
[What materially changed, or the consequential audit/non-action.]

**✅ Verification**
[Direct check and result.]

**📍 Remaining state**
[Anything material still unresolved, or `None confirmed`.]

**📌 Status**
[completed and verified / completed with partial verification / audited; no mutation performed / blocked / unresolved]
`` ``` ``

### Full mode

Use when work spans multiple systems or targets, changes direction materially, has partial verification, carries meaningful risk, or leaves important unresolved state.

`` ```markdown ``
## 🧾 Auditable Action Log

**🎯 Scope and targets**
[What was materially acted on.]

**🔐 Authorization boundary**
[What was authorized and any material boundary that constrained action.]

**🛠️ Material actions**
[Concise ordered actions; include material non-actions only when they explain the outcome.]

**🧾 Resulting state**
[What is now true in the affected systems or workstream.]

**✅ Verification**
[Direct post-action checks and their results.]

**🧭 Trace containment**
[Only when useful: what operational detail remained chat-local and what durable facts were legitimately persisted elsewhere.]

**📍 Remaining state**
[Leftovers, blockers, unresolved questions, inaccessible surfaces, or `None confirmed`.]

**➡️ Next safe action**
[Only when a concrete next action remains. Omit when complete.]

**📌 Status**
[completed and verified / completed with partial verification / audited; no mutation performed / blocked / unresolved]
`` ``` ``

Adapt labels when the task needs different terminology, but preserve the underlying distinctions.

## Special cases

### Substantive audit with no write

Trace what was examined, the bounded finding, the evidence used, and the fact that no mutation occurred. Do not turn an audit finding into a durable company fact unless it is verified, belongs in a durable source, and persistence is authorized.

### Cleanup and deletion review

Distinguish:

- current value that must be preserved;
- obsolete or duplicate material that can be removed when authorized;
- historical material that still has provenance value;
- unresolved material that blocks deletion;
- final deletion readiness.

Keep the cleanup trace in chat unless a durable lifecycle or provenance record is actually required.

### Sandbox or local demonstration

Identify the synthetic/local target. Never imply that production, company knowledge, canon, or another live system changed when only a sandbox or local artifact was modified.

### Cross-system work

Trace each material mutation against its actual owning system. Do not treat a successful update in one system as proof that another system was synchronized unless that second state was verified.

## Skill drift

If real use exposes stale terminology, source assumptions, authorization logic, verification behavior, or trace-containment guidance:

- flag the exact mismatch in the maintained skill/governance surface when such maintenance is authorized and available;
- tell the user what needs maintenance and why;
- do not silently modify this skill without explicit authorization;
- after authorization, update, validate, test, and repackage the complete skill;
- verify the corrected behavior against the case that exposed the drift.

## Style

Be factual, concise, forensic, and easy to scan. Prefer concrete state-changing verbs and direct verification evidence. Use visual anchors when they improve readability. The purpose is accountability and continuity, not ceremony.
