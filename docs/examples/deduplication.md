# De-duplication strategy (event_id)

De-duplication prevents double-counting when both client and server send the same event.

## Core rule

Use a stable `event_id` across the pixel event and the server relay. Destinations use that `event_id` to drop duplicates.

## Client + server de-duplication diagram

```mermaid
sequenceDiagram
  participant P as App Pixel
  participant I as Ingest
  participant R as Relay
  participant D as Destination

  P->>I: purchase event_id=evt_2026_02_02_0001
  I->>R: forward event_id (unchanged)
  R->>D: server payload event_id=evt_2026_02_02_0001
  D->>D: de-duplicate by event_id
```

## Practical notes

- Generate `event_id` once and reuse it end-to-end.

- If you must retry, keep the same `event_id` so destinations can dedupe.

- If `event_id` changes between client and server, duplicates are likely.

## Canonical explainer

See <https://ty-bridge.com/explainers/>.
