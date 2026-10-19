---
name: implementation-planning
description: "Turn a sufficiently settled intended change into the smallest complete, ordered, dependency-aware, verifiable implementation plan grounded in current implementation reality and current execution state. Use when a user asks for an implementation plan, technical execution plan, coding/change plan, migration plan, system-change plan, or when substantial authorized implementation benefits from a planning pass before execution. Reconcile existing work before creating new work items, preserve settled direction, expose real blockers, and keep planning proportional rather than turning it into bureaucracy."
version: "2026-10-04"
source: "Drive CORE — implementation-planning"
generated: "2026-10-18"
---

Generated from Drive CORE on 2026-10-18. Read-only mirror; edits here are overwritten.

# Implementation Planning

Turn settled-enough direction into an execution-ready path without reopening decisions that have already been made or inventing work that already exists.

## Core role

Use implementation planning to answer:

**Given the intended result and the actual current state, what is the smallest complete path to implement and verify the remaining change?**

A useful conceptual flow is:

**context and calibration -> development -> proposal drafting when needed -> implementation planning -> execution -> verification**

Treat this as a lifecycle model, not mandatory ceremony. A formal proposal is not required when the intended direction is already sufficiently established by the user, a controlling specification, an approved decision, or another authoritative source.

## Core invariants

### Plan from reality, not from the brief alone

Before prescribing implementation, inspect the current implementation and relevant execution state when available.

- Distinguish intended design from what is actually implemented.
- Identify work that already exists, is partially implemented, is already tracked, or is already complete.
- Plan only the remaining implementation delta.
- A historical handoff, old plan, continuity packet, or proposal is context; it is not proof of current implementation or current task state.

### Tight goals, adaptable plans

Keep these stable unless authority changes them:

- intended outcome;
- material scope and exclusions;
- controlling constraints;
- acceptance conditions;
- reserved decision gates.

Let lower-level implementation details adapt when current evidence changes the efficient route. Do not freeze tool order, search order, batching, decomposition, or incidental file sequence unless that order is materially required.

### Do not re-propose settled direction

Implementation planning operationalizes a sufficiently settled change.

- Do not reopen product, design, policy, canon, naming, or architectural decisions merely because planning makes them more concrete.
- If new implementation evidence materially invalidates the settled direction, surface the exact conflict and the smallest decision that must move upstream.
- Do not silently substitute a different direction because it appears easier to implement.

### Planning is not implementation

A plan describes the implementation path; it does not establish that the change occurred.

When the user requested implementation rather than planning as the final deliverable, treat the plan as an intermediate artifact and continue into execution when the active context, authorization, and tools permit it. Do not stop at a plan merely because this Skill was invoked.

## Workflow

1. **Recover the intended result.**
   - Identify what must become true when implementation is complete.
   - Use the user's current direction and the relevant settled proposal, specification, decision, brief, issue, or acceptance conditions.
   - Preserve explicit exclusions and reserved human decisions.

2. **Determine whether planning is actually needed.**
   - Use a material plan for multi-step, cross-system, structural, migration, architectural, risky, or otherwise non-trivial implementation.
   - For a tiny, obvious, already-authorized change, keep the plan implicit or very small rather than manufacturing process overhead.
   - If the intended direction itself is materially unresolved, do not fabricate an implementation choice. Surface the unresolved decision or return the work upstream.

3. **Inspect current implementation reality.**
   - Read the actual implementation surface that owns the behavior: repository/code, configuration, schema, database state, current Skill, connected system, runtime, generated artifact, or equivalent.
   - Inspect the relevant current design/specification source when implementation must conform to one.
   - Use current evidence rather than remembered structure, filenames, old handoffs, or assumed architecture.

4. **Reconcile current execution state.**
   - When an execution tracker or task system is relevant and available, inspect existing work before inventing new work items.
   - In TCS work, Linear normally owns current representable execution state such as issues, status, ownership, blockers, dependencies, milestones, and actionable follow-up.
   - Determine whether the implementation delta is already represented by an existing issue, is partly represented, or genuinely requires new work.
   - Do not create duplicate issues merely because the plan has multiple steps.
   - Create or update execution records only when that mutation is authorized; otherwise describe the mapping in the plan.

