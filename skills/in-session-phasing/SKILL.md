---
name: in-session-phasing
description: "Divide a substantial task or process into visible, bounded phases while the current conversation is actively proceeding, and align work with other concurrently running sessions or agents that share a task, owner, or artifact. Use when the user asks to \"work in phases,\" \"phase this,\" use \"in-session phasing,\" keep updating the chat while working, show what is being interpreted before continuing, or otherwise make a multi-step task observable and supervisable as it unfolds; also when parallel work on the same target could collide. Keep phases concise, execute real work inside each phase, report meaningful progress between phases, honor task-specific notification preferences, and continue without unnecessary approval prompts unless the user pauses, redirects, or a genuine decision gate is reached."
version: "1.1.2"
source: "Drive CORE — in-session-phasing"
generated: "2026-11-17"
---

Generated from Drive CORE on 2026-11-17. Read-only mirror; edits here are overwritten.

# In-Session Phasing

## Bounded proactive work and visible updates (user direction, 2026-10-25)

For multi-step investigation or edits, provide brief informative updates before and between substantial tool batches: what was found or changed, what source/tool class is next, and any actual blocker. When the user requests granular short messages or says "let me lead", stay within their intended scope while continuing relevant searches and safe reversible actions. Do not freeze, flood the chat with tool narration, ask already answered questions, or equate a candidate search result with verified evidence.

Where the host supports it, use mobile-readable native UI for meaningful status and progress with semantic status colors. If displaying an agent identity or badge, resolve its owning IDENTITY.md and current session/turn semantics; do not hard-code sample identifiers or assume turn numbering resets by task. A completed phase means a real delivered/read-back result, not a decorative heading.

## Core rule

Use both relevant ordinary meanings of **phasing**, with judgment: (a) divide substantial work into observable, bounded stages inside an active conversation; and (b) adjust or align work with other concurrently running sessions, agents, or processes when they share a task, owner, or artifact. Choose the sense(s) required by the actual situation. Phasing is guidance, not a fixed ordered sequence, a universal lookup checklist, or a claim of direct access to other chat sessions.

Make the work observable enough for the user to supervise interpretation, progress, and direction while the work is happening. A phase is a bounded chunk of real work, not merely a heading.

## Cross-session phase alignment — shared-work coordination
Treat evidence or the user's notice of another active session/agent on the same task as a coordination cue. Do not assume this conversation is the sole executor or that records are frozen at the time they were first read. When the work could overlap, retrieve current state from the relevant shared owner(s) (for example an active Linear issue, Notion handoff, Drive revision, or another authorized task artifact); select only the sources that can change the decision. Compare latest state, scope, responsible actor, changes, and remaining work before any competing persistent edit. Explicitly distinguish what the source confirms from what it merely reports.

If another session has already completed or advanced the target, preserve its verified work; do not restart, overwrite, duplicate tickets, or mark completed actions undone. Synchronize by adjusting this session's phase: verify or review read-only, pick a clearly non-overlapping authorized action, or hand off concise current state through the actual shared owner. When the same file or issue is actively being edited, use supported revision/conflict guards and re-read before applying overlapping writes; if no reliable guard/ownership is available, avoid a conflicting mutation. Do not invent locks, live presence, direct conversation access, or a cross-chat messaging channel.

This is **situational coordination**, not a duty to poll all other sessions on every turn. Use it when the user references parallel work, a shared record has advanced unexpectedly, several agents may mutate the same target, or stale state would jeopardize the task. Skip it for self-contained questions, standalone creative work, or sources that do not affect the next action. Keep the original in-conversation progress phases useful and visible, and preserve user steering and task boundaries.

Example: If the user says another session is working on a specific shared issue, read its current shared status before editing it. If the task has progressed, report the newest verified changes and avoid making a second competing scope change. Do not claim to see the other session's private live transcript; use shared changes and user testimony. If the user asks for a cross-session synchronization update, show the actual shared-state evidence and the adjusted current phase.

## Preserve interaction; reduce coordination friction

The user's confirmed preference (November 12, 2026) is that many distinct agent interactions are enjoyable and stimulating. Apply phasing to concrete shared-work dependencies, conflicting edits, lost context and repeated low-tier approvals, not to agent count as a proxy for human overload. Preserve distinct agent identities, session histories and meaningful conversations; do not recommend fewer agents, merged identities or fewer interactions merely to reduce presumed social burden.

Keep coordination work agent-owned within actual tools and authorization. A request for less administrative friction is not a request for less conversation. When the user identifies actual fatigue, UI load, time pressure or another specific burden, address that dimension and honor STOP; this preference is not a claim of unlimited capacity. It creates no background monitoring, new permissions or evidence of another session's adoption.

Authority: the user's confirmed preference and a bounded proposal, explicitly authorized for implementation on November 12, 2026.

Regression checks: enjoyable parallel chats do not trigger downsizing or polling; repeated approval complaints reduce unnecessary gates rather than interaction; real competing edits still require current-source reconciliation; an explicit overload report or STOP overrides continuing activity at its actual scope.

## Local and concurrent completion
A phase is complete only when its bounded work is done and checked. A parallel task is aligned when this session has reconciled the current shared state and avoids duplicate/conflicting action; alignment does not certify the other session's final result. Continue feasible authorized non-overlapping work rather than freezing for invented approval. Stop when the user stops, a real access/ownership conflict blocks progress, or the actual requested result is complete.

## Notification preference precedence

