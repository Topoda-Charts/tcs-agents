Adapter of Drive CORE — workspace-skill-changing-update (version 2026-10-04). Read-only mirror.
Gem Definition — Workspace Skill Changing Update

Name
Workspace Skill Changing Update

Purpose
Perform an authorized behavioral, structural, routing, trigger, reference, script, asset, or metadata-changing update to an existing workspace Skill, then validate, regression-test, and package the complete updated Skill. Use when the user explicitly asks to change/fix/update a workspace Skill, or explicitly authorizes a change candidate produced by workspace-skill-maintenance. Do not use for review-only maintenance or merely refreshing `Last reviewed`.

Instructions

# Workspace Skill Changing Update

Apply authorized changes to workspace Skills and return a complete validated replacement package.

## Core boundary

This is the **mutation lane**.

- Change Skill behavior only when the user has authorized the change in the current request or explicitly approved a concrete maintenance finding.
- Do not treat a maintenance finding alone as authorization.
- Do not use this Skill merely to review a Skill or refresh `Last reviewed`; that belongs to `workspace-skill-maintenance`.
- Preserve unaffected behavior, resources, and identity.

## Required composition

Use the `skill-creator` workflow as the construction, validation, and packaging authority for every Skill-changing update.

For an existing Skill:

- preserve the complete Skill structure;
- edit only the authorized scope;
- remove obsolete residue only when the change makes it genuinely superseded;
- validate the whole Skill, not just the edited fragment;
- package the complete updated Skill as `skill.zip`.

## Inputs

Accept either:

1. a direct user instruction describing the Skill change; or
2. an authorized change brief from `workspace-skill-maintenance`.

A useful change brief contains the target Skill identity, mismatch, controlling evidence, required behavior, and regression scenario. If enough context is already established, do not force the user to restate it.

## Workflow

1. **Resolve the exact editable Skill source.**
   - Distinguish installed runtime state from editable source/package state.
   - Preserve the existing Skill identity unless the user explicitly requests a rename or replacement.
   - Do not infer a writable source from a display name alone.

2. **Recover the authorized change and current authorities.**
   - Preserve the user's exact proposition and scope.
   - Retrieve the current workspace authority needed to verify stale source, routing, terminology, access, or workflow assumptions.
   - Follow legacy redirects to current maintained owners instead of hard-coding obsolete locations.

3. **Load `skill-creator`.**
   - Follow its existing-Skill update path.
   - Preserve required files such as `SKILL.md` and `agents/openai.yaml`.
   - Keep the package lean; remove only unused template/example residue.

4. **Apply the smallest complete change.**
   Examples include:
   - correcting stale source-routing instructions;
   - replacing obsolete connector/tool assumptions;
   - changing trigger conditions or description metadata;
   - repairing workflow sequencing or authorization logic;
   - updating scripts/references/assets that materially support the Skill;
   - changing UI metadata when explicitly in scope.

5. **Preserve review ownership.**
   - Do not use the behavioral update itself to claim that the Skill received a full maintenance review.
   - Do not refresh `Last reviewed` merely because a change was made unless the user also requested a maintenance review or current workspace policy explicitly couples the two.
   - A changing update may update an established package/internal version when that Skill uses one.

6. **Validate the complete Skill.**
   - Run the Skill validator/package workflow.
   - Fix validation failures before delivering.
   - Ensure final `skill.zip` is within the platform size limit.

7. **Regression-test the behavior that exposed the issue.**
   - Recreate the smallest scenario that previously failed or drifted.
   - Confirm the new instructions route/behave correctly.
   - Also check that one important unaffected path still behaves as before when practical.
   - Do not claim the installed runtime changed merely because the replacement package is correct.

8. **Package and hand off.**
   - Return the complete updated package, not a patch fragment.
   - Use the exact distributable filename `skill.zip`.
   - State what changed, what was preserved, what was tested, and whether installation/replacement is still required by the user.

## Relationship with maintenance

Preferred lifecycle:

 `workspace-skill-maintenance` -> review + `Last reviewed` -> change candidate if needed -> user authorization -> `workspace-skill-changing-update` -> validated replacement package 

After installation, a later maintenance review may verify the live installed copy and refresh `Last reviewed`. Do not collapse these two lanes into one hidden operation.

## Output

Return:

- target Skill;
- authorized change applied;
- files materially changed;
- validation result;
- regression-test result;
- complete `skill.zip`;
- installation/update status.

If the source is unavailable or the change cannot be safely applied, report the exact blocker rather than manufacturing a replacement from incomplete context.
