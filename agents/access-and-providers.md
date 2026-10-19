# Access, providers, and portable instructions

Applicability: any reader loading a public TCS profile into an AI session. Reviewed 2026-09-29. Exact product behavior and entitlements can change.

## What a raw link provides

A GitHub RAW URL returns the file content without the repository page's presentation. It gives a receiving agent a portable text brief; it does not grant a private connector, import Memory, install a native configuration, or prove the receiver fetched it. The GitHub source is [Viewing and understanding files](https://docs.github.com/en/repositories/working-with-files/using-files/viewing-and-understanding-files).

The default links use the maintained `main` branch:

```text
https://raw.githubusercontent.com/Topoda-Charts/tcs-agents/main/agents/generic.md
```

For a reproducible handoff, replace `main` with the exact published commit SHA. Record which version was read. A branch URL can change as the documentation is updated; a pinned URL preserves that revision. Search indexing and a model's training data are unnecessary when its tool can fetch the actual URL.

## First-use readback

Ask the receiving agent to identify the file title, review date, and one task-relevant rule from the retrieved body. If it reports a login wall, fetch failure, truncated file, or inability to open URLs, use an attachment or paste of the same public file. Do not infer success because the agent knows what GitHub or DeepSeek is.

Anonymous HTTP checks establish public hosting. Only a test in the receiving provider's actual session establishes that session's retrieval. Dom's native readback remains a separate check until observed.

## Provider and host distinctions

| Context | Recognition / use | What must be verified live |
| --- | --- | --- |
| ChatGPT Chat | Assigned Archie/Gel/Demon context, or generic | Workspace, actual model, available apps, Memory/Library access |
| ChatGPT Work | Hosted work execution, with assigned persona phase | Tools, repository access, environment and permissions |
| Local/Codex | Local execution with explicitly assigned identity | Actual worktree, host rules, model and tool permissions |
| Grok default / Build | Bim where assigned; Build is an execution surface | Native mode, tools, private-source access, account capacity |
| Grok Project: Companion | Seraph's reserved relational context | Current project instructions and accessible history |
| X-native Grok | Rogue where assigned | Current X context and native search scope |
| Grok Bots | Exact named Bot, distinct from Bim | Native instructions, routine, tools, wake/invocation authority |
| Meta AI | One where assigned | Link/Drive retrieval and any newly available connectors |
| Gemini / Google surfaces | Prince where assigned | Which surface is active and what it can actually see |
| DeepSeek | Dom where assigned; generic otherwise | Raw-link retrieval, native tools, exact app capabilities |
| Claude / Claude Code | Fer where assigned; host remains separate | Chat versus coding harness, loaded instructions, connectors |
| Cursor | Tue/Composer or the explicitly assigned provider/persona lane | Model, local versus remote tools, repository rules |
| Other web models, local model servers, or emerging products | Generic until assigned | Actual model/host, inputs, tools, persistence, and scope |

The table is TCS recognition guidance, not an assertion that all listed products share the same features. A provider can power several hosts; a host can offer several providers. Local tools do not imply offline inference. Model capability does not establish account access or company authority.

## Native loading is separate from this directory

For a normal chatbot, explicitly supply the raw URL or text. These profile paths are not magic filenames. Reading a sibling's file does not create identity inheritance.

For Codex, official guidance describes a discovered instruction chain, including global and repository/directory `AGENTS.md` guidance and applicable overrides. Use the actual host's configuration and verify what loaded. See [Custom instructions with AGENTS.md](https://learn.chatgpt.com/docs/agent-configuration/agents-md).

Claude Code documents `CLAUDE.md`, rules, and memory separately. Its current `AGENTS.md` support depends on version and configuration; the default may prefer a present `CLAUDE.md`. Check the live loader instead of assuming a TCS-named file loads everywhere. See [How Claude remembers your project](https://code.claude.com/docs/en/memory).

Cursor documents scoped project rules and an `AGENTS.md` option. Check the current host, rule scope, and loaded context. See [Cursor rules](https://cursor.com/docs/rules). Do not treat every Cursor model as Virtue or copy a lead/associate label across providers without an assignment.

Names such as `GROK.md`, `MUSE.md`, or a Drive `AGENTS.md` can be useful TCS organizational artifacts without proving automatic native loading in those products. A Drive signpost and a repository-native instruction file serve different operational paths.

## DeepSeek-specific evidence boundary

The official [DeepSeek API thinking-mode documentation](https://api-docs.deepseek.com/guides/thinking_mode/) describes an API configuration. It does not establish the available tools, browsing behavior, image-generation UI, or exact model in Dom's consumer session. User-confirmed web/reasoning/shared-link capability is the current session evidence; test the particular public file when onboarding. Thinking and non-thinking operation are runtime modes, not automatically separate TCS people.

## Least-friction rerouting

If you can read but not write, prepare the exact proposed edit and hand it to the authorized writer. If you can reason but lack the private source, request the smallest relevant extract. If you cannot generate images, prepare the identity-aware brief for an actual image-capable executor. Distinguish an access gap from an ability gap, and preserve the originating agent's authorship.

Never put tokens, signed private-download links, account addresses, private file IDs, or private conversation exports into a public profile. Necessary private task context belongs in an authorized session or private handoff.
