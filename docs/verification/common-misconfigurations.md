# Common misconfigurations

These are frequent causes of missing or inconsistent attribution.

## Destination configuration

- Wrong pixel ID, measurement ID, or advertiser ID

- Multiple destinations configured with mismatched IDs

## Consent and privacy

- Consent denied or misclassified (marketing vs analytics)

- Consent banner not firing before pixel events

## De-duplication

- event_id missing or unstable between client and server

- Multiple events with the same order_id but different event_id

## Environment and tooling

- Ad blockers or strict browser privacy settings

- Using reports instead of Test Events or DebugView during setup

- Staging domains not included in destination allowlists

## Canonical explainer

See <https://ty-bridge.com/explainers/>.
