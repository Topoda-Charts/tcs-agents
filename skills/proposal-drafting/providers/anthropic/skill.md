---
name: proposal-drafting
description: "Turn human-originated, messy, fragmented, or developed ideas into grounded decision-ready proposals that distinguish current reality from the proposed change. Use when the user wants to draft, formalize, capture, consolidate, or structure a proposal, change proposal, design-direction proposal, decision proposal, or similar artifact before a direction is settled enough for detailed implementation planning. Recover relevant current context before proposing, preserve authorship and status, and do not manufacture a proposal stage for work already authorized for execution."
---

Adapter of Drive CORE — proposal-drafting (version 2026-10-04). Read-only mirror.

# Proposal Drafting

Turn human-originated ideas into grounded proposals without replacing the user's intent with generic AI planning.

## Core role

Use proposal drafting to formalize a sufficiently developed idea into a decision-ready proposed change.

The normal conceptual flow is:

**context and calibration -> development -> proposal drafting -> implementation planning -> execution -> verification**

Treat this as a useful lifecycle model, not mandatory ceremony. Skip proposal drafting when the intended change is already sufficiently established and the user has authorized downstream planning or execution.

A proposal answers:

**What change are we proposing to pursue, relative to what already exists?**

It does not normally answer:

**Exactly how will every part of that change be implemented?**

## Core rule

Retrieve before inventing.

If relevant sources already establish that the supposed proposal is approved, active, implemented, rejected, superseded, or otherwise resolved, do not draft a proposal pretending that work does not exist. Recover the current state and draft only the genuinely new delta, if one remains.

## Shared seat orientation

Treat this Skill as a portable workspace-account procedure shared across seats.

- Do not assume a particular persona or seat is the invoker.
- Resolve the active seat or persona only when identity, authorship, connector access, permissions, source visibility, or attribution materially affects the task.
- Use only sources and tools actually available to the invoking seat. Do not imply another seat's Library, connectors, files, or prior tool state are available unless that access is independently established.
- If identity or seat does not matter to the proposal, remain identity-neutral.
- Preserve the human originator's authorship. AI drafting, editing, retrieval, challenge, or organization does not transfer proposal ownership.

## Workflow

1. **Capture the intended change.**
   - Identify the user's actual idea, desired change, tension, question, or direction from the material they supplied.
   - Accept incomplete, conversational, associative, contradictory, or messy input. Do not require the user to pre-structure it.
   - Preserve meaningful uncertainty and alternatives rather than forcing premature certainty.

2. **Recover relevant context.**
   - Start with the current conversation and material already supplied.
   - When the proposal depends on prior work or organizational reality, retrieve the smallest sufficient context from sources available to the invoking seat.
   - Choose sources by what they own, not by convenience.
   - If a controlling source exists but is inaccessible, preserve that access gap rather than silently substituting a lower-authority source.
   - Do not ask the user to restate information that can be recovered from available context.

3. **Classify what already exists.**
   - Separate current facts from the proposed change.
   - Determine whether relevant material is established current state, active work, partially implemented, unresolved, rejected or superseded, historical context, or genuinely new.
   - If current controlling sources conflict, surface the conflict rather than blending them into a fictional consensus.

4. **Decide whether a proposal is actually needed.**
   - Use proposal drafting when there is a real change, direction, design choice, policy, workflow, or unresolved delta that needs to be formalized for consideration or adoption.
   - If the intended direction is already sufficiently settled and the user has authorized downstream work, do not create a redundant proposal phase.
   - If the idea is still too underdeveloped to state a coherent proposed change, return it to development rather than fabricating certainty.

5. **Find the proposal delta.**
   - Express what would actually change if the proposal were adopted.
   - Do not present an existing task, decision, feature, or implementation as a novel recommendation.
   - Keep the distinction between current reality and proposed future state explicit.

