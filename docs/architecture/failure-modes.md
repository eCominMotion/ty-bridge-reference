# Failure modes

TY-Bridge favors visible, explainable, and recoverable failures. The scenarios below describe expected behavior at a high level.

## Common failure modes

### 1) Consent denied

- Identifiers are withheld

- Only non-PII fields may be sent, if the destination allows

- Some destinations may drop the event because identifiers are missing

### 2) Pixel blocked or not executed

- No event reaches ingest

- Verification relies on Shopify and destination debug tools to confirm

### 3) Payload validation error

- Ingest rejects the event with a stable error code and message

- The event is not forwarded

### 4) Queue backlog or relay outage

- Durable delivery retries with backoff and bounded attempts

- Best-effort delivery may drop after a failure

- All attempts are logged for audit

### 5) Destination rejection

- Destination returns a validation error or rate limit

- The rejection is recorded with status and reason

### 6) Duplicate events

- event_id enables destination-side de-duplication

- If client and server both send, one is dropped downstream

## Canonical explainer

See <https://ty-bridge.com/explainers/>.
