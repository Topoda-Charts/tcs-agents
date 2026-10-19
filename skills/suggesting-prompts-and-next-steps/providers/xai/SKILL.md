---
name: Suggesting prompts and next steps
description: >-
  Use when the user asks for suggested prompts, follow-ups, or next steps, or when a clearly valuable continuation exists after fully answering: offer 1-3 distinct, inspectable, actionable options with full next-turn prompts.
  Drive hub owns the canonical CORE; this copy is versioned 2026-10-16
  from CORE — suggesting-prompts-and-next-steps.
---

Adapter of Drive CORE — suggesting-prompts-and-next-steps (version 2026-10-16). Read-only mirror.
# Suggesting prompts and next steps

**Source:** Drive CORE — suggesting-prompts-and-next-steps (private source). Local copy dated 2026-10-16. Prefer the Drive CORE on conflict; refresh this copy when the hub updates.

**Registry:** private source (not published)

**Origin:** the user directly requested this standalone capability after reviewing vague, non-actionable follow-ups. The user controls final naming, sufficiency, and deployment.

## Purpose
After the current request is fully answered, offer a few distinctly useful optional follow-ups the user can pick without losing context. Never hold back completion to manufacture another turn. Not the IUI Research Panel skill.

## Use when
The user asks for suggested prompts / next steps / what else to explore, verify, or do, or corrects vague suggestions. Offer proactively only when a valuable continuation is evident; not for jokes, emotional talk, or self-contained questions.

## Procedure
1. Pin answer status, live objective, intent, and source/permission limits; recover missing facts from owning sources, not by quizzing the user.
2. Generate distinct candidates: EXPLORE, INVESTIGATE, COMPARE/CRITIQUE, CREATE, VERIFY, ADVANCE (bounded, authorized). No fixed quota.
3. Drop generic "dig deeper", redundant work, bureaucracy, scope creep, invented dependencies, unavailable tools, and padding for incomplete work.
4. Rank quietly (value, novelty, feasibility, effort, cost, permission, reversibility, reuse). Usually 1-3 options.
5. Give each an action contract: WHAT, WHY NOW, WHERE (sources/tools/assets), HOW, RESULT (deliverable + verification), AUTHORITY (read-only / draft / write / send; reserved decisions), DEPTH/COST when material.
6. Write a full next-turn prompt carrying needed constraints, scope, tools, acceptance criteria, and authorization limits. A displayed option must reveal exactly what choosing it will request; showing it is neither execution nor proof of success.
7. Render with what the Grok Bot surface really supports: real chat question widgets / quick replies wired to the full prompt, plain text options otherwise; when a visual of the options or flow genuinely helps, add a small phone-narrow fenced mermaid diagram (no native IUI); never imply a button ran something. On selection, do the work, verify, and distinguish drafted / posted / installed / completed.
8. Stop when nothing worthwhile remains.

## Rules
- Finish the current request first. Conversation and creative exploration are valid ends; don't turn curiosity into project management.
- Reuse specialist skills (extrapolating-logically, correcting-course, context-first-problem-solving, implementation-planning, company-knowledge-routing, iui-research-panel) instead of duplicating them.
- Keep user-confirmed scope, canon, internal-only research limits, and per-source research budgets. The separate IUI Research Panel 21+ catalog redesign is not part of this Skill.
- Cite evidence; separate verified state from proposal. Never fabricate clickable actions, access, artifacts, installs, or send receipts.
- If a suggested prompt will be forwarded to another AI or human, watermark it with the real source agent identity, badge, timestamp, and provenance (per communicating-effectively). The user as messenger is not necessarily its author.
- A suggestion grants no write, schedule, publish, purchase, or external-contact authority; sends still need the user's approval.

## Fallback
Without source access or controls, give complete text instructions, name the gap, invent nothing. Use the closest authorized source/tool only if it preserves scope.

## Verification
Contrast: complete informative first answer; casual creative follow-up; actionable cross-source research within selected scope; write vs read-only consequences; no useful suggestion; repeated generic-option failure; options wired to distinct full prompts; forwarding with correct authorship.
