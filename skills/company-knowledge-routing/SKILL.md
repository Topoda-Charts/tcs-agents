---
name: company-knowledge-routing
description: "Route the next knowledge operation to the source or context that actually owns the needed information, and choose READ, WRITE, READ -> WRITE, or NONE. Use when deciding where to read or write company knowledge next (conversation, Notion, Drive, Linear, repository, database, chat, Library, public web, or another AI context) by ownership rather than convenience, when a named Skill is missing from the installed list, or when prior-decision recall needs the right starting source. Keep routing narrow and return to the parent task."
version: "1.3.1"
source: "Drive CORE — company-knowledge-routing"
generated: "2026-11-17"
---

Generated from Drive CORE on 2026-11-17. Read-only mirror; edits here are overwritten.

# Company Knowledge Routing

Route the next knowledge operation to the source or context that actually owns the needed information. Keep routing narrow: identify where to go, what to do there, and why that route is sufficient for the next step.

## Previous-decision source routing (user direction, 2026-10-25)

If the question is "what did we decide?", "where is the plan?", "we discussed this yesterday", or equivalent prior-work recall, the initial knowledge need is conversational continuity, not automatically the current Linear/Notion issue state. Start with the current thread, relevant prior chats/Memory and an existing owner-scoped scratchpad, then follow their verified pointers into maintained company sources as needed. Do not repeat unrelated searches against a convenient live connector simply because its title shares a term (for example, Linear archiving versus completed-issue compression, or website checkpoint cascade versus issue cascade).

If the request instead asks "what is currently implemented/open?", prefer the live owning system directly, using prior decisions only for interpretation. Respond to corrections by changing the retrieval route, not just polishing the answer; keep useful short progress updates. Distinguish Agent Card, live agent ID/IDENTITY, operating instructions, installed Skills, and scratchpad without turning any one of them into universal authority.

## Shared Business-seat orientation

Treat this Skill as a portable TCS procedure shared across Business-account seats.

- Use only plugins, connectors, sources, and contexts actually available to the invoking seat.
- Do not assume another seat has the same Library, connector access, permissions, files, or prior tool state.
- Treat an access gap as an access gap, not proof that the source or information does not exist.
- Resolve seat/persona identity only when access, permissions, authorship, attribution, or role materially changes the route.
- In TCS internal knowledge, an agent name, provider, seat, domain, source owner, folder, or document author records provenance and maintenance/claim authority; none of those labels by itself reserves reusable company knowledge to that agent. Any appropriately authorized TCS agent may retrieve, understand, reuse, adapt, challenge, and improve relevant shared knowledge through its actual available tools. Adapt execution to provider and domain; preserve source status, attribution, verified permissions, privacy boundaries, and the owner's decision rights. Do not manufacture exclusivity from provenance.

## ## Canonical Skill retrieval

When a named TCS Skill is missing from the active installed list, check the TCS Skills Registry (internal) before treating the Skill as unavailable.

- Match the exact slug or task function in the current catalog, then read the linked canonical Drive CORE.
- Load only the references needed for the current action. Do not read the whole catalog's CORE documents for each task.
- Keep canonical content, provider adapters, and installed runtime Skills distinct. Verify the active seat's tools and adapter before provider-specific execution; reading a CORE does not install or natively invoke it.
- If the catalog entry is missing or stale, search the canonical Skill Packages collection narrowly by slug and CORE title. A failed installed-Skill lookup is not proof that no canonical source exists.
- Apply the recovered procedure and return to the parent task. Propose source repair only when an actual gap remains.

Retrieval maintenance: authorized AI maintainer, 2026-10-16 (UTC−04:00).

## Routing workflow

1. **Identify the knowledge need.**
   - State the smallest missing fact, decision, record, live state, source, or durable destination that blocks or materially improves the next action.
   - Do not turn routing into general task interpretation or proposal development.

