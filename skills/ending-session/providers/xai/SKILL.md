---
name: Ending session
description: >-
  Use when the user says exactly "End session.", asks to close the session, or asks whether the session is ready to end — run the Yes/No/Other packaging-consent gate and orchestrate a verified, proportional closeout.
  Drive hub owns the canonical CORE; this copy is versioned 2026-10-16
  from CORE — ending-session.
---

Adapter of Drive CORE — ending-session (version 2026-10-15). Read-only mirror.
# Ending Session

**Source:** Drive CORE — ending-session (private Drive hub, CORE dated 2026-10-15). Local copy dated 2026-10-16. Prefer the Drive CORE on conflict; refresh this copy when the hub updates. Provider-specific adapters named in the CORE are optional; resolve real capabilities at runtime and report gaps rather than assuming them.

## Entry and consent routing

**Exact `End session.` message:**

1. Ask only: **Package this conversation for continuity using the conversation-continuity-packaging skill? Yes / No / Other**

2. Stop and wait. **Do not** run tools, retrieve sources, inspect files, prepare drafts, create packages, verify unrelated work, or perform writes before the user answers. The closing cue alone does not approve persistence.

3. On **Yes**, run the approved closeout flow below and invoke `conversation-continuity-packaging` without another confirmation.

4. On **No**, end briefly **without** creating any continuity artifact or doing source reads/writes.

5. On **Other**, follow the alternate instruction. Clarify only if materially ambiguous.

**Other explicit close requests:** If the user authorizes packaging in the same message (e.g. "Close and save a continuity packet"), proceed without another packaging question. If they request closing but do not decide about packaging, use the same brief Yes / No / Other gate. If they explicitly decline packaging, close without one.

**Readiness check only** (e.g. "Are we ready to end?", "What's left before closing?"): answer from known verified state, separating completed, pending, and optional work. Do not automatically package, persist, or treat the check as the literal end trigger.

**Already confirmed Yes:** Never restart the confirmation gate while packaging that same session. Multiple instructions or invocations of child skills must not cause duplicate packages or repeated questions.

## Approved closeout flow

1. **Bound the scope.** Identify the actual work and current-turn closure request from this conversation. Keep prior verified receipts; do not conduct an exhaustive workspace audit simply because the session is ending.

2. **Verify claims proportionally.** Distinguish completed actions from accepted decisions, unresolved work, unverified claims, and optional future projects. Retrieve a current source only when its state is necessary to establish a consequential closeout claim. Do not create phantom blockers or relitigate a settled decision.

3. **Preserve the useful state.** Invoke `conversation-continuity-packaging` after approval. It owns recovery, packet boundaries, concise source-faithful writing, authoritative source routing, subject-owned placement, deduplication, and readback. Keep continuity packets useful to a future conversation, not full transcripts or duplicate governance sources.

4. **Check the receipt.** Require the actual saved filename, path, file identity, and readable contents. If packaging fails, state exactly what was and was not saved; apply a proportional supported recovery before considering manual delegation. Never claim success solely because draft text or a local file exists.

5. **Present a verified retrievable result.** Use the active provider's supported native artifact reference or a tested durable link. Verify the stored identity, content and actual access behavior when possible; avoid fabricated deep links or unauthenticated temporary paths.

6. **Close cleanly.** Give a brief status: saved/verified or not; any genuinely unresolved prior work and its next action; then stop. Do not initiate a new project or ask another engagement question after successful closure.

## Compose, do not duplicate

Call or load the smallest applicable specialist(s), when available:

- **`conversation-continuity-packaging` (required only after packaging approval):** recovery, compression, packets, subject-owned storage, and readback. Its standalone `End session.` gate is already satisfied by this orchestrator; do not re-ask.

- **`company-knowledge-routing` (conditional):** decide whether a fresh Drive, Notion, Linear, Slack, or other owned-source check is really necessary; preserve owners instead of restating rules in packet form.

- **`connective-tissue-safe-handling` (conditional):** status/provenance ambiguity, rejected premises, proposed identities, or claimed approvals; avoid carrying stale material into the packet.

- **`library-file-processing` (conditional):** nontrivial subject placement, existing artifact identity, retrieval, or duplicate inspection. Let the packaging skill handle routine placement without a second processing pass.

- **`auditable-actions-tracing-and-logging` (conditional):** significant verified mutations need a concise receipt; do not invent a new permanent audit file for every session end.

- **`in-session-phasing` (conditional):** longer multi-step closeouts with genuine work and checkpoints. Skip ceremony for one straightforward packet.

- **`getting-dressed` (conditional):** source-chat context is materially missing or interrupted. Do not reload a workspace merely to close a well-understood session.

- **`paying-attention` (conditional):** an explicit correction needs its exact scope preserved in the closeout; do not broaden the correction.

If a specialist is not installed or callable in the current environment, apply only the supported locally known procedure and be transparent about missing capabilities. Naming a skill is not proof that it executed. No child skill's mere relevance authorizes writes outside the actual closeout request.

## Failure boundaries

- **No invented capability blockers.** Check realistic connector routes and input formats before offloading a simple task to the user. Describe the specific unsupported operation only when truly blocked.

- **No unsolicited durable mutation.** Packaging approval permits continuity storage, not identity migration, skill installation, GitHub commits, Notion rewrites, or creation of Linear issues.

- **No forced handoffs.** Retain explicitly unfinished work in the next-action field if the user prefers closing; do not demand that the user do ordinary agent operations.

- **No false app claim.** A native file reference working in one observed session do not promise identical behavior on every client or guess a deep-link scheme.

- **No duplicated orchestration.** The parent orchestrates the exit; the continuity child packages it. Avoid calling the whole closeout recursively.

- **Respect account boundaries.** Store in the invoking bot's authorized durable artifact store; do not assume packets are available to other seats, bots, or providers.

## Acceptance scenarios

- `End session.` -> ask **Yes / No / Other** and wait, with no reads or writes beforehand.

- Reply `Yes` -> package once, save, read back, cite the actual saved file inline, and close without further questions.

- Reply `No` -> close with zero new files.

- Reply `Other` -> use provided alternate closeout instructions rather than assuming consent.

- `Are we ready to end?` -> state readiness; do not initiate packaging.

- `End session and package it now.` -> execute the explicitly authorized packaging without redundant confirmation.

- A rich file view fails -> use a truthful simpler provider-supported reference; do not fabricate links, copies or confirmation.
