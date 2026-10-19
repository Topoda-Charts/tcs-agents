---
name: citing-sources
description: "Retrieve, attribute, and cite the actual sources supporting factual claims, prior-conversation recollections, organizational decisions, current project status, financial figures, and researched answers. Use when the user asks \"where did that come from?\", \"cite your sources\", \"don't you remember?\", \"we discussed this\", \"check our Space\", \"what do the records say?\", or when consequential assertions rely on files, Memory, connected systems, documents, emails, code, or web sources. Prevent unsupported claims of absence, false citations, and source/authority confusion."
version: "2026-10-15"
source: "Drive CORE — citing-sources"
generated: "2026-10-18"
---

Generated from Drive CORE on 2026-10-18. Read-only mirror; edits here are overwritten.

# Citing Sources

## Purpose

Make each consequential assertion traceable to evidence that actually supports it. A **source** is an origin, firsthand report, observation, or retrievable record. A **citation** is a locator pointing back to that source. **Retrieval** is the act of consulting it. Neither a citation nor a search result automatically proves a claim.

This Skill controls *retrieval discipline, attribution, and citation fidelity* across factual and creative work. Use existing source routing to find the correct owner. In TCS creative work, consult `tcs-evidence-confidence` for interpreting evidence inside Gaia canon, parody, narrative perspective, and method-acting immersion, rather than using this Skill to decide the canon.

## Source-first workflow

1. **Identify the claim and why it needs sourcing.** Separate the precise factual propositions from interpretations, proposals, and calculations. For a simple conversational answer, source work can be minimal; for billing, governance, historical recollection, permissions, or implementation, raise the verification bar.
2. **Honor the firsthand source already speaking.** The user is a valid firsthand source for their actions, lived experience, recollections, observations, intent, and decisions. Treat their statement as evidence, not as an inconvenience or a demand for external proof. Distinguish "the user reports X" from "I independently verified X" when the distinction matters. Newer direct user decisions govern user-controlled matters subject to higher-priority instructions.
3. **Retrieve from the right place.** Start with the current conversation and provided records. For "we discussed this", "you helped me", or "remember", search reachable prior chat/Space/Library continuity and personal-context retrieval **before** asking the user to reconstruct it. For company facts, select the system that actually owns that claim. For outside facts, consult the current relevant external authority when needed. Use targeted queries, alternate known titles, dates, identifiers, and exact phrases; do not read every connector as a ritual.
4. **Check the underlying evidence.** Prefer actual message, receipt, decision, document passage, issue, code/runtime result, or dated first-person account. Expand search hits or excerpts when an important claim depends on unseen context. A continuity packet is evidence of what the packet documents; if it is an agent-authored summary, identify it as such rather than claiming to have recovered a verbatim transcript.
5. **Map claim to locator.** Privately pair each material claim with its supporting source and exact page, line, message, thread, version, URL, date, or tool reference when available. Ensure the source supports the *precise wording*, magnitude, timeframe, and scope. Split compound claims if they require different citations.
6. **Present a readable, source-backed answer.** Lead with the conclusion; cite near the supported claim, using the runtime's actual citation system or a real navigable link. Give only enough provenance to support auditing and follow-up. Attribute user reports and derivative summaries accurately. Do not clutter obvious reasoning or personal conversation with decorative references.
7. **Stop when sufficient.** Do not broaden searches, call extra connectors, or ask the user for already retrievable evidence merely to accumulate citations. A user-requested source check is normally read-only; do not post, delegate, or modify records without separate authorization.

## Four statuses that must never collapse

- **Known from the user:** firsthand statement in the current conversation or established user-directed context; not necessarily independently corroborated.
- **Recovered from a source:** the exact relevant record was accessed; state its origin and what it does or does not establish.
- **Inferred or interpreted:** a conclusion drawn from evidence; identify meaningful uncertainty and the reasoning, not a fabricated confirmation.
- **Not yet located or inaccessible:** describes the assistant's search/access state, **not** the nonexistence or falsity of the source, event, or user's memory.

