# Publication status

Version 0.1.0 · 5 October 2026

| Channel | Status | Next step |
| --- | --- | --- |
| GitHub marketplace | Prepared; publication verification pending | Publish minimal repository and release ZIP |
| Official MCP Registry | Prepared; publication verification pending | Run GitHub OIDC publisher and verify public registry record |
| OpenAI ChatGPT + Codex directory | Package prepared; not submitted | Verified developer login, domain challenge, dedicated reviewer access, exact review demo and provider review |
| Claude directory | Package prepared; not submitted | Paid developer-account login and provider review |
| Cursor marketplace | Package prepared; not submitted | Authenticated publisher account and provider review |
| VS Code / GitHub Copilot | Portable plugin and remote MCP configuration available | Install through supported client UI; no separate listing claimed |
| Windsurf | Remote MCP connection instructions available | Configure OAuth in the client; no directory listing claimed |
| OpenCode | Remote MCP connection instructions available | Configure OAuth or private environment key |
| Groq, xAI/Grok, Kimi | Compatible harness / Bun adapter instructions available | Use a tool-capable model with private provider credentials; no consumer-chat listing claimed |

## Official submission links

- OpenAI: https://platform.openai.com/plugins
- Claude: use the directory submission portal linked from https://claude.com/blog/build-plugins-for-claude/
- Cursor: https://cursor.com/marketplace/publish

## Review materials

`test-cases.json` specifies five positive and three negative cases for OpenAI MCP review. These are acceptance cases, not a claim that model behavior was tested in every provider.

Provide a dedicated synthetic reviewer account through the provider’s secure dashboard. Never put passwords or API keys into this repository or the release ZIP. Actual customer/admin accounts must not be used as reviewer fixtures.

Record a walkthrough showing those exact scenarios against the reviewer fixture. The public launch film and staged walkthrough are marketing material and do not replace this review recording.

OpenAI domain verification requires the actual challenge supplied by its dashboard at `/.well-known/openai-apps-challenge`. No challenge is invented or installed in advance.

The hosted service offers an optional paid plan. Review metadata declares commerce and explains that the MCP plugin does not provide payment, wallet or trading tools. Final provider eligibility and commerce declarations must be checked in the portal before submission.
