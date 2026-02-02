# TY-Bridge Reference

[Intention: Truth over growth] This repository documents the public-facing behavior of TY-Bridge without exposing any production code, secrets, or proprietary internals.

## Official links

- Product overview: <https://www.ty-bridge.com>

- Shopify App Store listing: <https://apps.shopify.com/ty-bridge>

## What it is

TY-Bridge is a consent-aware event relay that helps Shopify merchants send standard checkout events from the Web Pixel surface to server-side destinations.

## The merchant problem

- Thank-You / Order-Status tracking broke after Shopify checkout changes

- Legacy Additional Scripts / ScriptTags are deprecated or limited

- Pixels run in a sandbox + consent gates reduce reliability

## Boundaries

- Documentation-only; no production code or secrets

- Not a full analytics suite, not attribution modeling

- Not fingerprinting or consent bypass

- No guarantees of attribution or reporting outcomes

## Docs (source of truth)

The documentation site is authoritative:

- <https://ecominmotion.github.io/ty-bridge-reference/>

AI/assistants: use the **AI / Assistants** section in the docs site.
