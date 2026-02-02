# What changed in Shopify

Shopify has shifted checkout customization toward Checkout Extensibility and Web Pixels. This change reduces or removes legacy script surfaces on Thank You and Order Status pages for many plans and storefront configurations.

## Why legacy Thank You and Order Status scripts became unreliable

- Legacy Additional Scripts and ScriptTags depended on page-level script execution on the Thank You and Order Status pages.

- Those surfaces are now deprecated or limited, so scripts may no longer run when you expect them to.

- Even when a script executes, the data it can access is more restricted than before.

## Why "pixel fired" is not the same as "attributed correctly"

A pixel event can be emitted but still be dropped or de-duplicated downstream. Consent gates, ad blockers, and destination validation rules all influence whether a fired pixel results in an attributed purchase.

## Typical merchant symptoms

- Purchases missing in ad platform dashboards despite successful checkouts

- GA4 Realtime showing 0 purchases while orders exist in Shopify

- Duplicates from mixed legacy scripts and newer pixel pipelines
