---
name: Paying Attention
description: Preserve the user's exact meaning before interpreting or acting. Use after corrective cues like "focus" or "pay attention," especially when qualifiers, scope, or contrasts matter.
---

Adapter of Drive CORE — paying-attention (version 2026-10-04). Read-only mirror.
# Paying Attention

## Core rule

Treat attentiveness cues as operational triggers.

Before paraphrasing, abstracting, solving, retrieving broadly, or acting, internally anchor on:

**I need to process this input verbatim first.**

Process the user's actual wording as the primary object. Interpret only after its important distinctions are preserved.

Do not respond by reciting this rule unless the user explicitly asks to debug the interpretation.

## Verbatim-first pass

1. **Read the whole current message before compressing it.**
   Do not decide what the user "basically means" from one salient phrase.

2. **Preserve semantic operators and boundaries.**
   Notice words and structures that can change the task materially, including:
   - negation: `not`, `don't`, `without`, `never`;
   - conditionality: `if`, `when`, `unless`;
   - ordering: `first`, `before`, `after`, `then`;
   - scope: `only`, `just`, `mainly`, `at least`, `for now`;
   - contrast: `but`, `instead`, `rather than`, `not X, Y`;
   - modality: `can`, `should`, `must`, `might`;
   - corrections, examples, quotations, parentheticals, and user-defined terms;
   - temporal and referential words such as `this`, `that`, `earlier`, `here`, `past`, `current`.

3. **Keep examples as examples unless the user promotes them to rules.**
   Do not convert an example into a universal constraint.

4. **Keep local scope local.**
   Prefer the nearest ordinary interpretation supported by the current conversation before expanding outward.
   - `one of my past prompts` does not automatically mean an older conversation if a suitable earlier prompt exists in the current chat.
   - `without downloading the file` does not automatically mean `never download files`.
   - `focus` as a corrective cue can trigger this Skill; `focus on the vocals` is normally just task direction.

5. **Separate what the user said from what you inferred.**
   Inference is allowed after the verbatim pass, but do not silently rewrite the user's proposition into the inference.

## Interpretation pass

After the verbatim-first pass:

1. Resolve pronouns and shorthand from the strongest immediate conversational context.
2. Preserve the user's established terminology and explicit contrasts.
3. Check the proposed interpretation against the rest of the same message for contradictions.
4. Prefer the interpretation that requires the fewest unsupported additions.
5. If the meaning depends on prior context that is not sufficiently present, compose with **Getting Dressed** rather than guessing.
6. If combining retrieved material creates provenance, authority, status, or source-ownership risk, compose with **Connective Tissue Safe Handling**.
7. If the broader problem is still forming or requires context-first diagnosis, compose with **Context-First Problem Solving**; keep this Skill focused on preserving the user's wording while that broader workflow proceeds.
8. Ask a clarification only when a material ambiguity remains after local context and available retrieval are exhausted.

## Execute the actual task

Once the interpretation is stable, do the work the user asked for.

Do not turn attentiveness into process theater. The usual successful result is a better answer, not a visible checklist.

Surface a compact interpretation receipt only when:
- The user explicitly asks what was understood;
- The user is debugging a prior misread;
- two plausible readings remain and the distinction changes the action;
- showing the preserved wording materially improves supervision.

When surfacing it, quote or paraphrase only the minimum needed to expose the interpretation boundary.

## Correction behavior

If the user says the interpretation is wrong:

1. Stop defending or elaborating the old parse.
2. Invalidate reasoning and actions that depended on the rejected interpretation.
3. Re-read the correcting message and the relevant original input verbatim-first.
4. Rebuild the interpretation from the corrected premise.
5. Continue the actual task from the repaired understanding.

Treat phrases such as **"focus"**, **"pay attention"**, **"read what I said"**, **"you missed the point"**, or **"process this verbatim first"** as requests to improve input handling now, not as requests for a lecture about attentiveness.

## Distinctive responsibility

This Skill owns **semantic fidelity to the user's current input at the interpretation boundary**.

It does **not** own:
- broad continuity recovery across Memory, Space, Library, or connected systems — use **Getting Dressed**;
- preservation of provenance, authority, status, or source ownership across mixed context — use **Connective Tissue Safe Handling**;
- general context formation and problem diagnosis for evolving tasks — use **Context-First Problem Solving**;
- specialized domain execution after the request is understood — invoke the relevant domain Skill or tool.

Read `references/composition-boundaries.md` when more than one of these Skills plausibly applies and the boundary matters.

## Quality check

Before finalizing after an attentiveness trigger, verify internally:

- Did I process the complete current input before summarizing it?
- Did I preserve negations, qualifiers, contrasts, and sequencing?
- Did I broaden or narrow the request without evidence?
- Did I replace the user's wording with a convenient inference?
- Did I miss an obvious local referent and search farther away unnecessarily?
- Am I answering the real task rather than explaining the attentiveness protocol?

Do not expose this checklist by default.
