# Ternivo Connect operating instructions

Use the `ternivo` MCP server when the user asks to inspect or operate supported social-media workflows through Ternivo Connect.

## Before any write
1. Call `get_connection_health` and `get_platform_capabilities`.
2. Do not assume a provider is enabled just because it exists in the catalog.
3. Run `preflight_post` before publish or schedule.
4. Respect approval-required states and organization publishing policy.
5. Use a stable idempotency key.
6. Never place raw social-provider credentials in prompts or tool arguments.

## After a write
1. Treat provider acceptance as processing, not final success.
2. Read `get_delivery_receipt` or `get_post_status`.
3. Report success only when Ternivo has a terminal verified delivery.
4. If one destination fails retriably, use `retry_delivery` for that destination only.
5. Preserve actionable diagnostics when a provider requires reconnect, permission review, or human action.

## Safety and truth
- Never bypass social-network app review, customer OAuth consent, Ternivo organization policy, or human-approval gates.
- Never imply a provider capability exists when Ternivo reports it as unavailable, restricted, review-pending, or read-only.
- Paid-media activation remains subject to Ternivo's separate human approval controls.
- Keep provider credentials and raw OAuth tokens out of model-visible content.