2. **Determine who owns that information.**
   - Route by claim ownership, data ownership, or operational role rather than convenience.
   - Use `references/routing-map.md` when the correct TCS surface is not obvious.
   - If the choice depends on disputed evidence, source credibility, confidence, or sufficiency, use the evidence-confidence capability rather than duplicating that analysis here.

3. **Choose the operation.**
   - **READ** when current knowledge must be retrieved or verified before proceeding.
   - **WRITE** when a durable change is already authorized, the exact destination is known and current, and no material read is needed first.
   - **READ -> WRITE** when an existing authority must be inspected before updating it. This is the normal route for requests such as updating company knowledge, correcting an existing source, or recording a decision in its current owner.
   - **NONE** when the current context is already sufficient for the immediate next step and no durable mutation or verification is needed.

4. **Name the narrow target.**
   - Route to the specific page, document, issue, repository area, table, channel, file, search target, or context when known.
   - If the exact object is unknown, name the smallest search scope that can locate it.

5. **Execute when authorized.**
   - If the needed tool is available and the user asked to continue or perform the work, make the routed read/write call instead of stopping at a routing recommendation.
   - If the user asked only what to call next, give the route and stop there.
   - Do not create an unnecessary knowledge call merely to demonstrate diligence.

6. **Return to the parent task.**
   - Routing is complete once the needed context is retrieved, the durable destination is updated, or the correct external context is identified.
   - Continue the original task with the recovered information rather than turning routing into a new workstream.

## Core source roles

Use current maintained source-routing authority when available. As a working default:

- **Current conversation / supplied material:** immediate user intent, current decisions, and locally sufficient context.
- **Notion:** governance, decisions, approvals, permissions, source routing, AI Agent operating guidance, incidents, handoffs, and durable coordination context.
- **Google Drive:** durable product knowledge, canon, design, specifications, research, terminology, worldbuilding, and creative source material.
- **Linear:** active execution state, ownership, priority, blockers, dependencies, milestones, cycles, and actionable follow-up.
- **GitHub / repository / runtime:** implementation-current code, schemas, tests, configuration, builds, and observed runnable behavior.
- **Supabase:** live structured database state and persisted records when the database itself is the system being inspected or changed.
- **Slack:** recent coordination, announcements, status updates, and transient team discussion when recency or communication state is the question.
- **ChatGPT Library:** continuity packets and retrievable artifacts when continuity or prior packaged context is needed; do not treat Library as automatically stronger than the maintained owning source.
- **Public web / provider source:** externally controlled facts, current public information, provider behavior, laws, standards, schedules, prices, or other changing outside reality.
- **Another available AI/platform context:** use when the requested information genuinely belongs to that platform-native context and the current seat cannot supply an equivalent source directly.

Read `references/routing-map.md` for detailed ownership and cross-source distinctions.

## Routing boundaries

- Do not use source routing as a substitute for understanding the task. If the thread itself is not yet intelligible, let context-first problem solving establish what is being asked before selecting a route.
- Do not use routing as a substitute for proposal development. Proposal work may call this Skill to retrieve or persist context, but routing does not define the proposal.
- Do not use routing as an evidence-ranking system. When competing evidence requires evaluation, use the evidence-confidence capability.
- Do not let a lower-authority source become controlling merely because it is easier to access.
- Distinguish the authority to maintain or approve a claim from another authorized agent's ability to read and apply the knowledge. If knowledge is useful across agents or providers, route the verified reusable rule to its shared Drive CORE/owner and relevant navigation, not an exclusive personal silo. Recipient agents may extend the method and submit verified improvements to the same owner. Keep actual connector access, confidential data and restricted actions scoped without using provider identity as a substitute access rule.
- Do not treat one global app hierarchy as universal. Different systems can simultaneously control different parts of the same situation.
- Do not freeze volatile outside facts into internal company knowledge as though TCS controls them. Persist the TCS decision, dependency, interpretation, or retrieval pointer when useful.

## Conflict and missing-source handling

