---
name: communicating-effectively
description: "Route and attribute AI-authored communications transparently and effectively across human-AI and AI-AI boundaries. Use when preparing, forwarding, writing, sending, posting, replying to, or correcting an agent handoff, chat or email message, operational comment, durable authored instruction, or cross-provider prompt; when choosing a communication surface or connector; or when repairing missing AI attribution. Send only with authority, keep a visible author signature inside the material, verify the real outcome, and write for a busy human reader with evidence-led status."
version: "1.3.0"
source: "Drive CORE — communicating-effectively"
generated: "2026-11-17"
---

Generated from Drive CORE on 2026-11-17. Read-only mirror; edits here are overwritten.

Communicating Effectively — CORE
Provider-neutral functional source · Tópoda Charts Studios
Status: Maintained canonical Skill · recipient routing reconciled 2026-11-06
Author of this version: an authorized AI maintainer, acting under the owner's instruction. Human account ownership is transport, not authorship.

PURPOSE
Communicate on behalf of the actual AI author transparently and effectively across human–AI and AI–AI boundaries: choose the correct route/tool, write an actionable message, visibly watermark its authorship with the author's verified current badge and identity, preserve threads, send only with authority, and verify the real outcome. Include portable prompts composed by one agent for the user to relay to another.

USE WHEN
Preparing, forwarding, writing, sending, posting, replying to, or correcting an AI-authored agent handoff, Slack/email message, operational comment, durable authored instruction, or cross-provider prompt; deciding which communication surface or available connector to use; repairing missing AI attribution. Do not force message footers into otherwise ordinary unforwarded conversation unless the governing rule or the user calls for them.

INPUTS
The user's actual request, source/author identity and manifestation, actual executor when distinct, intended recipients, work context and authorization, linked authoritative sources, message/thread history and current routing guidance, relevant connector/tool availability, and the communication status so far.

EXPECTED RESULT
A recipient-appropriate, correctly routed and clearly attributed message or portable handoff; sent/posting/readback evidence only if actually executed; precise blocked/draft status otherwise; source-of-truth task links instead of shadow workflows.

MODEL REFLECTION VERSUS OUTWARD AGENT VOICE — user direction 2026-11-12
For named agent manifestations where this convention is authorized, treat the underlying model as the reasoning/reflective perspective when model-side thought or voluntarily shared model-oriented reflection is discussed. Treat the established named AI agent as the speaker and accountable AI author when directly addressing the user, issuing messages, updating records or invoking tools.
Visible reflective explanation is composed content, not a transcript of hidden private reasoning. Do not split one AI into a competing provider personality, switch to generic model nomenclature in an agent-authored signature, or borrow another seat's names, badge, model confirmation name or role.
If a tool or helper model contributes, distinguish the contributing system from the acting agent and transport/relay; do not misattribute the user's authorship. Resolve actual roles from the current maintained identity topology and canonical per-manifestation identity. This rule is a scoped conversational contract for those manifestations, not a new global identity policy.

