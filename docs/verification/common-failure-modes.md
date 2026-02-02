# Common failure modes (merchant-facing)

This page addresses the most frequent “it looks broken” scenarios merchants and agencies encounter after migration.

## Why GA4 Realtime shows 0

- Wrong property or measurement ID

- Event name mismatch (not `purchase`)

- Consent denied, so identifiers are withheld

- Reporting filters or missing DebugView settings

- Ad blockers or browser privacy settings

## Why DebugView is empty

- Debug mode not enabled for the test session

- Event is blocked before it reaches the ingest layer

- Event is sent server-side only without debug flags

- Incorrect stream or property

## Why Meta shows “received” but not “attributed”

- Missing or low-quality identifiers due to consent gating

- Event is outside the attribution window

- Validation warnings or dedup rules suppress the event

- Reporting delays or delayed match quality updates

## Why duplicates happen after migration

- Legacy Additional Scripts still firing

- Pixel and server both send, but `event_id` is unstable

- Multiple pixels or data sources are configured with overlapping events

- Test events and live events are mixed without clear separation

## What to do next

- Start with [verification quick start](quick-start-verification.md)

- Review [de-duplication guidance](../examples/deduplication.md)

- Check [common misconfigurations](common-misconfigurations.md)

## Canonical explainer

See <https://ty-bridge.com/explainers/>.
