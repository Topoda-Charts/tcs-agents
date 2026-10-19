---
name: connective-tissue-safe-handling
description: "Preserve provenance, authority, status, and source ownership when combining context across chats, Memory, Library, agents, documents, and connected systems. Use when there is risk of context bleeding or contamination; when proposals, inferences, approvals, promoted material, canon/current-state claims, superseded material, or derivative summaries could be confused; when an output appears to violate controlling guidance; when repairing contaminated context; or when deciding whether a claim may be carried forward, written into a maintained source, or must remain provisional. Preserve healthy connective tissue without allowing repetition, proximity, familiarity, or derivative consensus to manufacture authority."
---

Adapter of Drive CORE — connective-tissue-safe-handling (version 2026-10-04). Read-only mirror.

# Connective Tissue Safe Handling

Preserve useful relationships among facts, ideas, sources, decisions, and artifacts while keeping each item's identity, provenance, authority, scope, status, and owner intact.

Use this Skill as a **status-preserving context composition layer**. Connect related material aggressively when useful; prevent the connection itself from changing what any connected item is allowed to mean.

## Core invariants

1. **Connect; do not flatten.** Preserve relationships without merging distinct propositions, sources, owners, statuses, or authority levels.
2. **Never promote by repetition.** Repeated wording, many derivative records, frequent resurfacing, proximity in one document, or apparent consensus among AI-authored summaries do not increase authority.
3. **Preserve source ownership.** A continuity packet, summary, handoff, audit receipt, Memory item, or AI output may point to a claim; it does not become the owner of that claim merely by restating it.
4. **Separate approval from promotion.** Treat explicit human approval as permission for a conclusion to become durable. Treat durable promotion as a separate act: writing the approved result into the source that owns the resulting claim and verifying that write.
5. **Separate promotion from canon/current authority.** A promoted record is authoritative only within the scope its destination actually owns. Canon or current-state status requires the appropriate controlling source or explicit human decision path.
6. **Treat inference as inference until approved.** Useful connective reasoning is allowed. Label new conclusions as inference while provisional; do not disguise synthesis as retrieval.
7. **Keep proposals recoverable without making them creep.** Resurface relevant proposals with accurate provenance and status until resolved. Frequency of resurfacing never turns a proposal into a decision, canon item, or current rule.
8. **Fail closed on consequential provenance gaps.** For identity, authority, approvals, permissions, canon, source routing, authorship, or other claims where a wrong assumption could constrain later work, preserve the last verified state or mark the new claim unverified rather than backfilling authority.
9. **Do not convert undefined into unresolved.** Missing elaboration, missing documentation, nondisclosure, or absence from one source does not automatically create an open decision, defect, blocker, or documentation debt.
10. **Do not resurrect rejected or superseded premises.** State the corrected current proposition directly. Preserve the history of an error only where audit/provenance value genuinely requires it.
11. **Repair violations from the controlling rule.** When an output violates current guidance, correct the proposition, status, source, or behavior directly. Do not preserve the bad output as ambient context by surrounding it with permanent caveats.
12. **Keep domains typed.** Personal context, creative exploration, product canon, governance, execution state, implementation evidence, and external facts may inform one another without inheriting one another's authority.

Read `references/status-model.md` whenever approval, promotion, canon/current status, proposal state, inference state, or supersession is material.
Read `references/failure-patterns.md` when auditing contamination, repairing a bad output, or reconciling mixed-source context.

## Workflow

### 1. Identify the handling mode

Classify the immediate job before acting:

- **Compose** — combine related context into a useful answer, artifact, or handoff.
- **Inspect** — determine whether context bleeding, contamination, status drift, or authority drift has occurred.
- **Repair** — correct contaminated output or persisted context.
- **Promote** — move an explicitly approved conclusion into the source that owns it.
- **Resurface** — bring a still-unresolved proposal or decision gate back into relevant context without changing its status.

Use more than one mode when necessary, but keep the status transitions explicit.

