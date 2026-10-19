---
name: workspace-skill-maintenance
description: "Review one or more workspace Skills for staleness, broken references, source drift, trigger drift, obsolete assumptions, package hygiene, and alignment with current workspace guidance. Use when asked to review, maintain, audit, inspect, health-check, or refresh workspace Skills without changing their intended behavior. This Skill may update only the target Skill's `Last reviewed` metadata and may produce a change brief for workspace-skill-changing-update; it must not silently rewrite behavioral instructions."
---

Adapter of Drive CORE — workspace-skill-maintenance (version 2026-10-04). Read-only mirror.

# Workspace Skill Maintenance

Review workspace Skills without becoming their behavioral editor.

## Core boundary

Treat **review** and **change** as different operations.

- Review the target Skill against current workspace reality.
- Update only its `Last reviewed` metadata when the review completes.
- Do not change triggers, workflow logic, source-routing rules, permissions, examples, scripts, references, assets, UI metadata, or intended behavior during maintenance.
- When a behavioral or structural change is warranted, produce a bounded change brief for `workspace-skill-changing-update` instead of making that change here.

A review finding is not authorization to edit behavior.

## Review metadata standard

Use this body metadata line in a workspace Skill's `SKILL.md`:

 `**Last reviewed:** <ISO 8601 timestamp with timezone>` 

Place it immediately after the introductory heading or existing package metadata block when practical.

- If the line exists, replace only its timestamp after a completed review.
- If it is absent, adding this one line is permitted as a metadata-only maintenance action.
- Do not treat `Last reviewed` as a package version or as proof that behavior changed.
- Do not update `Last reviewed` when the review was materially blocked or incomplete. Report the blockage instead.

## Workflow

1. **Resolve the target Skill.**
   - Use the installed Skill surface, an uploaded/package source, Library artifact, repositorythe working directory source, or another current authorized source.
   - Preserve the exact Skill identity and distinguish installed runtime state from editable source/package state.

2. **Recover current workspace guidance.**
   - Retrieve only the smallest current authorities needed to evaluate the Skill.
   - Follow redirects and migration notices to their maintained destination.
   - Treat legacy redirects and retired pages as navigation aids, not controlling authority.
   - Prefer the current topic-level authority over an obsolete monolithic page when the workspace has been reorganized.

3. **Review the Skill.**
   Check only what is relevant to the target, including:
   - trigger/description fit;
   - stale tool, connector, model, source, seat, persona, permission, Library, Memory, or routing assumptions;
   - hard-coded page/file names that now redirect or have been superseded;
   - obsolete terminology or source ownership;
   - broken internal references;
   - contradictory or duplicated instructions;
   - package hygiene and unnecessary example residue;
   - mismatch between documented workflow and observed real use.

4. **Classify findings.**
   Use one of these outcomes:
   - **current / no change needed**;
   - **maintenance metadata only**;
   - **change candidate**;
   - **blocked / unable to review**.

5. **Update `Last reviewed` only when review completed.**
   - Modify no other behavior-bearing content.
   - If changing a source file requires skill packaging tooling, use the supported Skill packaging workflow only for this metadata-only change.
   - Preserve the Skill's behavioral version unless workspace policy explicitly says review metadata changes version it.

6. **If a change candidate exists, prepare a changing-update brief.**
   Keep it concise and specific:
   - target Skill and source identity;
   - exact stale/current mismatch;
   - evidence or current authority that exposed it;
   - behavioral surface that would need editing;
   - expected corrected behavior;
   - regression scenario that should prove the fix;
   - authorization status: **not yet changed** unless the user separately authorized the changing update.

7. **Verify the maintenance action.**
   - Re-read the target source or packaged Skill.
   - Confirm the intended `Last reviewed` value.
   - Confirm no behavior-bearing content changed.
   - If a package was rebuilt only to carry review metadata, verify its structure and identity.

## Handoff to changing update

When behavioral drift is found, end with a clear handoff such as:

 `CHANGE CANDIDATE -> workspace-skill-changing-update` 

Do not auto-convert that finding into a rewrite. The changing-update lane requires explicit authorization through the user's request or a separate authorized invocation.

## Output

Report:

- Skill reviewed;
- review outcome;
- `Last reviewed` timestamp written or why it was not written;
- material findings;
- whether a changing-update handoff is needed;
- verification result.

Keep review evidence factual and proportional. Do not turn a maintenance review into a full workspace audit unless the user requested one.
