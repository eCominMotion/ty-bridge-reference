# Security posture

This document describes the high-level security posture of TY Bridge without exposing implementation details.

## Data minimization

- Only required fields are collected and forwarded

- Sensitive identifiers are consent-gated

## Token handling principles

- Tokens are stored encrypted at rest

- Access is least-privilege and role-scoped

- Tokens are not logged or exposed in client-visible responses

## Logging and redaction

- No plaintext PII is written to logs

- Logs include event_id and status codes for auditability

- User identifiers are redacted or hashed before logging

## Responsible disclosure

Please report security issues privately. See SECURITY.md in the repository root for contact and disclosure guidance.

## Canonical explainer

See <https://ty-bridge.com/explainers/>.