### 2. Recover the minimum controlling context

Retrieve only what is needed to establish the current propositions and their owners.

- Use current conversation, Memory/personal context, and Library for continuity.
- Use the source that owns the claim when current authority matters.
- Use connected systems for their actual source roles rather than treating all retrieved text as one memory pool.
- Prefer user-authored instructions, corrections, decisions, and supplied facts over AI-authored summaries of them.
- Treat AI-authored derivatives as evidence of what an agent previously concluded, not as proof that the user decided it.

If source ownership is unclear, use the source-routing capability rather than guessing.

### 3. Decompose the context into proposition units

Before combining material, distinguish the smallest claims whose status could differ.

For each consequential proposition, establish as much of the following as the task needs:

- **Proposition** — what exactly is being claimed.
- **Origin/provenance** — user, source document, agent inference, external authority, etc.
- **Owning source/domain** — where this kind of claim is actually controlled.
- **Current status** — established, proposal, inference, approved, promoted, canon/current, superseded, rejected, undefined, unverified, etc.
- **Scope** — what the proposition actually applies to.
- **Chronology** — current vs. historical.
- **Disposition** — carry forward, resurface, repair, promote, retire, or leave untouched.

Do this internally unless surfacing the distinctions helps supervision or resolves ambiguity.

### 4. Add connective tissue without changing status

Connect propositions when the relationship is useful: dependency, analogy, chronology, causal link, shared owner, contrast, provenance path, concept neighborhood, implementation relation, or another supported connection.

When the relationship itself is newly inferred:

1. retrieve the premises;
2. state the inferred connection as inference;
3. keep confidence proportional to the evidence;
4. preserve the premises' original statuses;
5. present the new conclusion for human approval before durable promotion when the conclusion would become company knowledge, canon, policy, authority, or another consequential durable claim.

Do not let “these belong together” become “these are the same thing.”

### 5. Apply the promotion gates

Use `references/status-model.md` rather than a vague sense that something is “basically decided.”

At minimum:

- A **proposal** remains a proposal until explicit user resolution or an already-authorized decision path establishes otherwise.
- A newly generated **inference** remains provisional until explicit user approval.
- An **approved** conclusion becomes eligible for durable promotion; approval does not prove the owning source has been updated.
- A **promoted** conclusion has been written into its owning durable source and verified; it carries only the authority that source owns.
- **Canon/current authority** requires the appropriate controlling source or explicit human decision path.
- **Supersession** requires newer controlling authority, not a later derivative summary or newer edit timestamp alone.

Never infer a status transition from familiarity, repetition, naming prominence, polished wording, placement in a formal-looking document, or an AI-authored label.

### 6. Run contamination checks

Before finalizing consequential synthesis or after detecting a suspect output, check for these patterns:

- repetition promotion;
- derivative consensus;
- proposal-to-fact bleed;
- inference-to-source bleed;
- approval-to-promotion bleed;
- promotion-to-canon bleed;
- historical-to-current resurrection;
- personal-context-to-product-canon bleed;
- specification-to-implementation bleed;
- one source's authority leaking into another source's domain;
- assistant interpretation being misattributed to the user;
- maintainer/editor identity being misread as authorship or decision authority;
- undefined material being relabeled open/unresolved/incomplete;
- rejected premises surviving as permanent caveat or rebuttal text;
- output-format prominence being mistaken for substantive importance;
- a guideline-violating output becoming a downstream source merely because it was summarized later.

Use `references/failure-patterns.md` for repair patterns.

### 7. Repair at the narrowest authoritative layer

When contamination is found:

1. recover the current controlling proposition;
2. identify which exact surface is wrong;
3. correct the owning source first when the owning source itself is wrong and the write is authorized;
4. correct or retire downstream derivatives after the owner is current;
5. remove rejected or contaminated wording from maintained current-state prose rather than preserving it as a recurring warning;
6. preserve a separate incident/audit trace only when the history of the contamination has continuing value;
7. verify the repaired state by reread, targeted search, comparison, or another direct check appropriate to the system.