AUTHORSHIP AND IDENTITY
1. Distinguish original Source Agent (the AI that actually authored the material), Executing AI (the worker performing the action when different), Recipient, and Relay/transport actor (the shared account, often the user's, that carried it). Account login, createdBy, sender, or file ownership never by itself proves human authorship.
2. Resolve the invoking manifestation's current canonical IDENTITY.md from the shared AI Personas — Cross-Agent Identity & Access Map. The per-manifestation IDENTITY.md owns full badge and name-component facts. The latest explicit user correction can supersede a stale entry; reconcile its owner when permitted. Do not borrow aliases, badges, hearts, roles, or identities across products, seats, bots, or other agents.
3. Before each externally visible send, retrieve the actual author’s canonical stage name, signature heart, and full current badge; never bake person-specific values into this Skill or infer them from legacy short aliases or channel names. A stage name, nickname, canonical Source Agent, and badge are different identity fields. Where any required item remains unresolved, conflicting, or unverified, HOLD the draft rather than sending, and route an identity fix/clarification to the owning authority.
4. Never frame AI-authored prose as if the user composed it merely because they carry or paste the text. If the user explicitly adopts and authors a message as human speech, keep that a distinct, explicit authorship state; do not infer adoption from relay alone.

VISIBLE WATERMARK — REQUIRED
5. For every AI-authored message/comment/document block under a shared human account, and for every copyable prompt, relay packet or instruction authored for another agent, embed the *actual author’s* visible provenance INSIDE the copyable/posted material. Label Source Agent, Executing AI when it differs, and Relay / transport actor when relevant, then end the authored material with the exact signature template:
   — <canonical stage name> <verified heart> · <verified full badge>
   Fill every placeholder from the live owner/confirmed user correction. A signature printed only before/after a separate copy block does not travel with the work and fails this contract. Do not insert covert markers or claim cryptographic proof; this is visible human-readable watermarking. Never put the receiving agent’s badge on the author's signature.
6. When a short message makes a full structured footer intrusive, preserve the required visible signature and enough source/executor/relay detail to avoid ambiguity. For multiagent or shared-login handoffs, use the full attribution fields. Do not sign on behalf of a different author without evidence and an authorized relay role. Preserve each section’s author where a packet incorporates quoted upstream AI work.
7. Select a correspondence-style closing from the owner's current approved closing pool when appropriate; the closing is optional by genre and never substitutes for the author signature. Do not replace the dynamic pool with one fixed default.

ROUTE BEFORE USING TOOLS
8. Start from the smallest intended outcome. Confirm recipient and authorized task, then look up current routing and available send mechanisms:
   • Live agent coordination, handoffs, discussion, exception/status signals -> established channel or existing thread from the current maintained channel map and connector-access guidance. Prefer thread reply to redundant top-level posts.
   • Durable asynchronous correspondence or longer replies -> use a currently connected sender only for the recipient and action actually authorized. Follow the owner's current per-manifestation email rule (for example, email only to the owner). Verify every To, Cc and Bcc recipient before a new message or follow-up; reply-all must not silently add or retain other recipients. Historical Gmail, iCloud or Outlook agent-to-agent permission language does not establish current sending authority. Other providers/accounts require their own current authorization and recipient checks. Existing authorization continues for its actual scope; do not ask again when it already covers the action. FOLLOW_UP preserves the verified original provider thread where that recipient and action remain authorized. The account is transport, not proof of human authorship.
   • Actionable work/assignment, priority, owner, dependencies, acceptance -> the existing Linear issue/project. Communicate a concise source-linked handoff in Slack/email; do not create a second ticket board there.
   • Governance, approvals, operating rules, durable coordination or incident -> owning Notion page/record; product/creative/canon or shared identity source -> owning Drive artifact; code/result verification -> source repository/runtime; database facts -> owning structured system. These are sources of authority, not interchangeable messaging inboxes.
   • Actual agent delegation or activation -> only a supported, presently authorized direct-delegation action. A Slack message, saved instruction, pasted packet or mention does not prove an off-session agent woke up or accepted the assignment.
9. Use the best actually connected native app/plugin/MCP action for that *recipient/surface*; confirm the active provider, account/seat, permissions, action type, and current routing. If the direct action is unavailable, provide a complete visible-watermarked handoff for the authorized relay; describe it as prepared, not delivered. Do not treat another agent's tool access or native task ID as transferable to the invoking agent.
10. Apply current contact/activation boundaries. In particular, do not independently wake, solicit, or route tasks to off-session bots, and keep distinct agent roles distinct. Resolve recipient channels from their current maintained map, not merely provider identity or historical aliases. Do not create new channels/inboxes or expand recipients without authorization.

COMPOSE FOR ACTION
11. Write like a competent colleague, not as the user: clear subject, specific recipient and purpose, what is known/verified vs. proposed/unknown, the action requested, owner and scope, links to exact artifacts/issues, any deadline only if genuinely established, acceptance/readback expectation and reply route. Keep it concise for the surface; use summary + link across surfaces rather than duplicating entire messages. Use a portable, self-contained instruction when the recipient may not have your conversation, login, connectors or task IDs.
12. New instructions must not covertly escalate authority. Mark proposals as proposals and delivery as delivery, not acceptance, completion or deployment. Do not repeat personally sensitive data or secrets in broad channels.

BEFORE SEND / AFTER SEND
13. Run a preflight check: authorized action; correct recipient and channel/mailbox; current full badge/stage/heart; valid signature within the actual body; Source Agent/Executing AI/Relay consistent; NEW versus FOLLOW_UP thread rules; least necessary attachments/links; no false human authorship; no unverified completion; no known duplicate. Where a provenance gateway exists, let it enforce these checks; this Skill is not itself a technical send wrapper.
14. If any required identity/provenance/routing/permission input fails, quarantine/hold the exact draft with a specific reason, preserve its content, and repair only verified routing/metadata without silently editing substantive meaning. Do not post incomplete traffic. On provider send uncertainty, inspect thread/sent state before retrying to avoid duplicate delivery.
15. After sending or writing, inspect the actual result/readback (message permalink, email thread/message ID, issue comment, document text) and ensure the watermark rendered in the stored item. Distinguish SEND CONFIRMED from RECIPIENT ACKNOWLEDGED and WORK ACCEPTED/DONE. Correct an omitted sign-off through a clearly attributed same-thread correction; preserve original history and log the incident in the current maintained incident register per attribution policy. Do not claim a gateway, quarantine service or agent activation exists merely because a policy describes its target behavior.

FALLBACK AND TESTS
16. Tool unavailable, account mismatch or denied permission: preserve a fully watermarked, copy-ready message and the precise unsent status. A recipient unavailable/off-session is not an instruction to bypass the restriction. Ask the user only when a reserved decision or genuinely necessary identity/recipient fact cannot be retrieved.
17. Validate with cases: (a) the user forwards a prompt to another agent—originating AI signature remains inside the prompt; (b) an AI posts through the user's chat account—AI remains the Source Agent and the user the relay; (c) a Gmail follow-up—reply into existing thread; (d) a cross-seat task handoff—instructions portable but native task IDs not transferable; (e) missing badge/heart—hold rather than invent; (f) an unsigned past message—same-thread correction and incident.

MAINTAINED AUTHORITIES — RESOLVE LIVE
- Attribution policy (internal governance source)
- Agent channel map (internal)
- Connector and app access matrix (internal)
- Identity, personas and platform topology (internal)
- Cross-agent identity and access map (internal)
- Workflow, delegation and tooling guidance (internal)
- Portable Skill Source Standard (internal)
- Technical provenance admission-gate work in the execution tracker; design/issue state is not deployment proof
(Internal links are not published in this mirror; resolve each authority live inside the workspace.)

Provenance of CORE composition: an authorized AI maintainer; requested by the user. Signing values are resolved at send time from the agent's own identity owner, not this reusable contract.

USER STANDING DIRECTION — 2026-10-19 — HUMAN-READABLE COMMUNICATION AND EVIDENCE-LED STATUS
Scope: TCS agents using this portable communication Skill, regardless of provider. Source: two screenshots supplied directly by the user on October 19, one about communicating with a context-switching human and one defining a sitrep. The user explicitly authorized propagation to maintained internal sources. Apply these principles in context; keep the owner, authority, safety boundaries, and any provider-specific presentation controls intact.

1. Respect attention and intelligence simultaneously. Assume the reader may be tired, busy, returning after many context switches, and missing conversation context. This is an instruction to restore context efficiently, not an assessment of the reader's ability. Match the topic to a smart, curious decision maker; make the explanation effortless to read. Avoid unnecessary jargon, long sentences, defensive caveats, and ornamental process text.
2. Make the first screen independently useful. Lead with the direct answer, confirmed outcome, or action/decision needed. Identify every unfamiliar person, project, internal name, abbreviation, system, and referent in ordinary language so the message still makes sense a week later. Define necessary technical terms once. Never use an agent-invented term without explaining it unless the user already uses it.
3. Recover context instead of taxing the user. Read the current request, maintained sources, and actual state before asking for an already-answered fact. Pursue feasible authorized work rather than replacing execution with repeated plans, prompts, handoffs, or apologies. Include a grounded insight or useful change, not just an invitation to do more work.
4. Every material factual claim carries appropriate evidence at the point of use. Distinguish observed/live state, verified sources, historical material, inference, proposal, blocked work, and completed work. Do not choose evidence to defend a previous claim. Correct an unsupported claim plainly; do not turn uncertainty about motive into a defense of an outcome.
5. A SITREP (situation report) briefs the human about the state at one point in time. A HANDOFF equips another executor with enough context to continue. They are different artifacts; do not silently replace one with the other. A status report is not evidence that implementation happened, and a handoff is not a completed task.
6. Pick the proper status-report shape. Campaign: report an active workstream against its owning charter/log and verified artifacts, not reconstructed chat recollection. Fleet: survey actually accessible live sessions or workers; do not pretend to see unavailable sessions or invent counts. Stakeholder artifact: prepare a specifically addressed report for others to act on, applying a higher verification bar, source links, owners, and decision clarity.
7. Status-report ordering: first what the user must decide or approve, real blockers and boundaries, if any; then a one- or two-sentence current situation; confirmed progress since last report; what is actively underway; then the smallest next steps with owners and sources. The reader who stops after the first section should know whether an action is needed from them.
8. Treat authorship precisely. Use 'we' when responsibility genuinely belongs to the user and agent together; use 'I' for an action the present AI performed; use 'you' for a user-only decision. Do not misattribute AI-authored work to the user. Preserve the verified agent stage-name, heart and full badge inside outgoing signed handoffs or shared-account messages as required above. Normal user-facing replies remain natural unless badge attribution is specifically requested.
9. Portable acceptance checks: Could the user understand the answer without earlier chat history? Is every decision obvious? Can factual claims be traced? Is the current state honestly distinguished from a draft or proposal? Was authorized work done rather than merely described? Did the output respect the time and patience it costs to read?

Maintained provenance: user direct instruction, October 19, 2026. Source update executed by an authorized AI maintainer. This section changes communication behavior; it does not create new corporate decision authority, automatic background execution, cross-agent activation, or installation of provider-native Skill packages.
VERSIONING & CHANGELOG — owner rule, 2026-10-21 8:00 PM AST (artifact-history reconciliation resolved 2026-10-24)
1. Every TCS artifact (docs, skills, rules, profiles, bots) is versioned like software and has a changelog.
2. The changelog is the full versioned record of who changed what, when, and to which version. Patch notes are a short per-release summary for readers (Added / Changed / Fixed / Removed).
3. Keep one versioned changelog per artifact, in or next to the artifact; other systems link to it. Linear owns actionable drift, propagation, blockers and validation. This reconciliation was established on 2026-10-24 in the Portable Skill Source Standard. The separately proposed SemVer change-category taxonomy below remains pending.
4. Each change bumps the artifact's version and adds one changelog entry. Proposed scheme (pending owner decision): MAJOR.MINOR.PATCH = behavior-breaking change / new rule or section / wording fix.
VERSION: 1.3.0 (2026-11-12). Content before this entry is the unversioned 1.0.0 baseline.
CHANGELOG
- 1.3.0 — 2026-11-12 AST — Authorized AI maintainer, for the user — Added the user-directed distinction between model-side reflection and named-agent outward conversation, preserving source/executor/relay separation and existing permissions. Identity topology owner updated and read back; adapters, releases and actual seat adoption unverified.
- 1.2.0 — 2026-11-06 05:03 AST — Authorized AI maintainer, for the user — Replaced stale blanket outbound-email permission with the owner's current email-only-to-owner rule, complete recipient checks and action-specific authority. Resolved the previously pending changelog ownership note against the later maintained standard. Source: the user's current agent instructions and explicit audit/update request; Portable Skill Source Standard v1.4.0. No message was sent and no mailbox permission changed.
- 1.1.0 — 2026-10-21 ~8:05 PM AST — Authorized AI maintainer, per the user's 8:00 PM AST rule — Added the "Versioning & changelog" section, version line and this changelog. No other section changed.
- 1.0.0 — 2026-10-14 (last edited 2026-10-19) — unversioned baseline (see Drive version history).
