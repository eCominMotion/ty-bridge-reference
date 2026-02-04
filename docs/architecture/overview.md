# Architecture overview

TY Bridge is a reference architecture for moving checkout events from the Shopify Web Pixel surface into consent-aware server delivery. The production implementation uses Cloudflare Workers (or an equivalent edge runtime), but the concepts apply regardless of vendor.

## Components

### 1) Shopify App Pixel (Web Pixel environment)

- Runs inside Shopify's Web Pixel sandbox

- Receives standard customer events (for example, checkout and purchase)

- Applies consent gating before identifiers are captured

### 2) Ingest layer

- Accepts normalized event payloads from the pixel surface

- Validates required fields and applies consistent formatting

- Generates or preserves a stable event_id for de-duplication

### 3) Optional queue-backed relay

- Best-effort mode: direct send to destinations when latency is acceptable

- Durable mode: queue-backed delivery for retries and outage tolerance

- Both paths preserve event_id for deduplication downstream

### 4) Destinations

- Meta Conversions API (CAPI)

- Google Analytics 4 Measurement Protocol

- TikTok Events API

- Google Ads server-side events (when supported)

## Boundaries

- This architecture does not include OAuth flows, encryption code, or proprietary routing logic

- All identifiers are consent-gated and minimized

## Canonical explainer

See <https://ty-bridge.com/explainers/>.
