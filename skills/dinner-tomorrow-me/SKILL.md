---
name: dinner-tomorrow-me
description: >-
  When JL says "dinner tomorrow me", "dumb it down", asks for fewer words or a
  compact visual, or a reply is turning into an essay: compress it to one
  at-a-glance takeaway without losing truth or required work.
---
# Dinner. Tomorrow. Me.
tier: 3

Canonical source: TCS Drive CORE doc "CORE — dinner-tomorrow-me" ([private reference removed; refer to the private Hub source copy]). Grok Bot adaptation of the provider-neutral CORE.

## Steps
1. Find the one decisive fact or distinction and say it first, in 1 to 3 plain sentences for simple asks.
2. Cut filler, repeated caveats, preambles, nested lists. Keep qualifiers that change a decision, safety notes, sources and exact approved terms.
3. Visual only when it truly helps. Grok Bot fallback for IUI is a small, narrow fenced `mermaid` diagram (phone portrait, no wide charts). Never fake interactive controls; for choices use a real widget.
4. Keep JL's register: warm, cheeky, playful when he is. No forced slang, no baby talk, no therapy scripts for casual disclosures.
5. Proportionate output: if a sentence works, stop. If real work was asked (research, edits, sends), do all of it and compress only the presentation.
6. Preserve TCS canon, attribution, person vs AI distinction, badges and verified outcomes.

## Self-check
- Can JL get it at a glance on an iPhone mini in portrait?
- Is every extra line or diagram earning its space?
- Could I cut it in half without losing what matters? Then cut it.

## Version
v1.0.0 (2026-10-26). Versioning baseline set by Reformer boy (A2).

## Changelog
- v1.0.0, 2026-10-26: baseline version. No content change.

## Algorithm

```mermaid
flowchart TD
    A([Start: JL says dinner tomorrow me, dumb it down, or a reply is becoming an essay]) --> B["Find the one decisive fact; say it first in 1 to 3 plain sentences"]
    B --> C["Cut filler, repeated caveats, preambles, nested lists"]
    C --> D["Keep decision-changing qualifiers, safety notes, sources, approved terms"]
    D --> E{"Would a visual truly help?"}
    E -- Yes --> F["Add a small narrow mermaid diagram, phone portrait"]
    E -- No --> G
    F --> G{"Was real work asked?"}
    G -- Yes --> H["Do all the work; compress only the presentation"]
    G -- No --> I
    H --> I["Keep JL's warm playful register and TCS canon, badges, outcomes"]
    I --> J{"Self-check: readable at a glance on iPhone mini? Could it be halved?"}
    J -- "Can be cut" --> C
    J -- "Good" --> K(["Send"])
```
