# Thank You and Order Status migration

Legacy tracking often relied on Additional Scripts and ScriptTags running on Thank You and Order Status pages. With Checkout Extensibility and Web Pixels, the migration path is to move intent into pixel events and then relay server-side where needed.

## Migration outline

1) Inventory what the legacy scripts were doing (events, fields, destinations).

2) Map each intent to a standard event name and payload.

3) Capture events in the Shopify App Pixel surface.

4) Relay server-side to destinations that require server delivery.

5) Verify using destination test tools and receipts.

## What changes in practice

- The pixel runs in a sandbox with limited access to window and browser APIs.

- Consent gating affects identifiers you can send.

- Server-side relay becomes the stable path for attribution where supported.

## Suggested next steps

- Read the architecture overview: [docs/architecture/overview.md](../architecture/overview.md)

- Run verification: [docs/verification/quick-start-verification.md](../verification/quick-start-verification.md)

## Canonical explainer

See <https://ty-bridge.com/explainers/>.