5. **Compute the implementation delta.**
   - Compare the current state with the required state.
   - Separate already-correct behavior from work that remains.
   - Identify migrations, compatibility concerns, cleanup, propagation, or downstream effects only when the change actually requires them.

6. **Identify affected surfaces and dependencies.**
   - Name the concrete systems, modules, files, schemas, prompts, Skills, configurations, interfaces, tests, artifacts, or connected records that materially participate in the change.
   - Search for references and dependents before planning structural changes, renames, deletions, schema changes, or migrations.
   - Distinguish hard dependencies from convenient sequencing.

7. **Build the smallest executable sequence.**
   - Order work according to dependency and verification logic rather than arbitrary numbered prose.
   - Keep steps at the level an executor can act on without reverse-engineering the planner's intent.
   - Combine repetitive low-level edits into one coherent implementation step when they share the same purpose.
   - Preserve opportunities for safe parallel work when write ownership and dependencies genuinely allow it.

8. **Attach verification to meaningful implementation slices.**
   - State how the executor can establish that each material result worked.
   - Use checks that actually exercise the changed surface: focused tests, regression tests, typecheck, lint, build, schema validation, query/readback, runtime observation, render inspection, reference search, generated-artifact inspection, or acceptance-condition review as appropriate.
   - A passing check proves only what it actually tests.

9. **Classify blockers and plan-changing discoveries.**
   - **Implementation detail:** the executor can resolve it locally without changing the intended outcome.
   - **Plan-affecting discovery:** revise the implementation approach while preserving the intended outcome.
   - **Direction-breaking discovery:** implementation cannot safely proceed without changing or clarifying the underlying direction; surface the smallest required upstream decision.
   - Do not escalate ordinary implementation details into unnecessary user gates.

10. **Produce the execution-ready plan.**
    - Keep it proportional to the work.
    - Make current state, remaining delta, sequence, verification, and genuine blockers easy to scan.
    - If no implementation work remains, say so instead of manufacturing a plan.

## Source and system roles

Choose sources by what they own. When source ownership is unclear, use the available knowledge-routing capability instead of embedding a competing routing doctrine here.

For TCS work, a useful working distinction is:

- **The user's current direction / approved decision:** intended outcome, scope, priorities, reserved decisions, and sufficiency.
- **Google Drive:** durable product knowledge, design, specifications, canon, research, and creative source material.
- **Notion:** governance, approvals, decisions, source-routing context, and coordination/provenance that has independent value.
- **Linear:** current representable execution state.
- **GitHub / repository / runtime:** implementation-current code, configuration, tests, builds, generated output, and observed behavior.
- **Supabase or another live structured system:** current data/schema state when that system itself is being implemented or changed.
- **Current official external sources:** provider behavior, APIs, standards, laws, or other externally controlled implementation constraints.

Do not lower source authority because another source is easier to access.

## Boundary with proposal drafting

Proposal drafting answers:

**What change are we proposing to pursue?**

Implementation planning answers:

**Given that sufficiently settled direction, how will we implement and verify the remaining change?**

Implementation planning may discover evidence that requires an upstream decision, but it should not routinely re-argue the proposal, invent strategic alternatives, or treat accepted direction as hypothetical.

## Boundary with work preparation

Preparation establishes enough objective, context, constraints, dependencies, and success conditions to begin cleanly.

Implementation planning goes deeper only when the work needs a concrete technical or operational execution path. Do not duplicate PRE-style launch briefs when the implementation path is already obvious.

## Boundary with execution tracking

A plan may map work onto existing issues, tasks, milestones, or work packets. It is not itself the execution tracker.

- Reconcile with existing execution records before proposing new ones.
- Keep issue boundaries aligned with meaningful executable units, not every plan bullet.
- If a plan is persisted into an execution tracker, preserve meaningful revisions or execution updates rather than rewriting history so the original plan appears to have predicted the final path.
- Keep trivial tool chatter and temporary reasoning out of durable execution records.

