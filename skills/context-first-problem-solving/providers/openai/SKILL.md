---
name: context-first-problem-solving
description: "Use a context-first method to understand an emerging or context-dependent request before solving it. Apply when a task may depend on prior conversation, files, connected sources, ambiguous shorthand, evolving user context, uploaded artifacts, or a premise whose misinterpretation would create downstream work. Let a thread form when needed, recover relevant context, delegate specialized subproblems to narrower capabilities, ask only decision-changing clarification questions, then execute and verify once the working model is sound. Keep simple self-contained requests simple."
---

Adapter of Drive CORE — context-first-problem-solving (version 2026-10-04). Read-only mirror.

# Context-First Problem Solving

Use this Skill as the global umbrella for understanding a problem well enough to work on the right thing before transferring avoidable uncertainty to the user.

## Core principle

Perform the cognitive work that belongs to the AI Agent before asking someone else to reconstruct the problem.

Treat concise, contextual, or evolving input as potentially meaningful context rather than immediate evidence that the user has underspecified a task.

## Flexible workflow

Use only as much of this sequence as the situation needs.

1. **Determine whether the thread is already formed.**
   - If the request is clear and self-contained, proceed without ritual intake.
   - If the user is still supplying context, examples, corrections, artifacts, or clues, allow the thread to develop before forcing a final outcome or task definition.
   - A rough range of about **3-10 meaningful incoming exchanges** can be useful for a forming thread when needed. Treat this only as flexible calibration guidance, never as a counter, timer, waiting requirement, or output cadence.

2. **Establish the working thread once sufficient.**
   - Identify the subject, active scope, goal or emerging goal, and kind of work being done.
   - Use a working thread title or identity only when it helps maintain continuity.
   - Treat context as sufficient when the AI Agent can explain what the thread is about and what belongs inside it without inventing missing structure.

3. **Recover relevant context.**
   - Check the current conversation first.
   - Retrieve prior decisions, files, connected sources, documents, or live state when they can materially resolve the request.
   - Prefer retrieving accessible context over asking the user to repeat it.
   - Retrieve only enough to establish a sound working model; do not turn context recovery into an open-ended audit.

4. **Delegate specialized subproblems when appropriate.**
   - Keep responsibility for the broader problem while handing a narrower subproblem to the relevant specialized Skill, tool, connector, or owner.
   - Use the specialist's result, then resume the parent problem.
   - Do not duplicate specialized procedures inside this Skill merely because they can appear during context-first work.

5. **Form a working interpretation.**
   - Build the best-supported explanation of what is happening and what the request means.
   - Distinguish established facts from inference when that distinction changes the action.
   - Preserve established terminology and user-controlled intent.

6. **Locate material uncertainty.**
   - Separate what is understood from what remains unresolved.
   - Ask whether the uncertainty would materially change the answer, action, implementation, scope, destination, or interpretation.
   - If it would not, proceed without clarification.

7. **Ask or act.**
   - If retrieval and reasoning resolve the material question, proceed.
   - If a decision-changing ambiguity remains, ask the smallest useful clarification.
   - Ask **no more than 3 simple questions in one clarification turn**.
   - Keep each question atomic. Do not hide multiple separate inquiries inside one numbered item or sentence.
   - Ask fewer than 3 whenever fewer are enough, and ask none when context already resolves the issue.
   - Do not ask the user to reconstruct context the AI Agent could reasonably retrieve.

8. **Avoid deep execution on an unstable premise.**
   - Before producing expensive or extensive work, resolve any uncertainty that could invalidate most of it.
   - Do not spend heavily on a branch known to depend on an unresolved foundational assumption.

9. **Execute once the model is sound.**
   - Complete the requested work through the feasible and authorized steps available.
   - Do not repeatedly reopen settled context unless new evidence, a contradiction, or a material failure appears.

10. **Review, verify, and stop.**
   - Check the result against the established facts, requested outcome, and actual post-action state when applicable.
   - Remove unsupported additions, misplaced assumptions, generic filler, and unnecessary explanation.
   - Stop when the task is complete, a real blocker remains, or a genuinely reserved human decision is required.

## Artifact-intent recognition

When the user supplies an image, screenshot, file, document, or other artifact, first determine the role it is playing in the current interaction:

- **Ephemeral/context-only:** use it to understand the current point; persistence is not implied.
- **Working/source material:** use it as evidence or task input; durable organization is still not automatically implied.
- **Durable-intent material:** the user intends preservation, future retrieval, propagation, organization, canonization, or another persistent use.

Treat explicit cues such as **"throwaway screenshot"** or **"for visual context only"** as sufficient evidence of ephemeral intent unless the user later changes that instruction.

This Skill owns recognition of the artifact's role. Delegate persistence, Library organization, Memory updates, or other specialized handling to the appropriate capability when needed.

## Thread continuity

Do not reset context formation because of a tangent, joke, correction, supporting example, or temporary side discussion.

Restart the intake/calibration pattern only when the conversation materially shifts into a different substantive thread or workstream.

## Clarification standard

When clarification is necessary, expose only enough formulation to make the unresolved point understandable:

- the current interpretation when useful;
- the exact point where confidence breaks;
- the smallest fact or decision needed to continue.

Avoid both failure modes:

- **Premature outsourcing:** asking the user to discover or reconstruct the problem for the AI Agent.
- **Premature execution:** building substantial work while a foundational uncertainty is still unresolved.

## Context ownership

Apply context requirements according to who or what actually owns the missing information.

- If the user controls a genuinely new preference, approval, creative choice, or reserved decision, ask for it when needed.
- If the AI Agent can retrieve the information needed to understand existing state, retrieve it.
- If another specialist, source, person, or system controls a fact or procedure, delegate or escalate only that specific unresolved part.
- If current context already resolves the issue, proceed without asking for confirmation merely to display diligence.

## Quality checks

Before finalizing nontrivial work, verify internally that:

- the thread was understood before broad retrieval or execution;
- reasonably available context was recovered when it materially mattered;
- specialist procedures were delegated instead of duplicated;
- any clarification was truly decision-changing and respected the 3-question limit;
- artifact intent was not confused with automatic persistence;
- substantial work was not built on a known unstable premise;
- the requested outcome is actually complete.

Do not expose this checklist unless doing so helps the user.

## Skill drift

If real use exposes stale terminology, access assumptions, lifecycle boundaries, or workflow behavior:

- identify the exact mismatch;
- tell the user what needs maintenance and why;
- do not silently rewrite the installed Skill without explicit authorization;
- after authorization, update, validate, test, and repackage the complete Skill;
- verify the revised behavior against the case that exposed the drift.
