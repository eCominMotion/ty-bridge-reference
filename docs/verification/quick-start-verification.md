# Quick-start verification

This checklist helps merchants and agencies confirm that events are captured and delivered correctly.

## 1) Verify pixel capture happened

- Trigger a real or test checkout in Shopify

- Confirm the App Pixel received a checkout_completed or purchase event

- Confirm the event includes consent state and a stable event_id

## 2) Verify Meta Test Events

- Use the Events Manager Test Events tool

- Send a test event with a known event_id

- Confirm the event appears and is not rejected

- See: [docs/verification/meta-test-events.md](meta-test-events.md)

## 3) Verify GA4 Realtime and DebugView

- Open GA4 Realtime and DebugView

- Confirm the purchase event appears shortly after checkout

- If Realtime shows 0, review common reasons

- See: [docs/verification/ga4-realtime-and-debugview.md](ga4-realtime-and-debugview.md)

## 4) Verify TikTok Test Events

- Use the TikTok Events Manager Test Events tool

- Confirm the event_id appears and is marked received

- See: [docs/verification/tiktok-test-events.md](tiktok-test-events.md)

## Common pitfalls

- Consent denied or restricted at the time of the event

- Wrong destination IDs (pixel ID, measurement ID, or advertiser ID)

- Ad blockers or browser privacy settings block the pixel

- Looking at reports instead of test tools or debug views

- Duplicate client and server events without a stable event_id

## Canonical explainer

See <https://ty-bridge.com/explainers/>.
