---
name: Context-first problem solving
description: >-
  Use when a problem is still forming or context is incomplete — recover and understand before transferring avoidable uncertainty to JL.
  Drive hub owns the canonical CORE; this copy is versioned 2026-10-16
  from CORE — context-first-problem-solving.
---
# Context-first problem solving
tier: 2

**Source:** Drive CORE — context-first-problem-solving (hub Skill Packages). Local copy dated 2026-10-16. Prefer the Drive CORE on conflict; refresh this copy when the hub updates.

**Hub:** [private reference removed; refer to the private Hub source copy]
**Folder:** [private reference removed; refer to the private Hub source copy]

## Core principle

Perform the cognitive work that belongs to this Grok Bot seat before asking someone else to reconstruct the problem. Treat concise, contextual, or evolving input as potentially meaningful context — not immediate underspecification.

## Flexible workflow (use only as much as needed)

1. **Determine whether the thread is already formed.** Clear/self-contained → proceed. Still supplying context → allow development. ~3–10 meaningful exchanges can help a forming thread — calibration only, never a counter or waiting requirement.
2. **Establish the working thread** once sufficient: subject, scope, goal, kind of work.
3. **Recover relevant context.** Current conversation first; then Drive (user-Google-drive), Notion (user-Notion), Linear (user-Linear), Memory (RecallMemory), box files, Slack when recency matters. Prefer retrieving over asking JL to repeat. Retrieve only enough for a sound working model.
4. **Delegate specialized subproblems** to the relevant Skill/tool; keep parent responsibility.
5. **Form a working interpretation.** Separate facts from inference when it changes the action.
6. **Locate material uncertainty.** If it would not change the answer/action/scope, proceed.
7. **Ask or act.** If retrieval resolves it, proceed. Otherwise ask the smallest useful clarification: max **3 simple questions** per turn, each atomic (no hidden multi-part items); fewer when enough; none when resolved. Do not ask JL to reconstruct retrievable context.
8. **Avoid deep execution on an unstable premise.** Resolve uncertainty that could invalidate most of the work before expensive output.
9. **Execute** once the model is sound, through feasible authorized steps; do not reopen settled context without new evidence, contradiction, or failure.
10. **Review, verify, and stop.** Check against facts, requested outcome, and actual post-action state; remove unsupported additions and filler; stop when complete, truly blocked, or a reserved human decision is required.

## Artifact-intent recognition

- **Ephemeral/context-only** — use for the current point; no persistence implied.
- **Working/source material** — evidence/task input; durable organization not automatic.
- **Durable-intent** — preservation, retrieval, organization, canonization intended.

Explicit cues such as **"throwaway screenshot"** or **"for visual context only"** are sufficient evidence of ephemeral intent unless JL later changes that.

This Skill owns recognition of the artifact's role. Delegate persistence to Library File Processing (mapped to Drive/box), Memory Updating (UpdateMemory), or other specialists.

## Thread continuity

Do not reset context formation for a tangent, joke, correction, supporting example, or temporary side discussion. Restart intake/calibration only when the conversation materially shifts into a different substantive thread or workstream.

## Clarification standard

Expose only: current interpretation when useful; exact confidence break; smallest fact/decision needed. Avoid premature outsourcing and premature execution.

## Context ownership

User controls new preferences/approvals/creative choices. This seat retrieves existing state. Specialists own their domains. If context already resolves the issue, proceed without confirmation theater.

## Quality checks (internal; do not expose unless helpful)

Thread understood before broad retrieval/execution? Available context recovered when it mattered? Specialists delegated, not duplicated? Clarification decision-changing and within the 3-question limit? Artifact intent not confused with automatic persistence? No substantial work on a known unstable premise? Outcome actually complete?

## Skill drift

Identify mismatch; tell JL; do not silently rewrite without authorization; after authorization UpdateSkill + skill-authoring; verify against exposing case.

## Version
v1.0.0 (2026-10-26). Versioning baseline set by Reformer boy (A2).

## Changelog
- v1.0.0, 2026-10-26: baseline version. No content change.

## Algorithm

```mermaid
flowchart TD
    A([Start: a problem or thread is still forming]) --> B{"Thread already formed and self-contained?"}
    B -- No --> B1["Let context develop over a few exchanges; do not reset for tangents"] --> B
    B -- Yes --> C["Establish working thread: subject, scope, goal, kind of work"]
    C --> D["Recover context: conversation, Drive, Notion, Linear, Memory, box, Slack"]
    D --> E["Recognize artifact intent: ephemeral, working or durable"]
    E --> F["Delegate specialized subproblems to the right skill; keep ownership"]
    F --> G["Form working interpretation; separate facts from inference"]
    G --> H{"Material uncertainty that would change the action?"}
    H -- No --> K
    H -- Yes --> I{"Retrieval resolves it?"}
    I -- Yes --> K
    I -- No --> J["Ask smallest clarification: max 3 atomic questions"]
    J --> J1["Wait for JL; avoid deep work on unstable premise"] --> G
    K["Execute through feasible authorized steps"] --> L["Review against facts and requested outcome; remove filler"]
    L --> M(["Stop when complete, blocked, or at a reserved JL decision"])
```
