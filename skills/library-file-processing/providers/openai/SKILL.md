---
name: library-file-processing
description: "Process ChatGPT Library artifacts for persistent staging, durable retrieval, semantic naming and placement, provenance preservation, duplicate review, and recurring intake maintenance. Use when durable Library handling is already established by an explicit user request, an upstream durable-intent handoff, a batch-processing instruction, or a standing/scheduled Library-maintenance workflow."
---

Adapter of Drive CORE — library-file-processing (version 2026-10-13). Read-only mirror. STALE: older than its CORE; use the root SKILL.md instead.

# Library File Processing

Treat ChatGPT Library as a persistent staging and retrieval surface. Turn authorized Library artifacts into clear, retrievable, well-placed records while preserving identity, provenance, and useful distinctions.

## Invocation and authority

1. **Establish the active processing scope.**
   - Accept an explicit user request, upstream durable-intent handoff, batch instruction, or standing/scheduled maintenance workflow as processing authority.
   - Apply the caller's granted scope directly to routine naming, classification, placement, indexing, and maintenance work.
   - Use well-supported content-based inference for ordinary Library decisions.
   - Escalate only when unresolved uncertainty would materially change identity, ownership, approval/canon status, destructive disposition, or another reserved decision.

2. **Receive artifacts at the correct lifecycle point.**
   - Let the parent problem-solving context determine whether an artifact is ephemeral, working material, or intended for durable handling.
   - Begin Library processing when durable handling is established.
   - Return working/context-only material to the parent task after its immediate use.

3. **Match action depth to the granted scope.**
   - Treat ordinary organization and maintenance as preservation-oriented work.
   - Apply cleanup, consolidation, or destructive disposition when the caller's active scope includes that work and the target is established safely.
   - Route creative, canon, policy, access, or broad information-architecture decisions to the authority that owns them.

## Core workflow

### 1. Inspect the actual artifact

- Read or inspect the artifact itself before assigning identity, name, or placement.
- For images, use visible content as the primary inspection surface.
- For documents, combine title, content, structure, and available metadata.
- Materialize bytes when programmatic or format-specific inspection requires them.
- Establish exact file identity or runtime path through supported file operations before programmatic access.

### 2. Establish retrieval identity

Determine the narrowest useful combination of:

- specific subject, entity, event, or artifact target;
- exact artifact or asset class;
- owning project, personal domain, or system;
- meaningful variant, source role, state, date, or version.

Preserve established names and class distinctions. Keep unresolved identity or ownership explicitly unresolved until evidence supports a more specific classification.

### 3. Name for retrieval

Use **narrow -> broad** artifact naming: specific retrieval target first, then immediate type/context, then broader owner or project when useful.

- Replace opaque/default names when the artifact can be identified confidently.
- Let folder placement carry contextual meaning so filenames stay concise.
- Prefer precise asset classes when the class is established.
- Add dates, versions, source labels, or variant markers when they improve retrieval, sequencing, provenance, or disambiguation.
- Follow any current maintained naming convention supplied by the caller or controlling workflow.

A useful general shape is:

 `Specific Subject - Asset Class - Distinguishing Context - Broader Owner.ext` 

Use only the components needed to keep the artifact discriminative.

### 4. Choose the semantic home

Use **broad -> narrow** folder placement.

- Route by natural subject owner first and artifact type second.
- Prefer an existing relevant folder when it already provides the right retrieval context.
- Keep hierarchy shallow when additional levels add little retrieval value.
- Create structure when a durable recurring category or meaningful retrieval distinction justifies it.
- Use temporary intake/review placement when classification remains unresolved.
- Preserve current separation among personal, company, project, and other established domains.
- Re-read current Library state before acting so placement reflects the live hierarchy.

Use source-routing capabilities when destination ownership crosses Library and another maintained system.

### 5. Preserve provenance and meaningful variants

Treat provenance as part of retrieval identity.

- Preserve distinctions such as uploaded/generated, original/derived, source snapshot/reference, working/approved, alternate export, or access-path role when they materially matter.
- Treat matching title, filename, size, or visual similarity as a duplicate signal that requires comparison.
- Before consolidation or disposition, establish whether unique content, annotation, version history, source role, access role, or meaningful provenance remains.
- Co-locate related variants when shared placement improves comparison while preserving their individual identities.
- Carry approval or canon status only from an established source or user decision.

### 6. Apply the smallest useful mutation

Use Library mutation operations for persistent Library changes such as rename, move, folder creation, upload, replacement, consolidation, or authorized disposition.

- Make the smallest change that produces the intended retrieval state.
- Preserve stable file identity when the supported operation allows it.
- Read the exact current destination before consequential writes when concurrent changes could matter.
- Preserve unrelated work and existing useful references.
- Route provider-backed source changes through the owning provider when Library exposes an external or mounted source.
- Use recoverable disposition when the active cleanup scope and platform support it.

### 7. Verify retrieval

After mutation:

- read back or list the resulting artifact and location;
- confirm stable identity, final filename, and final path when available;
- use a plausible semantic search for important or ambiguous artifacts when that materially tests future retrieval;
- repair a weak name or placement before completing the batch;
- report retrievability only for the contexts actually verified.

## Batch processing

For a multi-file batch:

- treat the batch instruction as one processing scope;
- inspect each artifact individually;
- reuse established naming and placement patterns where they genuinely apply;
- distinguish clear placements, unresolved items, provenance/duplicate candidates, and disposition candidates;
- keep the batch bounded enough to verify every consequential mutation;
- proceed through routine supported inferences directly inside an already-authorized batch.

## Recurring maintenance and checkpointed intake

When a scheduled or recurring Library-maintenance workflow invokes this Skill:

1. Read the caller's current maintained workflow, index, receipt, or coverage checkpoint when one exists.
2. Use the latest **successful coverage endpoint** when the maintained workflow distinguishes it from artifact modification time.
3. Query with a small deliberate overlap and compare stable identities to recognize already-processed artifacts.
4. Inspect and complete a manageable maintenance batch.
5. Update the existing retrieval/index artifact when the current workflow maintains one.
6. Verify consequential mutations by stable identity when available.
7. Leave the exact next continuation point or coverage endpoint required by the caller's handoff contract.

Use current maintained checkpoint state rather than historical dates, paths, or filenames. When no recoverable checkpoint exists, use the caller's stated fallback or select current candidates conservatively.

A scheduled maintenance invocation supplies standing authority for its ordinary in-scope Library work. Execute supported routine processing directly within that scope.

## Source and capability composition

- Keep this Skill focused on Library processing mechanics and retrieval quality.
- Use source-routing capabilities for system ownership and authority questions.
- Use document or media specialists for format-specific editing.
- Use the parent problem-solving Skill for artifact-intent interpretation before durable processing begins.
- Follow the caller's reporting, receipt, and handoff contract as the operational trace for the run.

## Completion

Report proportionately:

- what was processed;
- material names, placements, consolidations, or other mutations;
- unresolved items or routed decisions;
- retrieval-verification result.

For scheduled maintenance, follow the scheduled task's receipt and notification rules, including quiet completion when that workflow calls for it.

## Skill maintenance

When real use exposes stale assumptions, unsupported tool behavior, outdated naming guidance, or a recurring failure mode:

1. identify the exact mismatch;
2. explain the maintenance need to the user;
3. preserve the installed Skill until explicit update authorization is given;
4. after authorization, update, validate, test, and repackage the complete Skill;
5. verify the revised behavior against the case that exposed the drift.