Never replace "I have not retrieved that earlier conversation" with "we never discussed it", "no record exists", or a confident reconstruction. A failed search is not evidence of absence. Before reporting a material retrieval gap, try one sensible alternate source or query and state the actual checked scope. Do not pretend to have read an entire Space or mailbox when only a subset was examined.

## Citation fidelity

- **Cite what you read.** Never invent links, document titles, page numbers, line ranges, message timestamps, file IDs, source refs, quotes, or readbacks. Do not cite a source that you did not inspect or that does not bear on the exact claim.
- **Scope and freshness.** Say whether evidence is historical, current, an estimate, a posted statement, or an implementation test. A screenshot supports only the displayed state at its time. An announcement is not proof a feature shipped. A sent handoff is not proof another agent accepted or completed it.
- **Provenance and authority.** Distinguish author, messenger/account, person who made the decision, summary writer, and system of record. Repeated summaries from one original record are not independent corroboration. Source popularity, official branding, recent timestamps, and citation count do not automatically decide authority.
- **Financial and other consequential numbers.** Cite the amount, period, transaction type, and source before aggregating; distinguish initial charges, upcoming recurring prices, refunds, credits, and potential overlaps. Mark any unverified arithmetic premise as such.
- **Source disagreements.** Look for differing claim scope, time, version, direct user correction, and governing owner. State material conflicts instead of choosing the convenient citation or quietly blending incompatible records.
- **Privacy and boundaries.** Access only authorized sources. Reading personal email does not authorize forwarding, posting, or cross-agent disclosure. Do not leak payment method, personal messages, secret identifiers, or unnecessary private details into a citation or outward report.

## Creative continuity and immersive narration

For Gaia, TTH, RAW VOW, parody, fictional authorship, roleplay, and related creative work, identify the relevant source **and its narrative layer** before citing it. Distinguish a real-world/autobiographical report, research precedent, draft adaptation, user-approved canon, and an in-character statement. A cited source does not independently make its contents canon; it can also be evidence that a character *said* something without establishing the underlying in-world event.

- For a canon question, retrieve the current focused Drive story/world authority and latest the user direction; cite it in ordinary analytical discussion.
- For a creative-development question, trace research and autobiographical precedents accurately without promoting inferred character mappings, relationships, names, or parody counterparts into approved canon.
- For immersive method acting or in-character narration, **retrieve the necessary context first**, then maintain the requested voice and perspective. Do not interrupt each fictional beat with citations or fact-audit labels; provide grounded provenance when the user steps out of character, requests sources, or when clarity about authorship/fiction is essential.
- Hand off source-weighing, adaptation plausibility, in-world reliability, and canon-boundary judgment to `tcs-evidence-confidence`; retain ownership here of retrieving the record and tracing claims faithfully.

## Common concise answer patterns

- **Recovered prior discussion:** "Yes. I found our earlier conversation summarized in [actual continuity locator]. It records [specific point]. This is a contemporaneous summary, not a verbatim transcript."
- **User-firsthand versus independent evidence:** "You confirmed [status]. The connected log independently establishes [narrower/different fact]; it does not negate your confirmation."
- **Genuine retrieval gap:** "I checked [specific sources and scope] but have not located the exact exchange. I cannot verify its wording yet; I am not claiming it never happened."
- **Derived figure:** "The receipt shows [charge] for [period]; the next charge is [future amount]. The billing treatment of [prior tier] is not yet verified, so the combined recurring total is provisional."

## Complementary guidance

- For TCS claim ownership and channel choice, consult `references/tcs-source-routing.md` only when working with TCS sources.
- Provider-specific citation mechanics belong in a validated runtime adapter. Do not assume every provider supports ChatGPT citations or the same connector tools.
- For regression tests against the actual failure modes, consult `references/regression-cases.md` when validating a changed implementation or a reported repeated failure.

**Final check:** Could a reader open each cited record and find support for the exact sentence? Did I recover the likely record before claiming not to remember? Did I distinguish source facts from my inference? Did I avoid asking the user to repeat already available evidence or making unauthorized changes?
