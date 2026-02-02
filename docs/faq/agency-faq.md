# Agency FAQ

## What is the verification workflow?

Start with [docs/verification/quick-start-verification.md](../verification/quick-start-verification.md) and confirm test events in each destination.

## Can I use my own server-side stack?

TY-Bridge describes a reference architecture. The concepts can be implemented in multiple runtimes.

## How does de-duplication work?

A stable event_id is preserved from pixel to server so destinations can drop duplicates.

## What data is sent when consent is denied?

Identifiers are withheld. Non-PII order properties may be sent if the destination allows.

## Do you provide guarantees about attribution?

No. Attribution depends on destination policies and consent state.

## Canonical explainer

See <https://ty-bridge.com/explainers/>.
