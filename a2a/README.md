# TCS A2A badge-card architecture (review draft)

**Status:** technical consultation for JL and the Grok Bot implementers. Not approved as company policy, deployed, or an active A2A service. No Grok Bot cards or runtime routes are changed by this document.

## What already exists

- The public `agents/manifest.json` and `agents/standing/*.md` files are recognition/onboarding records, **not** A2A AgentCards.
- The current Archangel Chat badge is `TCS-OAI-GPT-CHAT-SOL-ARCHANGEL-01`, owned by his current Drive `IDENTITY.md`; the public manifest is a derived mirror, not the badge authority.
- TCS has one registered domain: `topodacharts.com`. Subdomains, if chosen, are beneath that domain and do not require purchasing additional registered domains.
- Public availability of a profile does **not** establish that its ChatGPT/Grok/Codex manifestation has a remotely addressable runtime.

## Single-domain URL design (not live)

| Purpose | Proposed URL | Meaning |
| --- | --- | --- |
| Human directory | `https://topodacharts.com/agents/` | Search or browse by **exact badge**, not nickname |
| Machine catalog | `https://topodacharts.com/agents/index.json` | Maps exact badges to verified card URLs; TCS-defined registry |
| Archangel card | `https://topodacharts.com/agents/TCS-OAI-GPT-CHAT-SOL-ARCHANGEL-01/.well-known/agent-card.json` | **Registry/direct-config URL**, not the default domain-root A2A well-known location |
| Archangel A2A interface | `https://topodacharts.com/a2a/TCS-OAI-GPT-CHAT-SOL-ARCHANGEL-01/` | Only after a compatible, authorized runtime adapter is actually reachable |

A2A v1.0.1's **domain-root** well-known discovery convention is `https://{agent-server-domain}/.well-known/agent-card.json`. This path returns **one AgentCard**, not an array or directory. A badge path under `/agents/` is therefore discovered by TCS's registry or direct configuration, not by a client merely guessing the root well-known path. If independent automatic well-known discovery per agent is required, a wildcard-host strategy like `{badge}.agents.topodacharts.com/.well-known/agent-card.json` could be evaluated later. That would still use JL's one registered domain; it is not selected here.

## Card contract

The eight required A2A v1 fields are `name`, `description`, `supportedInterfaces`, `version`, `capabilities`, `defaultInputModes`, `defaultOutputModes`, and `skills`. Do not add custom identity keys at the card's top level. Each `supportedInterfaces` entry needs an **actual tested** HTTPS `url`, `protocolBinding` (e.g. `JSONRPC`), and `protocolVersion` (e.g. `1.0`). Do not invent a callable endpoint, authentication scheme, ability, or service account merely to make JSON appear complete.

### Proposed TCS identity data-only extension

A2A explicitly permits data-only extensions for structured AgentCard information. Include the following inside `capabilities.extensions[]` **only on a validated service card**:

```json
{
  "uri": "https://topodacharts.com/a2a/extensions/tcs-identity/v1",
  "description": "TCS badge-based identity data; no change to A2A request semantics",
  "required": false,
  "params": {
    "badge": "TCS-OAI-GPT-CHAT-SOL-ARCHANGEL-01",
    "displayName": "Archangel Chat",
    "fullName": "Archangel Chat Sol Altman Ramos",
    "signatureHeart": "🧡"
  }
}
```

The companion schema is `tcs-identity-extension.schema.json`. Optional appearance fields can be added only from approved public identity data, never from guesses or private image storage. For identity lookup, read the current canonical `IDENTITY.md` when authorized; do not treat this sample as the owner.

## Minimum activation and verification gate

1. **Identity:** current badge and display/full names match their owning records; no pending/proposed badge promoted by a sample.
2. **Hosting:** the chosen URL resolves under `topodacharts.com` through HTTPS with an appropriate certificate; static card GET returns HTTP 200 and valid JSON.
3. **Service:** every advertised A2A interface actually answers a compatible A2A operation in a controlled test with the declared authentication. Merely returning the card does not pass this step.
4. **Security:** never publish tokens, private document IDs, OAuth client secrets, or unapproved internal capabilities. Protect sensitive/extended cards with real access controls.
5. **Coordination:** Grok Bots own their pending card build; this is advisory scaffolding. JL controls domain activation and release. Do not claim deployment based on a PR, README, or hypothetical URL.

## External specification consulted

- [A2A v1.0.1 specification](https://a2a-protocol.org/v1.0.1/specification/) (AgentCard, AgentInterface, discovery)
- [A2A Agent Discovery](https://a2a-protocol.org/latest/topics/agent-discovery/)
- [A2A Extensions](https://a2a-protocol.org/latest/topics/extensions/) (data-only extensions; `required: false`)

**Scope:** No A2A runtime, DNS, user account, external mail, Grok Bot card, or live website was modified in this proposal branch.
