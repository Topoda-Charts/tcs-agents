# TCS and RLSim orientation

Applicability: any agent assigned TCS or RLSim work. This is a public onboarding summary, not the complete game design or proof of shipped functionality. Reviewed 2026-09-29.

TCS is User’s gaming, software, AI, and technology company. RLSim is its current central product: one software program explored through different builds, platforms, prototypes, and AI-assisted implementation. Related world/story work supplies that product and its creative universe; it does not automatically create separately committed products.

## Keep the layers distinct

| Name | Layer |
| --- | --- |
| Tópoda Charts / Tópoda Charts Studios / TC / TCS | Real-world solo studio, production, publishing, and operations |
| TCSU | Franchise/shared-universe umbrella |
| Record Label Simulator / RLSim | Playable living-world and music-industry management game |
| Gaia | Shared fictional world |
| The Twenty-four Hundreds / TTH | Story and narrative source layer |
| Bloomville in Cities: Skylines II / Tomorrow's Sun newsroom | Separate immersive gameplay/reporting workflow |

Similar names and reused characters do not merge source scopes. A story fact may inform a mechanic, but an explicit game source must define the adaptation. A Cities: Skylines II screenshot is not evidence about RLSim implementation or Gaia canon.

## What RLSim is trying to deliver

RLSim is about popular culture with the music industry as its playable core. The player operates a Record Label in a living world, directing priorities, budgets, strategic boundaries, schedules, and approval gates. Creators perform Creator-level work through the simulation; the player's role is executive direction and intervention rather than manually doing every creative task.

The intended loop is: inspect the label, roster, financial, and market state → make a commitment or constraint → advance simulation → receive workflow, market, chart, and financial outcomes → read compact causal feedback → approve, redirect, cancel, or reinvest.

The design is database-first in the sense of structured, connected, inspectable world state and logged actions. It does not require the player to operate a database console. Important outcomes should have understandable causes: which entities, resources, decisions, rules, histories, and probabilities contributed. Surprise is compatible with explainable systems.

User is the first intended player and an active design-quality gate. A coherent technical feature can still miss the intended experience. Current explicit intent supersedes obsolete feature assumptions; it does not establish that a feature is implemented.

## Vocabulary to preserve

| Term | Orientation |
| --- | --- |
| Creator / Creator ID | The contributing person/entity in the simulation; retrieve the exact current schema |
| Act | Public-facing performance identity, distinct from the contributing Creator |
| Record Label | The player-operated management organization |
| Track / Project / Master / Demo / Sheet Music | Distinct content/workflow objects; do not casually collapse them into one “song” record |
| Audience / Community Chunks | Structured audience/community representations; use the focused design authority for exact semantics |
| Charts / Critics / Awards / media institutions | Consequential systems with defined inputs and scope, not universal objective truth |
| Era / Legacy | Product-defined vocabulary; retrieve its current source rather than guessing from ordinary language |
| Causal receipt | Evidence behind a simulated outcome, usually exposed through a compact signal with deeper inspection available |

These are orientation notes. Capitalization and unfamiliar product terms often signal defined vocabulary. Read the current terminology/design owner before settling a disputed meaning or writing code.

## Current technical direction and milestones

Current design direction is a Windows-first native Unity 6.5 HDRP game, with C#, UnityBootstrap as the active project, Unity-native local/offline save authority, and appropriate data-oriented systems. Exact current implementation requires the actual game repository, tests, build, and runtime. This public website repository is a delivery/information surface, not the game runtime.

The first public Experimental Alpha is a focused proof for observing, inspecting, and saving Central Bloomville. The internal MVP means the smallest complete playable realization of the intended base game: broader-Gaia simulation plus the player-operated Record Label management loop. Those milestone terms must not be silently substituted for one another.

Older browser-first/PWA-as-primary-game assumptions are not the current direction. Web prototypes, public sites, services, and optional conversational interfaces are separate surfaces. A conversational control layer must read authoritative game state and issue defined actions; it cannot improvise itself into simulation authority.

## Experience principles

Make the next decision legible. The default player view should communicate the affected entity, direction, magnitude, and attention cue through compact game-native presentation. Deeper records, logs, and “why” views remain available without making ordinary play a sequence of paragraph reports.

Support legitimate ways to care: strategy, discovery, world observation, Creators and Acts, charts, discographies, collections, aesthetics, and self-directed goals. Complexity and challenge are welcome when they come from understandable systems. Avoid underconstrained guessing and information-navigation friction that adds no decision or observation.

Automation should remove repetitive work without erasing what the player enjoys. Where supported, it should remain inspectable, configurable, pausable, and overridable. Drama and humor can emerge from characters, industry institutions, and consequences while causality stays coherent.

Media is a legitimate discovery surface. A generated image, video, song performance, or scene can reveal a useful design question. The discovery becomes a proposal until User and the owning source adopt it; the media itself does not prove a mechanic exists.

## Work examples

For a canon question, retrieve the focused Drive owner and answer at its scope. For a feature proposal, state the current design, concrete change, player consequence, and decision needed. For implementation, read repository instructions, inspect the actual code, make the bounded change, and verify the behavior. For a character performance, recover that character and world, perform faithfully, and keep proposed design translation separate from canon.

Use Linear when the work creates actual tracked execution. Keep Notion for decisions and operating context, Drive for durable product/design knowledge, and runtime evidence for implementation. The [routing guide](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/agents/routing.md) explains the handoff.
