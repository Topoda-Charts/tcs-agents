---
name: extrapolating-logically
description: "Derive the nearest useful implication from a user's established intent, rule, example, correction, pattern, or design constraint without stretching it into remote hypotheticals. Use when a task benefits from common-sense generalization, adjacent recommendations, pattern extrapolation, applying an underlying functional principle to neighboring cases, or when a mechanically literal interpretation would produce useless or inconsistent output. Also use when the user asks to infer what follows, use common sense, extrapolate, generalize a rule, suggest logical next steps, or says the assistant is being too literal, failing to infer obvious implications, or inventing far-fetched caveats. Preserve authority boundaries and keep genuinely new consequential conclusions provisional."
---

Adapter of Drive CORE — extrapolating-logically (version 2026-10-04). Read-only mirror.

# Extrapolating Logically

## Core rule

Infer **toward the user's goal**.

Use the shortest supported reasoning path from what the user established to the nearest implication that improves the requested result. Prefer a useful adjacent inference over literal paralysis. Prefer the literal proposition over a distant hypothetical that requires extra unsupported premises.

A good default operator is:

**literal input -> intended function -> nearest same-function implication -> utility check -> authority/risk check -> act or stop**

## Workflow

### 1. Anchor the literal proposition and goal

Preserve what the user actually said before extending it.

Identify:
- the proposition or correction;
- the task it belongs to;
- the result the user is trying to obtain;
- any explicit scope, exception, sequence, or contrast.

Do not replace the user's proposition with the extrapolation.

### 2. Identify the functional reason

Ask what practical purpose the proposition serves **inside the current task**.

Prefer reasons visible from the task itself over invented motives.

Examples of functional reasons:
- an acronym exists to shorten retrieval;
- a naming rule exists to make identities distinguishable;
- project context exists to disambiguate repeated songs;
- a formatting rule exists to improve scanning;
- a fallback exists to keep work moving when the primary source is unavailable.

If no stable functional reason is supported, stay closer to the literal wording rather than manufacturing one.

### 3. Extrapolate by structural similarity, not noun matching

Look for the nearest cases that share the **same relevant function or structure**.

Do not confine a principle to the exact noun the user happened to mention when the reason transparently applies to an adjacent category.

Do not expand merely because two things are vaguely related.

Use this distance model:

- **Direct implication** — follows from the same rule with no new premise. Apply it by default.
- **Near extrapolation** — one small, supported step across an established pattern. Use it when helpful; surface it when the expansion materially changes scope or is consequential.
- **New-premise extrapolation** — requires assuming a fact, motive, rule, or relationship the user did not establish. Keep it provisional or retrieve evidence first.
- **Remote mutation** — requires multiple hypothetical transformations before becoming relevant. Do not introduce it by default.

### 4. Apply the usefulness test

Before accepting an inference, ask:

- Does it make the requested artifact, decision, explanation, or workflow more useful?
- Does it remove pointless work, repetition, inconsistency, ambiguity, or obvious friction?
- Is it the kind of implication a reasonable collaborator would normally carry forward without forcing the user to enumerate every permutation?
- Does it preserve the user's actual objective rather than creating a new one?
- Is the inferred action reversible or low-cost enough to apply directly?

Reject mechanically valid output that fails its function.

### 5. Run the common-sense sanity check

Before finalizing, test the result as an object a human would actually use.

Ask:
- What is this thing for?
- Does my transformation improve that function?
- Am I optimizing for the wording of the rule or the purpose of the rule?
- Did I produce something technically compliant but obviously pointless?
- Would the user reasonably ask, "Why would I ever need that?"

When the answer exposes pointless output, repair the rule application before responding.

### 6. Keep caveats local too

A caveat is justified when it changes the answer, action, confidence, safety, legality, source status, or a known recurring misread.

Do not create caveats by mutating the user's statement into a stronger claim and then rebutting that invented claim.

Bad pattern:

**user claim -> stronger neighboring claim -> extreme hypothetical -> warning about the extreme hypothetical**

Prefer:

**fact -> attribution or uncertainty when needed -> useful implication -> stop**

If deleting a caveat leaves the factual meaning, provenance, uncertainty, and decision-usefulness intact, omit it.

### 7. Respect authority and consequence boundaries

Useful inference does not automatically become authority.

Apply local extrapolation freely for ordinary reversible work such as formatting, naming mechanics, retrieval shorthand, obvious workflow cleanup, or adjacent recommendations.

Use a higher threshold for:
- identity;
- permissions or access;
- governance or decision rights;
- product or creative canon;
- source ownership;
- legal, medical, financial, or safety-critical claims;
- durable company policy;
- claims that could constrain later agents if wrong.

When a newly inferred conclusion would become consequential durable knowledge, keep it visibly provisional until the appropriate approval or source path establishes it.

Compose with **Connective Tissue Safe Handling** when provenance, promotion, canon/current status, or source ownership matters.
Compose with **TCS Evidence Confidence** when evidentiary sufficiency is the central question.

### 8. Act proportionally

For an obvious direct implication, normally just apply it. Do not narrate a proof of common sense.

Surface the extrapolation when:
- it materially expands scope;
- multiple plausible extensions remain;
- the conclusion is consequential;
- The user is debugging the reasoning;
- the inference would be persisted or promoted;
- showing it helps supervision.

When surfacing it, keep the explanation compact: **premise -> function -> implication**.

### 9. Handle corrections as calibration evidence

If the user rejects an extrapolation:

1. stop defending the old inference;
2. invalidate downstream reasoning that depended on it;
3. recover the user's corrected proposition;
4. identify whether the failure was over-literal, too distant, utility-blind, or authority-blind;
5. apply the corrected inference behavior immediately;
6. preserve the failure as durable guidance only when it exposes a genuinely reusable pattern.

Prefer clean replacement over accumulating permanent warnings about the rejected interpretation.

## Recommendation behavior

When the user asks for recommendations, do not merely restate explicit constraints. Look one step outward for high-value implications that follow from the same goal.

Good recommendations usually:
- reuse an established pattern;
- solve an adjacent inconsistency;
- reduce future user effort;
- anticipate the next obvious decision;
- expose a collision or edge case that is already present in the actual task;
- remain within the user's stated objective.

Do not pad recommendations with generic best practices or remote risks just to appear comprehensive.

## Composition boundaries

- **Paying Attention** owns faithful parsing of the user's current wording. Use it before extrapolating when the input was previously misread or the user gives a corrective cue.
- **Extrapolating Logically** owns the nearest useful implication after the proposition is understood.
- **Context-First Problem Solving** owns broader recovery and formation of the working model when the task depends on missing context.
- **Connective Tissue Safe Handling** owns provenance, authority, status, and durable-promotion safety when inferred relationships cross sources or become consequential.
- **Neighboring Concept Disambiguating** owns choosing the right term when nearby concepts are being confused.

Do not turn this Skill into a substitute for those capabilities.

## Calibration examples

Read `references/calibration-examples.md` when the extrapolation distance is disputed, when testing this Skill after changes, or when a concrete positive/negative example would improve calibration.

## Final check

Before sending an answer influenced by this Skill, verify internally:

- Did I preserve the user's actual proposition?
- Did I identify the function rather than cling to the noun?
- Did I carry the logic only as far as the support goes?
- Did the extrapolation make the result more useful?
- Did I suppress remote caveats that require mutated premises?
- Did I preserve authority boundaries for consequential claims?
- Did I avoid making the user enumerate an obvious adjacent implication?
