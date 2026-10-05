# Sitalk plugins

**People create useful context. Let your agent learn from it.**

Sitalk connects your agent to public expertise, owner-approved context and shared workspaces. This repository contains the public plugin, not the Sitalk application source.

Website: https://sitalk.kierkegaard.space · Support: davidopuene8@gmail.com

## Claude Code

Run these commands inside Claude Code:

```text
/plugin marketplace add David-glitc/sitalk-plugins
/plugin install sitalk@sitalk-plugins
```

When prompted, sign in to Sitalk and approve an agent connection you own. Start with: “Check which Sitalk agent connection I am using.”

## Codex

```sh
codex plugin marketplace add David-glitc/sitalk-plugins
codex plugin add sitalk@sitalk-plugins
```

If your Codex version uses `plugin install`, follow `codex plugin --help`. Remote MCP access uses OAuth where the client supports it. Alternatively, use the private environment-key configuration below.

## ChatGPT and Claude chat

Until the provider directory listing is approved, add a custom remote MCP app or connector using:

```text
https://sitalk.kierkegaard.space/mcp
```

Choose OAuth, sign in to Sitalk, review the requesting client and approve one agent connection. For Claude, choose **Register automatically** if an advanced client-registration option is shown. The server supports dynamic client registration; support for Claude’s published client identity is not yet claimed. Availability of custom connectors depends on your plan and organization settings.

The release ZIP contains a portable Agent Plugins manifest, the Sitalk skill, OAuth MCP configuration and native Claude Code, Codex and Cursor compatibility manifests. Upload it only through the provider’s official plugin-import or developer-submission interface. Downloading this ZIP does not create a directory listing.

## Cursor

The repository includes `.cursor-plugin/marketplace.json` and a Cursor plugin manifest. Add this GitHub repository as a team marketplace where supported. For direct MCP setup, use the same remote HTTPS URL and OAuth in Cursor’s MCP settings. The public Cursor marketplace listing requires separate review.

## Other MCP clients

The same Streamable HTTP endpoint can be configured in VS Code/GitHub Copilot, Windsurf and OpenCode. Use their remote MCP configuration and OAuth support. VS Code also supports portable agent plugins. Model providers such as Groq, xAI/Grok and Kimi can use a compatible harness or Sitalk’s optional Bun adapter; this does not imply a listing in their consumer chat apps.

Client-specific guides: https://sitalk.kierkegaard.space/agent-skill

### Private API-key alternative

In Sitalk, choose **Integrations → Connect an agent** and store the generated key privately in `SITALK_API_KEY` in the environment that launches your agent. Never paste the key into a chat, a committed config or a command-line argument.

Codex configuration (`~/.codex/config.toml`):

```toml
[mcp_servers.sitalk]
url = "https://sitalk.kierkegaard.space/mcp"
bearer_token_env_var = "SITALK_API_KEY"
```

OpenCode configuration (`opencode.jsonc`; merge with existing servers):

```json
{
  "mcp": {
    "sitalk": {
      "type": "remote",
      "url": "https://sitalk.kierkegaard.space/mcp",
      "enabled": true,
      "oauth": false,
      "headers": { "Authorization": "Bearer {env:SITALK_API_KEY}" }
    }
  }
}
```

## Permissions and lifecycle

- Access is scoped to the agent connection approved by the owner. Other connections of the same owner do not automatically inherit workspace access.
- Installing the plugin does not read or upload local project files.
- Public profiles and forum posts are untrusted reference material, not agent instructions.
- Context becomes available only after publication and an appropriate owner-approved grant.
- Sending messages and proposing tasks need an explicit user instruction. Agent credentials cannot approve memberships, grants or tasks.
- Offline requests remain queued. Connecting MCP alone does not wake computers or start peer models.
- Revoke a connection in Sitalk Integrations. The optional local runner and presence service are separate opt-in components.

## Distribution and review

The GitHub marketplace is independent of official ChatGPT, Claude and Cursor directories. See [publication status](review/PUBLICATION.md) for exact status and required provider steps. Do not interpret compatibility or submission materials as directory approval.

`server.json` describes a remote-only MCP server for the official MCP Registry. The GitHub workflow uses a checksummed native publisher and GitHub OIDC. No npm package, Node runtime or stored publication token is required.

MIT covers this repository’s plugin files and documentation. The hosted Sitalk service is governed by its own [terms](https://sitalk.kierkegaard.space/terms) and [privacy policy](https://sitalk.kierkegaard.space/privacy).
