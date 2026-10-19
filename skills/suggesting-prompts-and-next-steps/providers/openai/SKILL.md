Adapter of Drive CORE — suggesting-prompts-and-next-steps (version 2026-10-16). Read-only mirror.
# SKILL.md — OpenAI adapter for suggesting-prompts-and-next-steps

Status: Packaged and locally validated; not yet installed.
Package contents: SKILL.md, agents/openai.yaml, assets/icon.svg, references/regression-cases.md.
Authoritative provider-neutral method: CORE document in the same canonical Skill folder's source/ subfolder.

## Trigger
Generate specific, useful, context-aware follow-up prompts and next actions after genuinely finishing the user's current task, or when asked what to do/explore/investigate/create/verify next. Involve native clickable controls where they improve selection. Reject vague labels, hidden tools and consequence-free suggestions.

## Algorithm
1. Ground in the actual finished response, direct user steering, source restrictions and unresolved objective; recover important context.
2. Generate Explore, Investigate, Compare/Critique, Create, Verify, Advance candidates only where relevant. Include conversational options for conversational topics.
3. Filter generic/redundant/impossible/scope-inflating options. Rank value, novelty, operational feasibility, user attention and permission/reversibility cost; present normally 1–3.
4. For every action, show target, why now, exact source/tool scope, concrete operations or reasoning algorithm, tangible expected output, read/write/send/installation implications and any real constraints.
5. Compile a complete next-turn prompt for each, preserving source limits and current context. Make the displayed action auditable before launch.
6. Chat UI: use supported DIL state and callbacks; use actual onClick={() => GenUI.issueNewTurn(completeDistinctPrompt)} in the UI only. Never imply a button press executes an external action before the new turn. If controls unavailable, show exact text prompts.
7. Carry out only the user-selected task when submitted, through actual tools, verify real effects, then distinguish draft, posted, installed and finished.
8. Avoid offering suggestions when current task does not merit them or when user wants simply a result.

## Distinctions
This Skill owns suggestion selection and executable framing. It composes Extrapolating Logically, Correcting Course, Context First Problem Solving, Implementation Planning, Company Knowledge Routing, Citing Sources, Communicating Effectively, and IUI Research Panel. It must not rewrite any of those Skills or claim they are absent. The Research Panel's own future 21+ sources and independent per-plugin counting are a separate redesign instruction.

## Portability and authorship
Only ChatGPT Chat may be assumed to offer its native IUI after capability verification. On another platform use the provider's actual tools or accessible text options. When writing a portable or forwarded agent prompt, embed the verified originating agent's stage name, signature heart and full badge INSIDE copyable material. Do not present the user as the author of AI-written text.

## Regression
Use the bundled regression-cases.md for: creative talk without homework, already-complete answers, named source constraints, write permission visibility, native functional buttons, missing installed exact Skill, independent research-source budgets, and cross-agent signatures.
