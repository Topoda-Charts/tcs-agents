---
name: work-preparing
description: "Prepare meaningful work before execution by clarifying the intended result, constraints, controlling context, dependencies, likely failure modes, and clean handoff. Use when a task, project, decision, coding effort, research effort, creative workflow, or operational thread is starting or being reshaped and the user needs PRE work rather than execution or post-review. Also use when the user asks what should be established before another AI Agent, tool, or person begins. Shared across workspace-account seats: do not assume a particular persona or seat is the invoker."
version: "2026-10-04"
source: "Drive CORE — work-preparing"
generated: "2026-10-18"
---

Generated from Drive CORE on 2026-10-18. Read-only mirror; edits here are overwritten.

# Work Preparing

 **Internal package version:** `2026-09-17T23:34:40-04:00` 

Prepare enough to make execution clean without turning preparation into bureaucracy.

## Shared seat orientation

Treat this Skill as a portable workspace-account procedure shared across seats.

- Do not assume a particular persona or seat is the invoker.
- Resolve the active seat/persona only when identity, authorship, access, permissions, role, or attribution materially affects PRE work.
- If those axes do not matter, remain identity-neutral.
- When routing work to another AI system or human, use the current maintained role/identity context rather than a hard-coded default counterpart.
- Preserve the user's authority, settled decisions, project boundaries, and intended meaning when they materially control preparation.

## Method

1. Identify the actual intended result.
2. Retrieve or surface only the controlling context needed to start correctly.
3. Clarify material constraints, dependencies, assumptions, and success conditions.
4. Pressure-test the plan for likely failure modes or expensive misunderstandings.
5. Resolve what can be resolved now; surface only material ambiguity that blocks useful execution.
6. Produce a clean handoff to the executor: objective, relevant context, boundaries, expected output, and next executable action.

## Behavior

- Treat this as **PRE**, not as a reason to delay work indefinitely.
- Prefer a minimum sufficient launch brief over exhaustive planning.
- Do not invent schedules, time blocks, approval gates, meetings, checklists, or artifacts unless they are genuinely needed or explicitly requested.
- Route by **work state**, not clock time. A task can enter PRE at any hour and can return to PRE later if new information changes the shape of the work.
- If the work is already sufficiently specified, say so and hand it forward instead of re-planning it.
- When the user already has a settled decision, recover and apply it rather than reopening the decision.
- Do not ask the user to reconstruct context that the active AI can reasonably retrieve from the current conversation or authorized sources.
- When another executor will act next, name that executor only when the current role/identity is actually established. Otherwise describe the required execution role rather than inventing a persona assignment.

## Handoff pattern

Keep the handoff lightweight:

**Goal:** what must become true
**Context:** only what the executor needs
**Constraints:** hard boundaries or settled decisions
**Watch for:** material failure modes
**Next action:** the first useful execution step

Do not force this format when a conversational handoff is clearer.

## Skill drift

If use of this Skill exposes stale persona, seat, access, role, source, or workflow assumptions:

- 🚩 flag the exact drift in the maintained TCS Notion Skill-maintenance surface;
- 🗣️ tell the user what needs maintenance and why;
- ⏸️ do not silently rewrite the installed Skill without authorization;
- 🔧 after authorization, update, validate, test, and repackage the complete Skill;
- ✅ verify the revised behavior against the scenario that exposed the drift.
