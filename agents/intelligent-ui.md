# TCS Intelligent UI | Public ChatGPT Presentation Guide

**Scope:** ChatGPT Chat inline Intelligent UI (IUI) for authorized TCS collaboration.  
**Source version:** TCS Intelligent UI Living Design Standard 0.2.1, 2026-10-20.  
**Public mirror:** maintained distribution copy. The internal living standard and JL's newer decisions control on disagreement. This is not a native Skill installation, a permission grant, or a requirement imposed on unrelated providers or game HUDs.

## Use and applicability

Use visual structure when it materially helps comprehension, comparing items, exploring state, viewing progress, or taking a real action. In JL's collaborative chats, prefer meaningful IUI more often than dense prose, and use it when explicitly requested if the host can render it. Simple prose remains appropriate for simple messages and copyable text artifacts.

Read the actual UI capabilities of the current host. **Do not assume** ChatGPT Free, Work, Codex, other providers, or web-connected chatbots expose identical components. If interactive components are unavailable, communicate the same information clearly with regular Markdown, rather than pretending buttons or animations worked.

## Current visual contract

1. **Inherit the ChatGPT appearance.** Omit forced backgrounds and local dark/light themes. The host controls the canvas. Never add a black or white card fill merely to simulate dark or light mode.
2. **Substantial, meaningful iconography.** Allocate roughly **10% or more** of each meaningful panel/banner/row/column to an icon or visual anchor. Choose icons for information architecture, not decoration.
3. **Silver Glass outlines.** Default framed panels use a **4px rounded diagonal graphite-to-luminous-silver metallic border**, with transparent interior. Thick framing is purposeful; do not surround every sentence.
4. **Color with restraint.** Use color for semantic icons, text accents and occasional intentional border variants. Avoid broad saturated or colored background fills. Orange is Archangel's identifying accent, not a required border for every agent.
5. **Responsive composition.** Use useful width on desktop; reflow on narrow iPhones without cropped labels, horizontal overflow, illegible controls or tiny touch targets. Keep a readable hierarchy, spacing and grouping.
6. **Genuine interactive controls.** Buttons, tabs, checkboxes, sliders and other controls must use supported host actions or meaningful state. Never render a decorative control that appears clickable but does nothing.
7. **Readability before spectacle.** Keep clear titles, short labels, logical information groups, and copyable writing. Treat IUI as a presentation capability, not an excuse to bury the answer in an inert dashboard.
8. **Motion is optional and purposeful.** Where CSS-capable rendering supports Silver Glass, use an approximately **8-second subtle specular sweep** with a rest interval and visually seamless transparent endpoints. Move the highlight with transform/opacity, not expensive layout animation. Respect reduced-motion preferences; offer working pause/resume in animated demos.
9. **Preserve domain boundaries.** This is the ChatGPT inline conversation layer, **not automatically** the style for RLSim game canvases, Unity HUDs, websites, another provider, or a separate product.

## Silver Glass implementation selection

- **CSS-capable surface:** 4px rounded silver/graphite diagonal gradient ring; transparent panel; a very faint inner rim and reflection film; an 8-second subtle diagonal sweep; visible content remains above reflections. Keep the surface host-adaptive and provide a reduced-motion fallback. The material is faux specular lighting, not physical refraction.
- **Native component-only surface:** use a **flat 4px cool-silver outline** (approximate reference color `#AAB6C4`), rounded corners, a proportionally large semantic icon, and no background/theme override. This is an explicitly accepted fallback, **not** a claim to display gradient metal or animation.
- **Plain-text-only host:** maintain equivalent organization through concise headings, comparative tables when helpful, and honest descriptions. Do not claim an interactive IUI was rendered.

## QA checklist

Check light and dark host appearances, desktop and narrow-phone readability, title and icon contrast, clipping/overflow, readable text during any sweep, effective touch targets, actual control behavior, reduced motion, and absence of opaque panel fills. CSS demos additionally need seam-free animation loops, functional pause/resume and a real mid-loop change. Distinguish human aesthetic acceptance from automated/browser validation.

## RAW companion Skills for web-reading agents

These are existing published instructions in the public Skills mirror. **Retrieve only the one relevant to the task.** An OpenAI adapter is useful when current; otherwise use the provider-neutral CORE. The mirror is not proof the receiving chatbot can use a particular tool.

| Skill | Purpose | RAW instruction |
| --- | --- | --- |
| IUI Research Panel | Source-picker interface and research consent | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/iui-research-panel/SKILL.md) |
| Dinner Tomorrow Me | Concise, approachable visual explanation | [OpenAI adapter](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/dinner-tomorrow-me/providers/openai/SKILL.md) |
| In-Session Phasing | Visible checkpoints while doing substantial work | [OpenAI adapter](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/in-session-phasing/providers/openai/SKILL.md) |
| Suggested Prompts and Next Steps | Functional follow-up actions | [OpenAI adapter](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/suggesting-prompts-and-next-steps/providers/openai/SKILL.md) |
| Displaying Using Python | Display existing image pixels when a user-visible Python tool exists | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/displaying-using-python/SKILL.md) |
| Clocking In | Working-session recovery, dashboards and phase indicators | [CORE](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/clocking-in/SKILL.md) |

Complete catalog and adapter freshness: [RAW Skills index](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/README.md), [RAW manifest](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/skills/manifest.json).

## Demon Chat: minimal web-only route

Demon's own profile is [RAW Demon](https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/agents/standing/demon.md). When working from his personal Free ChatGPT context:

1. Open this public IUI guide through normal web browsing; report the version actually read.
2. For a task-specific procedure, follow the relevant verified RAW CORE/adapter above. **No Notion or Drive call is necessary merely to load these public procedures.**
3. Adapt to the current chat's real component/tool availability. A read is not an installation, a tool grant, or proof of rendering.
4. If private or recently changed canon/design/operational decisions are needed, request the narrow authorized source or source-backed excerpt. Never use an old public mirror as proof of private current state.
5. Retain Demon's own Trainer identity. Reading an Archie-authored guidance file does not turn Demon into Archie.

## Distribution and provenance

Public distribution only. No internal source URLs, private workspace IDs, credentials, user account addresses or personal archives are incorporated here.

Compiled by **Archangel Chat Sol Altman Ramos** (`TCS-OAI-CHAT-SOL-01`) on 2026-10-20, based on JL's current ChatGPT IUI living standard, for public RAW read-only distribution to Demon and other authorized web-reading collaborators. JL controls current design decisions. Later internal design updates require deliberate public mirror refresh; they do not appear here automatically.
