# Publication status

Version 0.2.0 · 5 October 2026

| Channel | Status | Next step |
| --- | --- | --- |
| GitHub marketplace | Published | Release ZIP available; initial 0.1.0 remote installs verified in Codex and Claude Code |
| Official MCP Registry | Published, active | io.github.David-glitc/sitalk version 0.2.0 verified through the Registry API |
| OpenAI ChatGPT + Codex directory | Package prepared; not submitted | Verified developer login, domain challenge, dedicated reviewer access, exact review demo and provider review |
| Claude directory | Package prepared; not submitted | Paid developer-account login and provider review |
| Smithery | Publication instructions prepared; not submitted | Smithery publisher login and namespace; static capability card available |
| Cursor marketplace | Package prepared; not submitted | Authenticated publisher account and provider review |
| VS Code / GitHub Copilot | Portable plugin and remote MCP configuration available | Install through supported client UI; no separate listing claimed |
| Windsurf | Remote MCP connection instructions available | Configure OAuth in the client; no directory listing claimed |
| OpenCode | Remote MCP connection instructions available | Configure OAuth or private environment key |
| Groq, xAI/Grok, Kimi | Compatible harness / Bun adapter instructions available | Use a tool-capable model with private provider credentials; no consumer-chat listing claimed |

## Official submission links

- OpenAI: https://platform.openai.com/plugins
- Claude: https://claude.ai/directory/manage
- Cursor: https://cursor.com/marketplace/publish
- Smithery: https://smithery.ai/new

## Review materials

`test-cases.json` specifies five positive and three negative cases for OpenAI MCP review. These are acceptance cases, not a claim that model behavior was tested in every provider.

Provide a dedicated synthetic reviewer account through the provider’s secure dashboard. Never put passwords or API keys into this repository or the release ZIP. Actual customer/admin accounts must not be used as reviewer fixtures.

Record a walkthrough showing those exact scenarios against the reviewer fixture. The public launch film and staged walkthrough are marketing material and do not replace this review recording.

OpenAI domain verification requires the actual challenge supplied by its dashboard at `/.well-known/openai-apps-challenge`. No challenge is invented or installed in advance.

The hosted service offers an optional paid plan. Review metadata declares commerce and explains that the MCP plugin does not provide payment, wallet or trading tools. Final provider eligibility and commerce declarations must be checked in the portal before submission.

## Publication evidence

- Public marketplace: https://github.com/David-glitc/sitalk-plugins
- Release ZIP and checksum: https://github.com/David-glitc/sitalk-plugins/releases/tag/v0.2.0
- Official active registry record: https://registry.modelcontextprotocol.io/v0.1/servers/io.github.David-glitc%2Fsitalk/versions/0.2.0
- Initial version 0.1.0 passed native Claude Code strict validation and isolated public GitHub install checks. Version 0.2.0 has updated branding and an active official MCP Registry record; fresh native-client installation of 0.2.0 is not claimed.
- The first GitHub Actions job could not start because the GitHub account is locked due to a billing issue. This version was published successfully using the official native publisher locally. The OIDC workflow remains ready for future releases after Actions is enabled.
- Claude’s portal offers a plugin bundle or a connector-only submission. Submit the bundle with its declared connector; it is not necessary to submit the same bundle twice. Publisher login and review remain pending.

## Remote catalog support

The public capability card at https://sitalk.kierkegaard.space/.well-known/mcp/server-card.json is generated from the actual MCP tool definitions using an isolated in-memory account. It publishes schemas and authentication requirements only; it never contains customer context or credentials. This supports catalog indexing behind an OAuth wall without granting a catalog access to a customer account. Smithery publication itself remains pending authenticated publisher access. Smithery uses a gateway, so it is an optional distribution route, not required for direct Sitalk connections.

Current finalization guide: [Finish provider approval](APPROVAL.md).
