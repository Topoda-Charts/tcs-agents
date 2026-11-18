---
name: wrapping-up-turn
description: "Provide an accurate, visually useful final checkpoint for the current turn and stop expanding the task. Use when the user asks to stop and calibrate, show what the agent has been doing before stopping, summarize its current thinking and pause, or wrap up only this response. A bare STOP means stop immediately; session-ending and clock-out requests belong to their own procedures."
version: "0.1.0"
source: "Drive CORE — wrapping-up-turn"
generated: "2026-11-17"
---

Generated from Drive CORE on 2026-11-17. Read-only mirror; edits here are overwritten.

CORE — wrapping-up-turn
Version: 0.1.0 | 2026-11-13 AST
Authority: the workspace owner, TCS. Provider-neutral source for a focused turn-level pause and calibration capability. This is separate from session ending, clocking out, and continuity packaging.

PURPOSE
When the user asks the agent to stop, calibrate, synthesize its current thinking, show what it has been doing, or wrap up only this response, provide an accurate, visually useful final checkpoint and stop expanding the task. Preserve the user's corrections and current intent. Do not convert a pause into session close, a new workstream, an audit, or a status performance.

TRIGGERS AND EXCLUSIONS
Trigger on: 'stop and calibrate', 'show me what you're up to before stopping', 'wrap up this turn', 'summarize your thinking so far and pause', or equivalent user-directed interruption with a request for a final state display.
A bare STOP with no other request means stop immediately, without extra tools or content beyond minimal acknowledgement. 'End session.' or 'Clocking Out' belongs to the separate session-close procedures and their actual consent gates. An ordinary task finishing naturally does not require this Skill.

INPUT / OUTPUT
Input: current exchange, the last valid user instruction, corrections, actual tool outcomes and current known work state. Fetch only a small missing fact if necessary for a consequential closing claim and explicitly allowed within the last request.
Output: a compact, truthful turn-level state snapshot; an optional user-requested concept visualization with proposal/canon status visible; relevant actual artifact links; and no new demand for the user to repeat established context.

PROCEDURE
1. Freeze the expanded work plan. Preserve the user's latest directive, qualifiers and actual scope. Stop unrelated research, tool calls, brainstorming, and new operations.
2. Extract the smallest useful synthesis: What the user established, what the agent has independently proposed, what has actually been done or verified, and what is not settled.
3. If the user explicitly authorized a final narrow action in the same turn (for example, an existing plugin Skill update), complete only that action with normal source ownership, collision control and verification. Do not use the stop cue as either a false prohibition or broad permission for extra work.
4. Present the current state in a mobile-readable form. Use color, icons, tiers or spatial layout when the user requests a visual; label all invented palettes and definitions as placeholders. Preserve substantive accessibility in text and avoid UI-only information.
5. Give a precise receipt distinguishing draft, attempted, saved, published, installed, behavior-tested and accepted. State real blockers without inventing approvals or background work. Provide one clear resume point only when helpful.
6. End this assistant turn. No forced follow-up question, artificial engagement hook, automated scheduling, new ticket, unsolicited persistence, or session-packaging consent prompt.

COMPOSITION / OWNERSHIP
Fits in the existing TCS agent plugin alongside in-session-phasing, auditable-actions-tracing-and-logging and updating-scratchpad. Read the parent plugin map first when available; call a sibling only when needed. Session Continuity still owns ending-session and clocking-out. Linear owns actionable work when a shared source/plugin edit is explicitly authorized; do not log read-only turn wrap-ups by default.

REGRESSION SCENARIOS
A. 'Stop.' alone -> no new reads, writes or expanded summary.
B. 'Stop and calibrate; show the nine-tier proposed color palette' -> source-faithful nine labels, explicit proposal status, visual color legend, no canon promotion or new tier assignments.
C. 'Wrap up this turn after creating wrapping-up-turn inside the existing plugin' -> only named existing plugin, check current release and collision claim, verify result, then stop, no broad skill restructuring.
D. 'End session.' -> defer to session-ending consent workflow, no duplicate/hidden packaging.
E. Mid-work user correction: replace wrong proposition before final synthesis, don't defend prior framing.
F. Proposed work not executed -> report as proposed or queued, never as saved/published.

CHANGELOG
0.1.0 — 2026-11-13 AST — Initial focused turn-level stop/calibration/visibility contract, derived from the user's direct instruction. Authored by an authorized AI maintainer for the user. Provider plugin publication and live adoption must be reported independently.