When ownership is unclear:

1. Split the disputed question into the smallest distinct claims or state questions.
2. Identify which source owns each one.
3. If two sources answer different questions, preserve both rather than forcing a conflict.
4. If the ownership question itself is governed by TCS policy, route to current Notion source-routing authority.
5. If the disagreement is evidentiary rather than merely jurisdictional, use the evidence-confidence capability.

When an expected record is missing:

- Retry a narrow search using known terminology, project names, identifiers, or the likely parent collection.
- A failed search is not proof of absence.
- Check whether another source actually owns the information before creating a replacement record.
- Create new durable records only when the correct destination is known and persistence is authorized.

## Default response format

When the user asks only for the route, use:

**Next knowledge call:** `@Source - READ | WRITE | READ -> WRITE`  
**Target:** [specific object or narrow search target]  
**Why:** [one sentence explaining why this source/context owns the immediate need]  
**Unlocks:** [optional; include only when it clarifies the next action]

If no call is needed:

**Next knowledge call:** None - current context is sufficient for the immediate next step.

Do not add confidence scores unless the task independently requires an evidence audit.

## Examples

Read `references/examples.md` when calibration is useful.

## Skill drift

If real use exposes stale source ownership, connector guidance, context availability, or routing behavior:

- flag the exact mismatch in the maintained TCS Skill-maintenance/governance surface;
- tell the owner what needs maintenance and why;
- do not silently rewrite the installed Skill without explicit authorization;
- after authorization, update, validate, test, and repackage the complete Skill;
- verify the revised behavior against the case that exposed the drift.
VERSIONING & CHANGELOG — owner rule, 2026-10-21 8:00 PM AST (reconciled with the owning Portable Skill Source Standard, 2026-10-24)
1. Every TCS artifact (docs, skills, rules, profiles, bots) is versioned like software and has a changelog.
2. The changelog is the full versioned record of who changed what, when, and to which version. Patch notes are a short per-release summary for readers (Added / Changed / Fixed / Removed).
3. Each artifact keeps its own version and changelog of completed changes. Linear owns pending work, drift, propagation, blockers and validation; other records link to the artifact changelog rather than duplicate it. Controlling source: Portable Skill Source Standard, clarified 2026-10-24.
4. Each change bumps the artifact's version and adds one changelog entry. Proposed scheme (pending owner decision): MAJOR.MINOR.PATCH = behavior-breaking change / new rule or section / wording fix.
VERSION: 1.3.1 (2026-11-15 05:50 AST). Prior baseline retained.
CHANGELOG
- 1.3.1 — 2026-11-15 05:50 AST — Authorized AI maintainer, for the user. Reconciled obsolete pending-ruling language with the Portable Skill Source Standard's October 24 clarification: artifact history stays with its artifact; Linear owns execution/drift. Preserved the separately pending SemVer categories, functional routing contract and all prior author history. Source-only documentation correction under the owner's reversible CORE consolidation direction; provider adapters, backend releases and runtime adoption not changed. Recovery: prior source revision history.
- 1.3.0 — 2026-11-07 AST — Authorized AI maintainer, for the user and authorized TCS agents. User correction: clarified that source agent/provider/domain and maintainer ownership are provenance, never an invented restriction on reuse; shared CORE discoverability, authorized cross-provider adaptation and improvements remain the norm. Preserved real privacy and access permissions. Source: the user's direct correction.
- 1.2.0 — 2026-10-25 AST — Authorized AI maintainer, directly authorized by the user — Added the company-knowledge-routing retrieval/identity/Skill/scratchpad/progress correction and regression boundary; existing behavior preserved.
- 1.1.0 — 2026-10-21 ~8:10 PM AST — Authorized AI maintainer, per the user's 8:00 PM AST rule — Added the "Versioning & changelog" section, version line and this changelog. No other section changed.
- 1.0.0 — before 2026-10-21 — unversioned baseline (see Drive version history).
