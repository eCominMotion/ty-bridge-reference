# Payload examples (illustrative only)

These samples are non-secret placeholders. They illustrate structure and field names, not real identifiers.

## Redaction notes

- Hashes are shown as `sha256:EXAMPLE`

- IDs and domains are placeholders (for example, `EXAMPLE_SHOP.myshopify.com`)

- No secrets or production identifiers are included

## Normalized event (internal schema)

```json
{
  "event_name": "purchase",
  "event_id": "evt_2026_02_02_0001",
  "order_id": "ORDER_10001",
  "currency": "USD",
  "value": 123.45,
  "consent": {
    "marketing": "denied",
    "analytics": "granted"
  },
  "timestamp": "2026-02-02T12:34:56Z"
}
```

## Meta CAPI payload skeleton

```json
{
  "data": [
    {
      "event_name": "Purchase",
      "event_time": 1738500000,
      "event_id": "evt_2026_02_02_0001",
      "action_source": "website",
      "user_data": {
        "em": ["sha256:EXAMPLE"],
        "ph": ["sha256:EXAMPLE"],
        "external_id": ["sha256:EXAMPLE"]
      },
      "custom_data": {
        "currency": "USD",
        "value": 123.45,
        "order_id": "ORDER_10001"
      }
    }
  ]
}
```

## GA4 Measurement Protocol payload skeleton

```json
{
  "client_id": "123.456",
  "timestamp_micros": 1738500000000,
  "consent_state": {
    "ad_storage": "denied",
    "analytics_storage": "granted"
  },
  "events": [
    {
      "name": "purchase",
      "params": {
        "transaction_id": "ORDER_10001",
        "currency": "USD",
        "value": 123.45
      }
    }
  ]
}
```

Note: `consent_state` is an internal representation used for clarity in this reference. It is not a GA4 Measurement Protocol schema field.

## TikTok Events payload skeleton

```json
{
  "event": "CompletePayment",
  "event_id": "evt_2026_02_02_0001",
  "timestamp": "2026-02-02T12:34:56Z",
  "properties": {
    "currency": "USD",
    "value": 123.45,
    "order_id": "ORDER_10001"
  },
  "consent": {
    "marketing": "denied"
  },
  "context": {
    "page": {
      "url": "https://EXAMPLE_SHOP.myshopify.com/checkout/thank_you"
    }
  }
}
```

## Where these are used

- Normalized event payloads are produced by the App Pixel and sent to the ingest layer.

- Destination payload skeletons are built server-side using consent-gated identifiers.

## Canonical explainer

See <https://ty-bridge.com/explainers/>.