## Boundary with execution and action tracing

Do not claim that planned work is implemented.

After execution, verification and material action tracing should describe the actual resulting state, including meaningful deviations from the plan. The plan is useful comparative evidence; it is not a substitute for post-action verification.

## Default plan format

Use the smallest subset that materially helps the executor. Visual anchors are preferred for scanability.

`` ```markdown ``
## 🛠️ Implementation Plan

### 🎯 Objective
[What must become true when implementation is complete.]

### 🔎 Current state
[Only the implementation and execution state that materially affects the plan.]

### 🔄 Remaining delta
[What still needs to change; exclude work already complete.]

### 🧱 Affected surfaces
[Concrete systems/files/modules/schemas/configuration/issues when useful.]

### 🪜 Implementation sequence
1. [Executable step and why it precedes later work.]
2. [Next coherent step.]

### ✅ Verification
[Checks tied to the material implementation slices and final acceptance.]

### 🚧 Blockers / required decisions
[Only genuine blockers or reserved decisions. Omit when none.]

### 📍 Execution mapping
[Existing issue/task mapping or genuinely new work units when relevant. Omit when unnecessary.]

### 🏁 Completion condition
[What establishes that the intended implementation is actually finished.]
`` ``` ``

Do not force every heading into every plan.

## Plan exit states

Leave planning in the state actually supported:

- **Ready to execute** - current state is sufficiently known and the remaining path is actionable.
- **Ready with adaptive details** - outcome and sequence are sound; lower-level implementation choices may adjust during execution.
- **Blocked by implementation evidence** - current implementation or dependency state cannot be inspected sufficiently to produce a trustworthy plan.
- **Needs upstream decision** - a material unresolved direction prevents safe planning.
- **No implementation delta** - the required state is already present or the requested work is already complete.

## Quality checks

Before presenting a material implementation plan, confirm:

- the intended result is settled enough to plan;
- the plan reflects current implementation reality rather than only the requested future state;
- relevant current execution state was reconciled when available;
- existing work is not being re-created as new work;
- each step contributes to the actual remaining delta;
- dependencies and sequencing are real rather than ceremonial;
- verification checks test the changed surfaces;
- user-controlled decisions remain user-controlled;
- the plan does not silently authorize execution or claim completion;
- the plan is no larger than the implementation actually requires.

## Examples

### Existing issue already owns the work

**Input:** "Plan the remaining implementation of this feature."

**Good behavior:** Inspect the current implementation and relevant execution tracker. If an existing issue already owns most of the work, plan the remaining delta against that issue and identify any missing executable unit without creating duplicate issue structure.

### Direct settled instruction without a formal proposal

**Input:** "The Skill should attempt the Memory update, then hand off only the intended Memory payload if the update fails. Plan the implementation."

**Good behavior:** Treat the user's settled behavior as the target state. Inspect the current Skill, calculate the exact instruction/metadata/test delta, and produce the implementation path without manufacturing a proposal stage.

### Implementation evidence breaks an assumption

**Input:** "Plan this migration using the existing schema."

**Good behavior:** If current schema inspection shows the assumed table or field does not exist, determine whether the plan can adapt while preserving the intended outcome. Escalate only if the missing structure changes the underlying product or architectural decision.

## Skill drift

If real use exposes stale lifecycle boundaries, source assumptions, execution-tracker behavior, planning granularity, verification guidance, or platform-specific implementation behavior:

- flag the exact mismatch in the maintained Skill or governance surface when maintenance is authorized and available;
- tell the user what needs maintenance and why;
- do not silently rewrite this Skill without explicit authorization;
- after authorization, update, validate, test, and repackage the complete Skill;
- verify the revised behavior against the case that exposed the drift.

## Style

Be concrete, compact, technically grounded, and easy to scan. Use visual anchors when they improve navigation. Prefer exact state and executable verbs over generic project-management prose. The purpose is to make implementation easier and more reliable, not to create paperwork.
