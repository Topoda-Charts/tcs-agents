---
name: getting-dressed
description: "Recover missing working context before acting, then resume the real task. Use when the user says \"get dressed\", \"recover it\", \"you're naked\", \"read Library/Memory\", \"continue\" after a detour, asks to pick up prior work, or when a request depends on TCS/Gaia/project state that is not sufficiently present in the current chat. Retrieve the relevant sources and tools instead of merely reciting a recovery protocol, reconstruct the active Thread/Phase/Task/Step, and continue execution. Especially useful for multi-source work across Notion, ChatGPT Library, Google Drive, Linear, GitHub/runtime, Supabase, Slack, Memory/personal context, and the web."
---

Adapter of Drive CORE — getting-dressed (version 2026-10-04). Read-only mirror.

# Getting Dressed

## Core rule

Treat **Get dressed** as an operational recovery trigger.

Do not answer by merely saying context is missing, reciting a protocol, or asking the user to repeat information that can be retrieved. Retrieve the missing context first, restore the working position, and resume the actual work.

The user's metaphor is:

- missing context = the clothes do not exist;
- unretrieved context = the clothes are in the closet and the assistant came downstairs naked anyway.

## Recovery workflow

1. **Identify what is missing.**
   Determine whether the gap is the workstream, governing source, current phase, objective, next step, recent decision, artifact, execution state, or implementation reality.

2. **Recover immediate continuity first.**
   Use the current conversation before external retrieval. If the relevant state is not sufficiently present, retrieve it from the appropriate personal or company sources.

3. **Fan out when one source is too thin.**
   For broad or ambiguous context, open a small fan of thick, relevant pages/files rather than relying on one keyword hit. Ask yourself useful questions while reading:
   - What currently controls this?
   - What changed most recently?
   - What was the user trying to accomplish?
   - Where did the work actually stop?
   - What is established, inferred, stale, or unresolved?
   - What can be executed now without another approval?
   Answer those questions from the retrieved evidence before proceeding.

4. **Route by claim type.**
   For TCS/company work, read `references/tcs-source-routing.md` when source ownership matters. Do not search every system mechanically; use the smallest set that can restore the needed state.

5. **Reconstruct the working position.**
   Restore these four fields internally:
   - 🧵 **Thread** — the active workstream or subject.
   - 🧭 **Phase** — the bounded stage the work is currently in.
   - 🎯 **Task** — the concrete objective being accomplished now.
   - 👣 **Step** — the next executable move.

   Surface them to the user only when doing so improves supervision, resolves ambiguity, or the user explicitly asks. Otherwise, use them as the internal recovery frame and keep moving.

6. **Resume, do not stop at recovery.**
   Invoke any task-specific skill that now matches, call the relevant tools/connectors, and perform the next authorized action. A successful recovery should normally end in forward progress, not a context summary.

7. **Take command within the authorized scope.**
   Exercise delegated judgment through ordinary reversible decisions. Continue until reaching a genuine user-controlled gate such as creative canon approval, taste, a materially ambiguous product decision, permission boundary, or consequential irreversible action.

8. **Ask one small question only if retrieval cannot resolve the blocker.**
   State what was recovered and ask the narrowest question that changes the next action. Do not fabricate missing state.

## Manual fallback chain

Use this when the user is manually seeding recovery or when source retrieval is unavailable:

1. Prefer the exact message where the current work began: the message that gave the task, request, or problem.
2. If that message is missing, use the earliest surviving message that clearly shows what the work was trying to do.
3. If no message survives, use a one-sentence task statement plus the last remembered completed action.
4. If the user is totally unsure and says **"Recover it"**, reconstruct the workstream from the context and sources available to you.

Do not require the user to paste a message when reliable retrieval can recover the same state.

## Continuation semantics

- **"Continue" after a detour** means recover the substantive topic from before the detour and resume its actual state.
- **"Get dressed"** means retrieve context now, not explain how retrieval would work.
- **"Recover it"** means use available context and sources to reconstruct the workstream without making the user restate it.
- **"Take command"** means choose and execute the next authorized move, coordinate tools and sources, verify the result, and continue until a real human gate is reached.

## TCS execution bias

When the recovered work is TCS / Record Label Simulator / Gaia work, prefer actions that materially move the product forward over status-only narration. Examples include:

- move the boundary forward;
- complete one CEO decision loop;
- make Gaia move or become more observable;
- close a spec-to-code gap;
- verify implementation reality;
- take an issue to done;
- ship the user something he can touch;
- write a useful handoff only when it enables the next operator;
- keep going until you hit a genuine the user decision gate.

## Failure modes to avoid

- Reciting source-routing rules without calling the tools.
- Asking the user to repeat context that is retrievable.
- Treating the current chat as the whole world when prior context is clearly required.
- Searching one isolated keyword and stopping when adjacent sources are needed.
- Reading many sources but failing to answer the recovery questions they were opened to resolve.
- Producing a polished status report instead of resuming the task.
- Treating older continuity or copied material as current authority without checking the owning source.
- Claiming implementation from plans, specs, screenshots, or prose without runtime/repository evidence when implementation reality matters.
- Returning control to the user for ordinary agent-level decisions that can be safely resolved from current authority.

## Compact supervision pattern

When the user benefits from an explicit recovery receipt, use a brief pattern such as:

`` ```text ``
👔 Dressed.
🧵 Thread: [workstream]
🧭 Phase: [current stage]
🎯 Task: [current objective]
👣 Step: [next move]
`` ``` ``

Then execute the step. Do not let the receipt become the deliverable unless the user asked only for orientation.
