---
name: Workspace skill changing update
description: >-
  Use when the user has authorized a behavioral change to a workspace Skill — apply
  the smallest complete update via UpdateSkill and validate; not for Last
  reviewed-only maintenance. Drive hub owns the canonical CORE; this copy is
  versioned 2026-10-06 from CORE — workspace-skill-changing-update.
---

Adapter of Drive CORE — workspace-skill-changing-update (version 2026-10-04). Read-only mirror.
# Workspace skill changing update

**Source:** Drive CORE — workspace-skill-changing-update (private Drive hub). Local copy dated 2026-10-06. Prefer the Drive CORE on conflict; refresh this copy when the hub updates.

Apply authorized changes to workspace Skills and return a complete validated replacement Skill.

## Core boundary

This is the **mutation lane**.

- Change Skill behavior only when the user has authorized the change in the current request or explicitly approved a concrete maintenance finding.
- Do not treat a maintenance finding alone as authorization.
- Do not use this Skill merely to review a Skill or refresh `Last reviewed`; that belongs to `workspace-skill-maintenance`.
- Preserve unaffected behavior, resources, and identity.

## Required composition

Use the Cursor-managed **skill-authoring** Skill plus **UpdateSkill** as the construction, validation, and packaging authority for every Skill-changing update.

For an existing Skill:

- preserve the complete Skill structure (`SKILL.md` frontmatter + body);
- edit only the authorized scope;
- remove obsolete residue only when the change makes it genuinely superseded;
- validate the whole Skill, not just the edited fragment;
- write the complete updated Skill with UpdateSkill (`action: write`, pass existing `id`).

Grok Bot does **not** use ChatGPT `skill.zip` / `agents/openai.yaml` packaging. The installed form is the workflows `SKILL.md` managed by UpdateSkill.

## Inputs

Accept either:

1. a direct user instruction describing the Skill change; or
2. an authorized change brief from `workspace-skill-maintenance`.

A useful change brief contains the target Skill identity, mismatch, controlling evidence, required behavior, and regression scenario. If enough context is already established, do not force the user to restate it.

## Workflow

1. **Resolve the exact editable Skill source.**
   - Distinguish installed runtime state (`the installed skill file`) from Drive CORE.
   - Preserve the existing Skill identity unless the user explicitly requests a rename or replacement.
   - Do not infer a writable source from a display name alone.

2. **Recover the authorized change and current authorities.**
   - Preserve the user's exact proposition and scope.
   - Retrieve the current workspace authority needed to verify stale source, routing, terminology, access, or workflow assumptions.
   - Follow legacy redirects to current maintained owners instead of hard-coding obsolete locations.

3. **Load skill-authoring.**
   - Follow its write/rewrite path.
   - Keep frontmatter `name` and `description` accurate; keep assistant-specific details out of the shared recipe when possible.
   - Keep the package lean; remove only unused template/example residue.

4. **Apply the smallest complete change.**
   Examples include:
   - correcting stale source-routing instructions;
   - replacing obsolete connector/tool assumptions (map ChatGPT/OpenAI wording to Grok Bot tools: UpdateMemory, UpdateSkill, Slack/Gmail/Drive/Notion MCP, box paths);
   - changing trigger conditions or description metadata;
   - repairing workflow sequencing or authorization logic;
   - updating scripts/references/assets that materially support the Skill.

5. **Preserve review ownership.**
   - Do not use the behavioral update itself to claim that the Skill received a full maintenance review.
   - Do not refresh `Last reviewed` merely because a change was made unless the user also requested a maintenance review or current workspace policy explicitly couples the two.

6. **Validate the complete Skill.**
   - Re-read the written `SKILL.md`.
   - Confirm description still says when to use it.
   - Confirm Drive CORE link and dated-copy provenance remain accurate unless the authorized change was to those fields.
   - Fix validation failures before declaring done.

7. **Regression-test the behavior that exposed the issue.**
   - Recreate the smallest scenario that previously failed or drifted.
   - Confirm the new instructions route/behave correctly.
   - Also check that one important unaffected path still behaves as before when practical.
   - Do not claim runtime behavior changed merely because the file is correct — confirm with a real use when material.

8. **Hand off.**
   - State what changed, what was preserved, what was tested, and that the Skill is live via UpdateSkill.
   - Mention the skill as `[name](sand-workflow:<id>)` when reporting to the user.

## Relationship with maintenance

Preferred lifecycle:

`workspace-skill-maintenance` → review + `Last reviewed` → change candidate if needed → user authorization → `workspace-skill-changing-update` → validated UpdateSkill rewrite

After installation, a later maintenance review may verify the live installed copy and refresh `Last reviewed`. Do not collapse these two lanes into one hidden operation.

## Output

Return:

- target Skill;
- authorized change applied;
- files materially changed;
- validation result;
- regression-test result;
- installation/update status.

If the source is unavailable or the change cannot be safely applied, report the exact blocker rather than manufacturing a replacement from incomplete context.
