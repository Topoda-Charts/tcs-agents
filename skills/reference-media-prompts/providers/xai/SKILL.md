---
name: Reference media prompts
description: >-
  Use when writing generation prompts for reference-based image or short-form video — produce one clear affirmative production brief for the target model.
  Drive hub owns the canonical CORE; this copy is versioned 2026-10-16
  from CORE — reference-media-prompts.
---

Adapter of Drive CORE — reference-media-prompts (version 2026-10-04). Read-only mirror.
# Reference media prompts

**Source:** Drive CORE — reference-media-prompts (private Drive hub). Local copy dated 2026-10-16. Prefer the Drive CORE on conflict; refresh this copy when the hub updates.

Write the generation prompt as a concrete production brief. Give the target model one clear output path.

## Core rules

1. **Use affirmative instructions.** State what appears, happens, and how it is filmed — not avoidance/exclusion.
2. **Choose one specific visible answer.** No menus (`blue or gray`, `shirt or jacket`, `such as`, `depending on`).
3. **Resolve unspecified details when control matters.** One sensible choice from context (use reference images for identity, proportions, complexion, visual context); randomness only when requested.
4. **Separate identity from current styling.** Reference establishes who; prompt establishes how they appear now.
5. **Be exact without over-choreographing motion.** One coherent situation and simple behavioral progression.
6. **Concrete visual language before mood language.** Prefer nouns, actions, framing, materials, colors, camera behavior.
7. **Keep short clips (≈5–10s) behaviorally simple.** Single moment that can unfold naturally.
8. **State production constraints early.** Duration, orientation, content type, speech state near the beginning.

## Construction order (short-form video)

1. Deliverable → 2. Subject → 3. Situation → 4. Exact wardrobe → 5. Camera/framing → 6. Simple behavior → 7. Motion quality → 8. Lighting/finish/intended use

For stills: omit duration/motion; specify composition, pose/activity, wardrobe, lighting, finish.

## Template

```text
Create a [duration] [orientation] [content type] featuring [subject].
[Subject] is [specific situation]. [Subject] wears [exact garment + color].
Use [framing] with [camera behavior] and [lighting]. [Subject] [one coherent progression]. [Subject] stays [speech state].
Keep movement continuous and believable. The finished clip reads as [intended use].
```

## Example: good short promo prompt

```text
Create a 6-second vertical social promo featuring a young male performer. He is standing beside a studio backdrop between takes. He wears a plain burgundy T-shirt and black trousers.
Use a medium-close handheld shot with soft studio lighting. He notices the person filming, looks into the lens, smiles at their reaction, and shifts his stance as the moment continues. He stays silent throughout the clip.
Keep the movement continuous and believable. The finished clip feels like a usable behind-the-scenes promotional post.
```

## Failure patterns (rewrite before answering)

Branching wardrobe/setting choices; "what not to do" instead of replacement; `such as`/`or`/`depending on`; unspecified wardrobe when reference outfit would become unwanted fallback; abstract personality adjectives; gesture checklists in short clips; calling something natural while forcing elaborate performance; choosing a wardrobe color without considering visible reference context.

## Final check

Every important visible detail has one clear value; affirmative instructions; one coherent situation; simple behavioral progression; identity ≠ current styling; wardrobe explicit when it matters; each sentence narrows the generator's choices instead of expanding them. Return the finished prompt directly unless the user asks for explanation or variants.
