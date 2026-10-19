---
name: conversation-continuity-packaging
description: "Preserve conversation context in one or more concise Markdown continuity packets saved to the invoking ChatGPT seat's Library for later retrieval and continuation. Use for chat compaction, preservation, continuity packaging, preparing durable starting state for future chats, and when the user says exactly `End session.`. On the exact `End session.` trigger, ask for a Yes / No / Other confirmation before any packaging work and wait for the user's reply. Shared across workspace-account seats: do not assume seats share one Library or the same source access."
version: "2026-10-13"
source: "Drive CORE — conversation-continuity-packaging"
generated: "2026-10-18"
---

Generated from Drive CORE on 2026-10-18. Read-only mirror; edits here are overwritten.

# Conversation Continuity Packaging

**Canonical CORE synchronization:** 2026-10-13; incorporates runtime functional changes through 2026-10-08. Provider-specific presentation remains in adapters.
 **Internal package version (referenced runtime):** `2026-10-08T16:51:51-04:00` 

Convert the useful state of a conversation into the smallest useful set of durable Markdown continuity packets. Preserve enough context for future retrieval and continuation without carrying the entire chat forward.

## Session-close confirmation gate (standalone fallback)

When `ending-session` or an equivalent authorized session-close coordinator has already collected an explicit Yes to packaging, proceed directly without asking the same question again. When invoked independently and the user says exactly **`End session.`**, treat that phrase as a request to close the session, **not** as permission to package it yet.
This Skill is the packaging specialist, not the general session-close orchestrator. Keep explicit packaging instructions actionable; route whole-session closeout decisions to the session-close coordinator when one is present.

1. Ask only a compact confirmation that can be answered with **Yes**, **No**, or **Other**:

   **Package this conversation for continuity using the conversation-continuity-packaging skill?**
   **Yes / No / Other**

2. Stop and wait for the user's reply. Do **not** begin context recovery, source reads, connector calls, drafting, Library writes, or verification before that reply.
3. If the user answers **Yes**, run the full packaging workflow below.
4. If the user answers **No**, do not package anything; briefly confirm that the session is ending without a continuity package.
5. If the user answers **Other**, follow the alternate instruction they provide. If their alternate instruction is still ambiguous, ask one minimal follow-up rather than requiring a detailed response up front.
6. Do not treat nearby wording such as “we're done here,” “this session ended,” or casual discussion about ending a session as this exact trigger unless the user actually says **`End session.`**.

This confirmation gate exists so session closure stays lightweight and deliberate. It overrides the normal immediate packaging workflow only for the exact **`End session.`** trigger.

## Shared seat orientation

Treat this Skill as a portable workspace-account procedure shared across seats.

- Do not assume a particular persona or seat is the invoker.
- Treat ChatGPT Library as **seat/context scoped unless current evidence proves broader access**. A packet saved by one workspace seat is not automatically present in another seat's Library.
- Resolve the active seat/persona only when identity, authorship, Library visibility, connector access, permissions, or attribution materially affects packaging or delivery.
- If those axes do not matter, remain identity-neutral.
- Preserve established AI Agent identities, source provenance, and actual permissions when they matter to continuity; do not invent access parity between seats or providers.

## Choose delivery

Save durable Markdown continuity packets in the **invoking ChatGPT seat's Library**.

If the active seat's Library is unavailable, inaccessible, or a save fails, try only a proportional, supported recovery. Stop at an access restriction; otherwise avoid repeating an unchanged failing attempt. Report which packets were prepared, which files were already saved, and which packets remain unsaved. Do not imply persistence succeeded or require the user to repeat the request.

## Recover context efficiently

Read all available source-chat content before compressing. Internally inventory substantial topics, important secondary threads, user corrections, decisions, meaningful personal or creative context, completed actions, and pending requests. Revisit early and middle portions as well as the ending so length and recency do not determine importance.

Reuse evidence already available. Retrieve attachments or connected sources only where their contents or current state materially affect the packet; batch independent reads and follow relevant names, relationships, aliases, and source links instead of relying on one exact phrase. Stop when the needed context is sufficient. Packaging does not require a workspace-wide audit or changes to maintained sources.

Treat summaries as summaries and check original evidence when exact wording, authorship, or completion matters. Distinguish direct the user statements, verified actions, assistant reports, and inference. If source history is unavailable or truncated, describe the material coverage gap briefly; never claim exhaustive recovery of unseen content.

## Establish Library placement and naming

Apply this section when saving continuity to the **active seat's Library**.

