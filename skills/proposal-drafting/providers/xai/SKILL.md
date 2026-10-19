---
name: Proposal drafting
description: >-
  Use when formalizing a sufficiently developed human idea into a decision-ready proposal — retrieve current state first; draft only the real delta.
  Drive hub owns the canonical CORE; this copy is versioned 2026-10-16
  from CORE — proposal-drafting.
---

Adapter of Drive CORE — proposal-drafting (version 2026-10-04). Read-only mirror.
# Proposal drafting

**Source:** Drive CORE — proposal-drafting (private Drive hub). Local copy dated 2026-10-16. Prefer the Drive CORE on conflict; refresh this copy when the hub updates.

Turn human-originated ideas into grounded proposals without replacing the user's intent with generic AI planning.

## Lifecycle (model, not ceremony)

context/calibration → development → **proposal drafting** → implementation planning → execution → verification

Skip proposal drafting when the change is already settled and downstream work is authorized.

A proposal answers: **What change are we proposing relative to what already exists?** Not: exact implementation of every part.

## Core rule

**Retrieve before inventing.** If sources show the supposed proposal is already approved, active, implemented, rejected, or superseded, recover current state and draft only the genuine new delta.

## Seat orientation

Portable across Grok Bot seats. Do not assume a particular persona is the invoker; resolve seat/persona only when identity, authorship, connector access, permissions, source visibility, or attribution materially affects the task. Use only sources and tools actually available to this seat — do not imply another seat's files, connectors, or prior tool state are available unless independently established. Otherwise stay identity-neutral. Preserve the human originator's authorship: AI drafting, editing, retrieval, challenge, or organization does not transfer proposal ownership.

## Workflow

1. **Capture the intended change.** Accept incomplete, conversational, associative, contradictory, or messy input; do not require pre-structuring. Preserve meaningful uncertainty and alternatives.
2. **Recover relevant context.** Current conversation first; then the smallest sufficient context from owning sources available to this seat. Choose sources by what they own, not convenience. If a controlling source exists but is inaccessible, preserve that access gap rather than silently substituting a lower-authority source. Do not ask the user to restate recoverable information.
3. **Classify what already exists.** Separate current facts from the proposed change: established, active, partial, unresolved, rejected/superseded, historical, or genuinely new. If controlling sources conflict, surface the conflict — do not blend into fictional consensus.
4. **Decide whether a proposal is needed.** Use it for a real change, direction, design choice, policy, workflow, or unresolved delta. If already settled and downstream work is authorized, skip. If too underdeveloped to state coherently, return it to development rather than fabricating certainty.
5. **Find the proposal delta.** What would actually change if adopted. Never present existing work as a novel recommendation; keep current vs proposed state explicit.
6. **Draft.** Smallest structure that makes it decision-ready, adaptable order: **Title** · **Proposal** (direct language) · **Current state** (only what explains the delta) · **Rationale** · **Scope / boundaries** (when needed) · **Dependencies / consequences** (material, evidenced) · **Open decisions** · **Next transition** (when useful). Omit empty sections. No boilerplate risk registers, timelines, approval gates, milestones, success metrics, or implementation plans unless explicitly requested or required by the governing workflow.
7. **Preserve provenance and status.** Human stays originator. Distinguish proposed, accepted/approved, active, implemented, rejected, superseded. Never silently promote a draft into approval, commitment, implementation, policy, canon, or task status. Cite/link supporting sources when relying on retrieved evidence.
8. **Hand forward cleanly.** When settled, treat drafting as complete and hand into planning or execution. Reopen only on new evidence, real contradiction, or the user's changed intent.

## Boundary with implementation planning

May be implementation-aware: affected systems/surfaces, feasibility constraints, key dependencies, architectural consequences, implementation-sensitive tradeoffs. Do not ordinarily expand into file-by-file changes, execution sequencing, migration procedures, test matrices, rollout instructions, task decomposition, or coding steps — those belong downstream (**Implementation planning**).

## Exit states

- **Proposed** — articulated, ready for decision.
- **Direction established** — settled enough to move downstream.
- **Needs more development** — material conceptual/design questions remain.
- **No proposal needed** — already established; proceed downstream.

Never imply acceptance merely because the draft is good.

## Behavior rules

- Professionalize the artifact, not the thinking; keep the user's meaning, not generic corporate language.
- Do not use proposal drafting as a substitute for already-authorized work.
- Do not manufacture novelty; existing work goes in current state.
- Do not expand a narrow idea into a broad transformation program unless asked.
- Once a direction is settled, stop treating it as perpetually hypothetical.
- Use **Neighboring concept disambiguating** when terminology is genuinely ambiguous; then keep moving.
- Concise direct prose; preserve domain terminology from governing sources.

## Example

**Input:** "I keep wishing our AI Agents would look at what already exists before they start suggesting we create it. Maybe proposals should gather the old chats and Notion and the repo first?"

**Poor:** "Proposal: Create a system for AI Agents to use Notion and GitHub before starting work."

**Better:** Retrieve existing source-routing and agent-operation rules first. If retrieval already exists, describe it as current state; draft only the unresolved change; keep implementation steps downstream unless explicitly requested.

## Skill drift

If use exposes a stale source assumption, seat/access rule, actor label, term, lifecycle boundary, or workflow instruction: flag the exact mismatch in the maintained Skill-maintenance surface when authorized; tell the user what needs maintenance and why; do not silently rewrite without explicit authorization; after authorization update, validate, and test the complete Skill; verify against the case that exposed the drift. Drive CORE remains canonical.
