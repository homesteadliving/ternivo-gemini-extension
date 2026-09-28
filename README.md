# Ternivo Connect for Gemini CLI

Ternivo Connect gives Gemini CLI users a controlled MCP interface for social-media operations across authorized accounts.

It supports connection health, provider capability discovery, content preflight, publishing and scheduling where approved, terminal delivery receipts, targeted retries, diagnostics, analytics, inbox/community workflows, listening, creator operations, and calendar workflows.

## Install from Gemini CLI

```bash
gemini extensions install https://github.com/homesteadliving/ternivo-gemini-extension
```

Then verify the extension:

```bash
gemini extensions list
```

On first authenticated use, Gemini CLI should follow Ternivo's OAuth discovery flow. Complete the browser authorization for your Ternivo organization when prompted.

## Direct MCP alternative

If you prefer to add the MCP server directly instead of installing the extension:

```bash
gemini mcp add --transport http ternivo https://ternivo.app/mcp
gemini mcp list
```

## Security model

Ternivo is the credential and policy boundary. Social-provider passwords and raw provider OAuth tokens are not placed in Gemini prompts. Ternivo enforces organization membership, provider-account assignment, provider capability truth, preflight, approval policy, idempotency, delivery verification, retries, diagnostics, and tenant isolation.

## Links

- Product: https://ternivo.app/social-delivery
- Gemini integration guide: https://ternivo.app/integrations/gemini
- Developer documentation: https://ternivo.app/developers
- Privacy: https://ternivo.app/connect/privacy.html
- Security: https://ternivo.app/connect/security.html
- Support: https://ternivo.app/connect/support.html

## Public Gemini CLI Gallery

This repository is structured for public discovery by the Gemini CLI Extension Gallery. Google indexes public repositories that use the `gemini-cli-extension` GitHub topic and contain `gemini-extension.json` at the repository root.

Ternivo, LLC
