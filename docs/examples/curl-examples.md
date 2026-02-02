# Curl examples (illustrative only)

These examples are placeholders. They are not production endpoints and are provided for documentation only.

## Redaction notes for sample JSON

- Hashes are shown as sha256:EXAMPLE

- IDs and domains are placeholders (for example, EXAMPLE_SHOP.myshopify.com)

- No secrets or production identifiers are included

## POST /ingest

```bash
curl -X POST "https://example-ingest.yourdomain.com/ingest" \
  -H "Content-Type: application/json" \
  -H "X-Shop-Domain: EXAMPLE_SHOP.myshopify.com" \
  -H "X-Signature: SIGNATURE_REDACTED" \
  -d @docs/examples/sample-normalized-event.json
```

## POST /ingest with inline payload

```bash
curl -X POST "https://example-ingest.yourdomain.com/ingest" \
  -H "Content-Type: application/json" \
  -H "X-Shop-Domain: EXAMPLE_SHOP.myshopify.com" \
  -H "X-Signature: SIGNATURE_REDACTED" \
  -d '{
    "event_name": "purchase",
    "event_id": "evt_2026_02_02_0001",
    "order_id": "ORDER_10001",
    "currency": "USD",
    "value": 123.45,
    "consent": {"marketing": "denied", "analytics": "granted"},
    "timestamp": "2026-02-02T12:34:56Z"
  }'
```

## Canonical explainer

See <https://ty-bridge.com/explainers/>.
