# Why pixels are not truth anymore

Pixels are an important signal, but they are not a guarantee of attribution or delivery. In the modern Shopify environment, a pixel can fire and still fail to produce an attributed purchase downstream.

## Reasons a fired pixel may not result in attribution

- Consent is denied or restricted, which removes identifiers needed by the destination

- Ad blockers or browser privacy controls interfere with network requests

- Destination validation rejects the payload (missing fields or formatting)

- De-duplication drops one of the duplicate events when client and server both send

- Reporting delays or window mismatches cause temporary gaps

## What this means for merchants

- A "pixel fired" message is necessary but not sufficient

- Verification needs to include destination-side test tools and receipts

- You must consider consent state at the moment of the event