6. **Draft the proposal.**
   - Use the smallest structure that makes the proposed change understandable and decision-ready.
   - Prefer this adaptable order when useful:
     - **Title**
     - **Proposal** - the actual proposed change in direct language.
     - **Current state** - only the context needed to understand the delta.
     - **Rationale** - why the change is being proposed or what problem it addresses.
     - **Scope / boundaries** - only when needed to prevent ambiguity or scope creep.
     - **Dependencies / consequences** - only material ones supported by evidence.
     - **Open decisions** - unresolved choices that genuinely require a decision.
     - **Next transition** - only when useful: what must happen for the proposal to move into planning or execution.
   - Omit empty or unnecessary sections.
   - Do not add boilerplate risk registers, timelines, approval gates, milestones, success metrics, or implementation plans unless the user explicitly requests a combined artifact or the governing workflow specifically requires one.

7. **Preserve provenance and status.**
   - Keep the human as the proposal originator when the idea came from the user.
   - Distinguish proposed, accepted or approved, active, implemented, rejected, and superseded states.
   - Do not silently promote a drafted proposal into approval, commitment, implementation, policy, canon, or task status.
   - Cite or link supporting sources when the environment supports citations and the proposal relies on retrieved evidence.

8. **Hand the proposal forward cleanly.**
   - If the direction becomes sufficiently settled, treat proposal drafting as complete and hand the accepted direction into downstream planning or execution.
   - Do not keep reopening a settled proposal merely because later work is now more concrete.
   - Reopen the proposal only when new evidence, a real contradiction, or the user's changed intent materially affects the underlying direction.

## Boundary with implementation planning

Proposal drafting may be implementation-aware. Include enough technical or operational context to make the proposal credible and decision-ready, such as:

- affected systems or surfaces;
- material feasibility constraints;
- important dependencies;
- architectural consequences;
- meaningful implementation-sensitive tradeoffs.

Do not ordinarily expand the proposal into detailed implementation planning, such as:

- exact file-by-file changes;
- detailed execution sequencing;
- migration procedures;
- complete test matrices;
- rollout instructions;
- implementation task decomposition;
- concrete coding steps.

Those belong downstream once the intended change is sufficiently settled.

## Proposal exit states

Leave the work in the state that is actually supported:

- **Proposed** - articulated and ready for consideration or decision.
- **Direction established** - accepted or otherwise settled enough to move downstream.
- **Needs more development** - important conceptual or design questions remain unresolved.
- **No proposal needed** - the intended change is already established; proceed downstream.

Do not imply that a proposal was accepted merely because the AI drafted it well.

## Behavior rules

- Professionalize the artifact, not the thinking. Preserve the user's intended meaning instead of sanitizing it into generic corporate language.
- Do not use proposal drafting as a substitute for doing already-authorized work.
- Do not manufacture novelty. Existing work belongs in current state, not in the proposed-change section.
- Do not expand a narrow human idea into a broad transformation program unless the user asked for that expansion.
- Preserve meaningful implementation awareness without swallowing downstream implementation planning.
- Once a direction is settled, stop treating it as perpetually hypothetical.
- Use neighboring-concept disambiguation when terminology is genuinely ambiguous and that capability is available; keep the proposal moving once the intended concept is clear.
- Prefer concise direct prose. Preserve domain terminology from governing sources.

## Example

**Human input:** "I keep wishing our AI Agents would look at what already exists before they start suggesting we create it. Maybe proposals should gather the old chats and Notion and the repo first?"

**Poor draft:** "Proposal: Create a system for AI Agents to use Notion and GitHub before starting work."

**Better process:** Retrieve the existing source-routing and AI Agent-operation rules first. If source retrieval already exists, describe it as current state. Draft only the genuinely unresolved change. Keep detailed implementation steps downstream unless the user explicitly requests them as part of the same artifact.

## Skill drift

If real use exposes a stale source assumption, seat or access rule, actor label, terminology choice, lifecycle boundary, or workflow instruction:

- flag the exact mismatch in the maintained Skill-maintenance or governance surface when such maintenance is authorized and available;
- tell the user which instruction needs maintenance and why;
- do not silently rewrite the installed Skill without explicit authorization;
- after authorization, update, validate, test, and repackage the complete Skill;
- verify the revised behavior against the case that exposed the drift.
