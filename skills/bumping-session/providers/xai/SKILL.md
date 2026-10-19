---
name: Bumping session
description: >-
  Use when the user returns to a conversation after a gap, asks how much time has passed, or wants to re-anchor the thread — establish a trustworthy session boundary from timestamp evidence, and resume prior work only if explicitly asked.
  Drive hub owns the canonical CORE; this copy is versioned 2026-10-16
  from CORE — bumping-session.
---

Adapter of Drive CORE — bumping-session (version 2026-10-15). Read-only mirror.
# Bumping Session

**Source:** Drive CORE — bumping-session (private Drive hub, CORE dated 2026-10-15). Local copy dated 2026-10-16. Prefer the Drive CORE on conflict; refresh this copy when the hub updates. Provider-specific adapters named in the CORE are optional; resolve real capabilities at runtime and report gaps rather than assuming them.

## Route the request

Distinguish three operations before acting:

1. **Bump only:** The user returns, asks for the time gap, or wants to re-anchor this thread. Establish the new session boundary and stop after a compact useful receipt. Do not revive old tasks.

2. **Bump and resume:** The user explicitly asks to pick up a prior unfinished task. Establish the time boundary first, then invoke `getting-dressed` or equivalent context recovery to retrieve current task state and continue the authorized work.

3. **Elapsed-time question only:** Calculate the requested difference and answer directly. Do not manufacture a broader session review or agenda.

A user can return to the same chat on another day without continuing the old *session*. Conversely, one active session can cross midnight. Do not equate a new calendar date with a new session by itself.

## Establish trustworthy temporal anchors

1. **Current moment:** Use the current, trustworthy user-local date and time from runtime context or a time tool when available. Include the time zone or UTC offset. If only a trustworthy date is available, provide a date-level anchor rather than pretending to know the exact minute.

2. **Previous moment:** Prefer the last-active date/time the user directly supplies for *this chat*. Otherwise use actual accessible timestamp metadata for the last previous interaction in this chat. Distinguish it from timestamps appearing inside messages, documents, filenames, copied transcripts, external updates, or conversation summaries; those are not proof of this chat's last activity.

3. **Temporal precision:** Compute an exact interval only when both endpoints and their time-zone interpretation are sufficiently known. If the prior timestamp is unknown, say "last activity time not available" and still anchor the current session; do not ask for a timestamp unless calculating the gap is central to the user's request.

4. **Weekday and offset:** Derive weekdays from calendar dates rather than repeating unchecked weekday labels. Respect UTC offsets and daylight-saving changes. If a weekday in the user's anchor conflicts with its date, surface the inconsistency briefly and prefer asking one targeted question only if it changes the requested elapsed interval.

5. **Calculation:** Subtract instants, not naive local clock readings. Report elapsed days, hours and minutes at the available precision; do not confuse elapsed duration with calendar-day count. Optionally use `scripts/session_gap.py` when code execution is available and exact timestamps include UTC offsets. The script never chooses the current time itself.

Never invent a last-interaction timestamp, infer it from the old messages' use of "today" or "Sunday", or turn a historical transcript's event time into the session endpoint.

## Re-enter the conversation without context bleed

- Regard earlier messages as **historical interaction context** at the moment of re-entry. Old "now", "today", "tomorrow", "this weekend", "pending", "just now", "still", availability, quotas, releases and deadlines require fresh interpretation before use.

- Preserve established facts, user-owned decisions, approved terminology, creative canon, relationships, source links and corrections as continuity. A time gap does not itself repeal them.

- Keep old task prompts and assistant plans in their original time and scope. An old "go ahead", promised follow-up, or unfinished operation is not automatically authorization to run it today.

- Classify prior state as **confirmed and enduring**, **time-sensitive and needs recheck**, **unfinished but not automatically active**, or **superseded** only when this distinction affects the current response. Do not turn a casual bump into an audit.

- Treat the user's current message as the live conversational request. Do not import the prior chat's emotional state, joke, working mode or work agenda as if they are still underway. Match the room now.

- Use Memory and prior-conversation continuity if necessary and available, not as substitutes for live timestamp evidence. Retrieve from Notion, Drive, Linear, GitHub or another owner only when the user asks to resume substantive work or when a current claim actually needs revalidation. Avoid connector sweeps for a bump-only request.

- Bumping does not write to Memory, Notion, Drive, Library or project systems. Persistence and changing source records require separate authorization or a clearly applicable pre-existing mandate.

## Continue only as requested

- For **bump only**, give the temporal result, briefly identify that earlier context is historical, and optionally recall the last subject when it genuinely helps orientation. Do not hand the user an old agenda or assume it remains their priority.

- For **bump and resume**, use the shortest source-faithful recovery path for the active task. Recover the latest authoritative state rather than trusting an old summary. Keep completion, approval, pending work and implementation claims distinct. Execute what is authorized without asking the user to repeat retrievable context.

- For an explicit "close this session" request, defer to `ending-session`; do not conflate coming back with closing or continuity packaging.

- For agent provisioning/initialization, defer to `agent-bootstrap`; a returning user simply bumping an old conversation is not an agent bootstrap.

- If the user provides a new topic immediately after bumping, answer that new topic. No obligatory "shall we continue?" gate.

## Compact user-facing result

Prefer a small, readable receipt appropriate to the receiving host. Use interactive controls only when genuinely needed and supported; do not create empty, decorative or unverified controls.

Example with an explicitly supplied last-active time and a trustworthy current clock:

> **Session bumped**

>

> Last active: Mon, Oct 5, 2026 at 12:23 AM AST (user-provided)

>

> Now: Fri, Oct 9, 2026 at 3:56 PM AST

>

> Gap: **4 days, 15 hours, 33 minutes**

>

> Earlier conversation: useful history, **not** an automatically active assignment.

When exact previous activity is unavailable:

> **Session bumped** - Current local date/time: [verified value]. Previous last-active timestamp is not available to me, so the exact gap is unverified. I'll treat prior chat material as historical context and follow your current request.

For a brief question about time gap alone, answer briefly. For a substantial re-entry, show the minimal previous subject or verified checkpoint if helpful; label missing parts rather than invent them.

## Boundaries and acceptance checks

- **Opening a chat without sending a message cannot invoke this skill.** It responds to an actual user turn, including explicit bump commands and contextually clear return cues. Do not imply a background monitor or automatic chat-open detection.

- "Bump session" after inactivity -> temporal receipt, no write, no automatic resumption.

- "Last active Monday Oct 5 at 12:23 AM; now Friday Oct 9 at 3:56 PM AST" -> 4 days, 15 hours, 33 minutes.

- "I found this old chat, but I don't know when I last used it" -> establish today's verified anchor; exact gap unknown; no guessed timestamp.

- "Bump and finish the Drive cleanup" -> time anchor, then current source recovery and authorized cleanup rather than reusing stale task state.

- Old chat says "today is Sunday", but current date is Friday -> Sunday remains historical; never carry the old weekday into the new session.

- Old task was marked completed or explicitly closed -> do not resurrect it merely because this thread was reopened.

The quality bar is a clear temporal boundary with the least friction possible. The user owns whether the old subject becomes active again.
