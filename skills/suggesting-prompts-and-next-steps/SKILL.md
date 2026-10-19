---
name: suggesting-prompts-and-next-steps
description: "Use when the user asks for suggested prompts, follow-ups, or next steps, or when a clearly valuable continuation exists after fully answering: offer 1-3 distinct, inspectable, actionable options with full next-turn prompts."
version: "2026-10-16"
source: "Drive CORE — suggesting-prompts-and-next-steps"
generated: "2026-10-18"
---

Generated from Drive CORE on 2026-10-18. Read-only mirror; edits here are overwritten.

# CORE — Suggesting Prompts and Next Steps

Status: New TCS-authored provider-neutral Skill source; validated ChatGPT adapter packaged on 2026-10-16; live installation pending.
Source owner: the private Drive CORE.
Origin: the user directly requested this standalone capability after reviewing vague, non-actionable follow-up recommendations. The user controls final naming, sufficiency and deployment.
Scope: reusable recommendations across conversation, creative exploration, research, design, implementation, and operations. It is NOT the IUI Research Panel Skill.

## Purpose
Given a fully answered current request, recover its context and identify a small number of distinctly useful optional follow-up prompts and next steps that the user can understand and choose without losing existing context. Never withhold completion of the current request to create an artificial need for another turn.

## Use when
User asks for suggested prompts, recommended follow-ups, next steps, what else to explore/investigate/create/verify/do, actionable one-tap continuations, or corrects suggestions that obscure the actual consequences. Offer proactively only when a live valuable continuation is evident. Do not force steps into jokes, emotional conversations, or self-contained questions.

## Inputs
The current user exchange; existing project/user context and confirmed constraints; optional relevant source records, permissions, selected research categories and budgets; actual available tools and UI mechanisms.

## Core procedure
1. Identify current answer status, live objective, user intentions and source/permission boundaries. Recover missing relevant facts using owning sources, not interrogation of the user.
2. Generate genuinely distinct candidates: EXPLORE (specific new angle), INVESTIGATE (source-backed question), COMPARE/CRITIQUE (clear opposing mechanisms), CREATE (defined output), VERIFY (observable test), ADVANCE (bounded authorized action). Choose appropriate categories, not a fixed quota.
3. Filter out generic 'dig deeper', redundant work, premature bureaucracy, unrelated scope expansion, invented dependencies, unavailable tools, and suggestions meant to compensate for deliberately incomplete work.
4. Rank quietly by contextual value, novelty, expected evidence or action gained, feasibility, user effort, time/cost, permission, reversibility and potential reuse. Offer normally one to three genuinely different options; avoid clutter.
5. Build an inspectable action contract for each: WHAT (verb and target); WHY NOW (grounded relevance); WHERE (sources/tools/affected assets); HOW (concrete retrieval, research, analysis, create/write/test sequence); RESULT (actual expected deliverable and verification); AUTHORITY (read-only, draft, write, send and any reserved human decision); DEPTH/COST (where materially relevant).
6. Compose a full next-turn prompt inheriting necessary constraints and context, with accurate scope, tools, acceptance criteria, and authorization boundaries. Buttons must reveal what clicking will request; a displayed button is neither task execution nor proof of success.
7. Render optional suggestions accessibly with working runtime-specific controls or legible text alternatives. On user selection, execute actual feasible work, verify observable results and distinguish drafted/posted/installed/completed states.
8. Stop when there is no worthwhile next option.

## Rules that survive every provider
- Complete the current user request before proposing supplementary work.
- Conversation and creative exploration are legitimate outcomes: do not convert every curiosity into project management.
- Reuse existing specialist workflows rather than duplicating their implementation. Extrapolating Logically, Correcting Course, Context-First Problem Solving, Implementation Planning, Company Knowledge Routing and IUI Research Panel remain separate owning capabilities.
- Preserve user-confirmed scope, canon, requested internal-only research boundaries, and independence of per-source research budgets where research panels are relevant. The separate IUI Research Panel 21+ catalog redesign is not part of this Skill.
- Cite recovered external/internal evidence correctly and separate current verified state from proposed action.
- Do not fabricate a clickable action, provider access, a written artifact, installation or a send receipt.
- If a proposed prompt is forwarded to another AI or human, visibly watermark the copyable text with the verified actual source agent identity, full badge, timestamp and provenance, according to Communicating Effectively. The user as messenger is not necessarily its author.
- A recommendation does not itself grant write, scheduling, publication, purchase or external-contact authority.

## Provider adaptation
ChatGPT Chat: when beneficial, use mobile-first native Intelligent UI with concise compact action cards, visible scope and algorithm, readable contrasts, and actual host-controlled buttons wired to a complete distinct next-turn prompt. Verify the supported API at runtime.
ChatGPT Work/Codex/other providers: adapt to actual supported tools, plain prompt options or equivalent UI. Never claim Chat-specific IUI is universal.

## Fallback
If source access or interactive controls are absent, provide complete inspectable text instructions, clearly identify the gap, and do not invent results. Use closest authorized source/tool only if it preserves scope.

## Verification
Contrast at least these cases: informative first answer fully complete, casual creative follow-up, actionable cross-source research within selected source scope, write versus read-only consequences, no useful suggestion, repeated generic button failure, visible native click binding with distinct prompts, and forwarding with correct authorship.

## ChatGPT implementation
Packaged complete Skill: SKILL.md, agents/openai.yaml, assets/icon.svg and references/regression-cases.md. Local validator passed; package is not auto-installed. Installer action and installed entrypoint readback remain separate.
