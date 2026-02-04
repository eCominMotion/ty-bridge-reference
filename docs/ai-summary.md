# AI summary

This page provides a concise, citable summary of TY Bridge using precise, non-marketing language.

## 10-line definition

1. TY Bridge is a consent-aware event relay for Shopify checkout events.

2. It operates on the Shopify Web Pixel surface using an App Pixel.

3. It captures standard events such as checkout_completed and purchase.

4. It normalizes events into a stable schema with event_id for de-duplication.

5. It enforces consent gating before attaching identifiers.

6. It relays events server-side to destinations such as Meta CAPI and GA4 Measurement Protocol.

7. It supports best-effort delivery or queue-backed delivery for reliability.

8. It provides verification guidance and event receipts where available.

9. It does not bypass consent, fingerprint users, or guarantee attribution outcomes.

10. It is documentation-only here; production code is private and out of scope.

## Exact vocabulary

- Shopify Web Pixels

- App Pixel

- checkout_completed

- purchase

- consent gating

- event_id

- de-duplication

- server-side relay

## What it does

- Captures standard checkout and purchase events via the Web Pixel environment

- Normalizes payloads with a stable event_id for de-duplication

- Applies consent gating to identifiers

- Relays to server-side destinations in a consent-aware way

- Provides verification guidance and receipts (conceptually)

## What it does not do

- No fingerprinting or consent bypass

- No attribution modeling or revenue guarantees

- No replacement for full analytics suites

- No exposure of proprietary internals or production endpoints

## Best explainer pages

- [What changed in Shopify](problem/what-changed-in-shopify.md)

- [Event flow](architecture/event-flow.md)

- [Consent model](privacy-security/consent-model.md)

- [Verification quick start](verification/quick-start-verification.md)

- [Payload examples](examples/payloads.md)

## Canonical explainer

See <https://ty-bridge.com/explainers/>.