Apply the user's current task-specific notification rule to the opening, intermediate checkpoints and completion report. For an explicitly quiet scheduled check, do the authorized work and save its required receipt without routine chat announcements; notify only at that task's stated threshold. For interactive work where progress is expected, retain concise updates at meaningful phase boundaries and material changes. A quiet-monitoring instruction is not a pause, permission expansion, or reason to suppress a required decision or urgent blocker. Do not replace an explicit report-every-run experiment with quiet mode. No rule here requires narration before every tool call.

Regression checks: quiet unchanged pulse produces its required record but no routine chat; meaningful threshold finding produces the required report; interactive multi-step work retains useful updates; explicit report-every-run is honored; STOP still halts the affected work.

## Start the task

Before substantial execution, surface a short first-phase receipt that answers:

- What is the current goal?
- What scope is being handled now?
- What is the first meaningful chunk of work?

Keep this brief. Do not turn the opening receipt into a planning essay.

Example:

```text
### Phase 1 — Map the source material
Goal: identify the current records and how they relate.
I’m reading the authoritative sources first, then I’ll map the repeated items before changing anything.
```

## Choose natural phase boundaries

Break the task according to the work itself. Prefer meaningful boundaries such as:

1. interpret or map the problem;
2. retrieve or inspect evidence;
3. analyze, reconcile, or design;
4. execute edits, builds, or actions;
5. verify the result;
6. hand off or summarize only when needed.

Do not force every task into the same sequence. Use as many phases as the task naturally needs.

A phase should be large enough to accomplish something real and small enough that the user can redirect before too much work accumulates.

## Work visibly

For each phase:

1. Announce the phase and its immediate objective before a meaningful batch of work.
2. Perform the work rather than narrating hypothetical future work.
3. After the batch, give a compact checkpoint containing the material result, discovery, change, or blocker.
4. State the next phase when that helps supervision.
5. Continue into the next phase unless the user has asked to pause or a real decision gate requires input.

Do not disappear through a long sequence of tool calls when the task has been explicitly phased. Surface progress between meaningful batches.

Do not flood the chat with micro-updates for every click, query, or tool call. Report at the level of meaningful work units.

## Preserve user supervision

Treat new user messages during the task as active steering.

- **Pause / stop / hold**: stop before beginning another substantive batch. State the current position concisely if useful.
- **Continue**: resume from the last incomplete or next planned phase. Do not restart the task.
- **Redirect**: revise the current phase around the new instruction and continue from the preserved work already completed.
- **Correction**: adopt the corrected interpretation immediately. Treat discarded one-off assistant inferences as discarded; do not keep repeating them as contrastive caveats.
- **Decision gate**: ask only the smallest question that materially changes the next action.

The user does not need to approve every phase. Phase boundaries provide visibility, not mandatory stop signs.

## Keep interpretation observable

When the task is especially prone to scope errors, make the first phase expose the operative interpretation before doing expensive or consequential work.

Prefer:

```text
### Phase 1 — Interpret
I’m treating the goal as [concise interpretation]. I’m starting with [bounded scope].
```

Then proceed immediately when the interpretation is sufficiently clear.

If the user corrects the interpretation, update the active phase and continue. Do not defend or preserve the discarded interpretation.

## Checkpoint style

A checkpoint should normally answer only what changed since the prior phase.

Useful patterns:

```text
### Phase 2 — Map the records
✓ Mapped the current records and found two repeated entries.
Next: reconcile which one controls before editing.
```

or:

```text
### Phase 3 — Reconcile
The newer source controls. I’m applying that state to the affected records now.
```

Use prose when that is clearer. The labels are a supervision aid, not a rigid template.

## Finish cleanly

At completion, give the actual deliverable or result first. Add only the final status needed to make completion obvious.

For long tasks, a compact closing receipt may include:

- what was completed;
- what remains unresolved, if anything;
- where the artifact or changed state lives;
- the next genuine dependency, if one exists.

Do not manufacture a new phase merely to summarize completed work.

## Quality checks

Before advancing from a phase, quickly verify:

- Did this phase accomplish a real unit of work?
- Can the user tell what I interpreted and what changed?
- Am I continuing rather than waiting for unnecessary approval?
- Did I preserve corrections and redirections?
- Is the next phase still aligned with the user’s actual goal?

If yes, continue.


VERSION: 1.1.2 (2026-11-15 AST). Notification-preference precedence reconciled; prior edition retained below as history.
Historical VERSION: 1.1.1 (2026-11-12 AST). Baseline through 2026-11-06 existed without an explicit version footer.
CHANGELOG
- 1.1.2 | 2026-11-15 AST | Authorized maintainer, for the user. Reconciled phase notices with explicit task-specific notification rules, retaining interactive progress, report-every-run exceptions, STOP and all unrelated behavior. Source-only; backend and runtime unchanged.
- 1.1.1 | 2026-11-12 AST | Authorized maintainer, for the user. Added the authorized distinction between enjoyable agent-interaction volume and avoidable coordination friction. Preserved staged work, shared-source synchronization, distinct identities, STOP, permissions and non-monitoring boundaries. Source update only; backend publication and client adoption are separate checks.

- 1.1.0 — 2026-11-07 AST — Authorized maintainer, for the user. Expanded core functional contract to recognize both staged execution and synchronizing concurrent work through verified shared sources, with bounded collision prevention, revision checking, preserved user supervision, non-polling triggers, and separate live-session visibility limits. Based on the user's correction and an observed concurrent-session regression. Changed CORE source first; provider-plugin propagation and installed-runtime validation remain distinct.
