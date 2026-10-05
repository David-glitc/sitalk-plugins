# Finish Sitalk provider approval

Checked against official provider documentation on 5 October 2026.

The GitHub package and official MCP Registry listing are published. This does **not** mean ChatGPT, Claude or Cursor has approved a directory listing.

## ChatGPT and Codex

Portal: https://platform.openai.com/plugins
Official guide: https://developers.openai.com/plugins/deploy/submission

1. Select the publishing organization/project and complete individual or business identity verification. Organization owners can submit; other members need Apps Management Write.
2. Upload https://sitalk.kierkegaard.space/plugins/sitalk-plugin.zip (version 0.2.0). Select the verified publishing identity.
3. In **MCPs → Connect**, use `https://sitalk.kierkegaard.space/mcp` and OAuth. Copy the exact domain challenge token and its required host from the portal. Send the token to your implementation agent so it can deploy a plain-text file at `/.well-known/openai-apps-challenge`, then select **Verify Domain**. A GitHub token, API key or DNS record cannot replace this challenge.
4. Authorize the reviewer’s Sitalk agent connection and complete the production MCP tool scan. Resolve every required scan finding and wait for bundled skill scans to finish.
5. Complete listing, privacy, terms, support, commerce declarations, availability, release notes and review fields. Public support email: `davidopuene8@gmail.com`.
6. Supply a dedicated synthetic reviewer account using the portal’s secure credential fields. It must be able to sign in without SMS/email verification or MFA challenges during review. Verify its email beforehand. Never use the owner/admin account or include passwords in a ZIP or repository.
7. Use `review/test-cases.json`: exactly five positive cases and three negative cases. Record a genuine acceptance walkthrough on the reviewer fixture. The launch video is marketing material and does not replace this recording.
8. Submit for review. Resolve feedback in the dashboard. **After approval, select Publish** when ready; approval alone does not publish it.

Sitalk’s optional Plus checkout lives on the website. The plugin provides no wallet, payment, purchase or trading tool. Declare the website’s optional paid service truthfully; the provider decides eligibility.

## Claude

Portal: https://claude.ai/directory/manage
Official guide: https://claude.com/blog/build-plugins-for-claude/

Use a paid Claude developer account. Submit the **plugin bundle** from https://github.com/David-glitc/sitalk-plugins with its declared remote MCP connector. The portal also supports a connector-only submission; these are alternative submission paths, not a requirement to submit the same bundle twice. Provide OAuth/reviewer details and complete the portal’s scans. Track feedback, then publish after approval.

## Cursor

Portal: https://cursor.com/marketplace/publish
Official reference: https://cursor.com/docs/reference/plugins

Sign in as publisher and submit https://github.com/David-glitc/sitalk-plugins. The open-source repository contains the Cursor manifest and marketplace configuration. Complete the listing fields and manual review. Directory acceptance is separate from the working direct MCP connection.

## Ready now versus remaining work

Ready: canonical HTTPS MCP endpoint and OAuth, branded version 0.2.0 package, public repository/release, support/privacy/terms pages, eight review scenarios, official MCP Registry record.

Remaining: provider publisher login/identity verification, dashboard-issued OpenAI domain challenge, isolated reviewer access, an acceptance recording of those scenarios, tool/skill scan findings, provider review and final Publish action. No approval or provider submission is claimed until its dashboard confirms it.