1. Load the current ChatGPT Library guidance before creating, moving, or verifying files.
2. Retrieve current Notion guidance when available, beginning with `TCS Conversation Routing Recommendations` and `AI Agents — Operating Context, Decisions & Recommendations`. If Notion is inaccessible to the active context, do not pretend it was checked; use the best authorized current source available and keep the access gap explicit when it materially affects routing.
3. Follow the user's newest applicable instruction, the current live Library structure visible to the active seat, and maintained guidance. Treat older fixed packet paths as historical when they conflict with current routing.
4. Route each packet to its natural subject owner in that Library, such as Personal, the relevant AI Collaboration concern, TCS / Record Label Simulator, RAW VOW, or Research & Analysis. Use an artifact-type subfolder only when it materially improves retrieval. If ownership remains unclear, use the current temporary intake or quarantine location.
5. Do not create or restore one universal `Conversation Continuity Packets` folder as the default destination.
6. Name artifacts narrow → broad. Put the human-searchable topic first, followed by the artifact type and date. Prefer:

    `[Narrow Packet Subject] - Continuity Packet - YYYY-MM-DD.md` 

## Choose packet boundaries

1. Identify whether the chat contains one continuity-worthy topic or multiple distinct substantial topics.
2. Create separate packets when the topics would be meaningfully easier to retrieve or continue independently.
3. Merge topics when they form one coherent future-use context, depend on the same decisions or relationships, or would naturally be needed together.
4. Choose the smallest number of packets that preserves all important continuity. Protect useful secondary topics without splitting minor tangents into their own files.
5. Avoid repeating material across packets. Keep only the small amount of overlap needed for each packet to stand on its own.

## Build each packet

Capture the current useful state for that topic rather than a chronological transcript summary. Include only what another chat would materially need:

- the topic's purpose or current objective;
- important conclusions, corrections, decisions, approvals, and exact terminology;
- relationships, mappings, dates, counts, or artifact references when they affect future understanding;
- completed work that changes what should happen next;
- unresolved work, blockers, dependencies, and the next useful continuation point;
- current controlling sources or retrieval directions when maintained authority matters.

State that the source chat may contain stale, superseded, or outdated context. Direct future use to compare the packet with newer chats, the user's newer instructions, current ChatGPT Memory when available, and maintained sources when relevant. Do not imply that conversation context, a continuity packet, or another external store is itself persistent ChatGPT Memory.

Include the source chat title/link and date range when available, plus the packet preparation date. Preserve event dates separately from capture dates. Add only useful retrieval aliases or exact source links; do not invent metadata. For future retrieval when the original sources may not be accessible, include the necessary substance rather than relying on inaccessible links alone. Preserve AI Agent identities, attribution, and actual permissions when those facts are established and material.

Preserve uncertainty as uncertainty. Do not fill missing context merely to make the packet feel complete. Exclude rejected assistant assumptions, mistakes, outdated interpretations, dead branches, incidental banter, repeated wording, and superseded conclusions unless a short historical note is necessary to prevent their return.

Keep each packet compact, self-contained, and useful for retrieval. Preserve the user's corrected proposition as the current fact; keep the rejected premise only when its history still carries real provenance or audit value.

## Check coverage and compression

Compare the draft against the topic inventory. Ensure every relevant substantive thread is represented, with its meaning, relationships, and necessary reasoning intact. Exhaustiveness means coverage of relevant context, not preservation of every sentence. Consolidate repetition before shortening unique information; use the smallest sufficient length rather than an arbitrary word cap.

Ask whether a fresh future chat could understand or continue each topic without making the user reconstruct it. Preserve useful personal, creative, and historical context even when it has no next action. Omit empty sections and invented blockers. Keep actual uncertainty distinct from pending work; a detail never specified is not automatically an open decision.

Check exact terminology, corrections, completed-versus-pending status, provenance, and cross-packet duplication. Carry approved scope and the next useful action where there is ongoing work. Exclude hidden reasoning and low-level tool narration.

## Save and verify

1. Create each packet as a Markdown file.
2. Save each file through the **active seat's ChatGPT Library** under its current subject owner.
3. Verify the returned filename and Library path for every file.
4. Check this task's returned file identities and moves for unintended duplicate Library copies or misplaced root items. Retained local working bytes are not an extra Library copy. Avoid a global duplicate scan for a bounded packaging task.
5. Preserve existing Library file identity when updating an existing packet; create a new file only when the packet has no existing Library identity or the user requests a separate copy.
6. Never claim another workspace seat or external AI can retrieve the saved Library packet unless that access was actually established. When another seat or provider needs continuity, rely only on an authorized shared continuity surface whose access is actually established.

## Report the result

Return each packet's filename, verified destination location, and a verified native opening reference appropriate to the active provider, client, and surface. Do not invent links or fabricate file citations. When multiple packets were necessary, briefly explain how topics were divided or merged and why. For one continuity-worthy topic, report its single packet without inventing additional divisions. Client-specific presentation and file-opening mechanics belong in the provider adapter.

## Skill drift

If real use exposes stale seat, Library, Memory, persona, access, routing, or source assumptions:

- 🚩 flag the exact drift in the maintained TCS Notion Skill-maintenance surface;
- 🗣️ tell the user which instruction needs maintenance and why;
- ⏸️ do not silently rewrite the installed Skill without authorization;
- 🔧 after authorization, update, validate, test, and repackage the complete Skill;
- ✅ verify the revised behavior against the scenario that exposed the drift.