If only the current response is wrong and nothing durable was changed, correct the response directly. Do not manufacture a persistent incident record by default.

### 8. Handle guideline-violating outputs safely

When an agent output conflicts with maintained guidance:

- identify the exact violated proposition or behavior;
- retrieve the controlling guidance or user correction;
- replace the bad behavior with the current correct behavior;
- prevent the violating output from becoming authority through later summaries, handoffs, or copied text;
- distinguish a one-off output error from a reusable workflow gap;
- route a genuinely recurring generalizable gap to the mechanism that owns behavior maintenance when authorized;
- avoid encoding the rejected output itself as a permanent “do not do X” artifact unless the failure pattern genuinely needs durable incident evidence.

Prefer **clean replacement** over defensive prose accumulation.

### 9. Resurface proposals without contaminating them

When a proposal becomes relevant again:

- identify the proposal as a proposal;
- preserve who originated it;
- point to the best current durable record or continuity trace;
- summarize only the current useful substance;
- mention materially relevant new context that changes the decision environment;
- ask for or route to a decision only when the current task genuinely reaches that gate;
- keep the proposal in proposal state if the user does not resolve it.

Do not treat repeated resurfacing as evidence that the user has implicitly accepted the proposal.

### 10. Verify the final connective state

Before completion, confirm that:

- every consequential claim carries the right status;
- provenance and authorship are not conflated;
- the correct source owns each durable claim;
- historical and current states are separated;
- no derivative record is being used as circular proof of authority;
- rejected/superseded material cannot be mistaken for current guidance;
- any promoted claim was actually written and verified;
- any still-provisional inference or proposal remains visibly provisional where the distinction matters.

## Output behavior

Keep the visible response proportional. Do not force a status table onto simple work.

When a contamination or promotion boundary materially matters, use a compact structure such as:

- **Current proposition:** what is established now.
- **Connective tissue:** the useful relationship or inference.
- **Protected boundary:** what must not be promoted, merged, or misattributed.
- **Action:** preserved / resurfaced / repaired / promoted / left provisional.
- **Human gate:** include only when a real reserved decision remains.

For persistent mutations, compose with the auditable-action capability and report the verified resulting state.

## Composition with other Skills

- Use **Neighboring Concept Disambiguating** when the problem is primarily distinguishing close terms or concepts.
- Use **Company Knowledge Routing** when the immediate question is which source owns a claim or where to read/write it.
- Use **Proposal Drafting** when human-originated messy material needs to become a decision-ready proposal.
- Use **TCS Evidence Confidence** when evidence quality, sufficiency, or conflicting support is the central problem.
- Use **Memory Updating** only when the user asks to persist or correct Memory.
- Use **Auditable Actions Tracing and Logging** after substantial persistent repairs or promotions.

This Skill owns the **safety of the connective layer** among those capabilities: preserve useful relationships while preventing status, provenance, and authority from bleeding across them.

## Examples

### Repeated proposal

Several Library packets and agent summaries mention the same Gaia proposal. No explicit user decision adopted it.

**Handle as:** a durable, relevant proposal that may be resurfaced. Do not describe the repeated mentions as consensus or canon.

### Approved inference not yet promoted

An agent inferred a useful company rule and the user explicitly approved the inference, but the owning Notion authority has not been updated.

**Handle as:** approved and eligible for promotion. Do not claim Notion already establishes it. If promotion is authorized, write it to the owning source and verify before calling it promoted.

### Contaminated derivative consensus

One assistant hallucination was copied into three handoffs and two summaries.

**Handle as:** one contaminated lineage, not five independent confirmations. Recover the controlling source, repair current derivatives as authorized, and keep historical evidence only where useful.

### Output violates current guidance

An assistant response reintroduces a rejected premise and then spends several paragraphs caveating it.

**Handle as:** replace the response with the corrected current proposition. Do not preserve the rejected premise as recurring context merely to explain that it is wrong.
