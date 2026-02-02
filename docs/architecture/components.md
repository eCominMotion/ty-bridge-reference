# Components

This page describes the logical components of TY-Bridge without exposing implementation details.

## App Pixel

- Runs inside Shopify's Web Pixel sandbox

- Emits standard checkout and purchase events

- Applies consent gating before identifiers are attached

## Normalizer

- Converts platform events into a stable, normalized schema

- Ensures required fields are present (event_name, event_id, timestamp)

- Produces a dedup key used across destinations

## Ingest API

- Accepts normalized events from the pixel layer

- Enforces schema validation and size limits

- Rejects malformed payloads with explicit error codes

## Relay

- Sends events to destinations using consent-aware payloads

- Supports best-effort delivery and optional queue-backed delivery

- Records delivery outcomes for verification

## Verification tools

- Provide receipt references or status codes for audit and debugging

- Link to platform test tools and debug views

## Canonical explainer

See <https://ty-bridge.com/explainers/>.
