---
name: zip-co-global-checkout-charge
description: Create a Zip Global checkout, then create, capture, refund or void the charge, using Idempotency-Key on writes.
api: openapi/zip-co-gateway-api-openapi.yml
operations:
  - CreateCheckout
  - GetCheckout
  - CreateCharge
  - GetCharge
  - CaptureCharge
  - RefundCharge
  - VoidCharge
generated: '2026-10-20'
method: generated
source: openapi/zip-co-gateway-api-openapi.yml
---
# Zip Global checkout and charge

Auth: Bearer token (securityScheme `Bearer`).

1. `CreateCheckout` (POST /global/v1/checkouts) opens a checkout session. Poll it with `GetCheckout`.
2. `CreateCharge` (POST /global/v1/charges) creates a charge on the completed checkout, or creates and captures it in one call.
3. `CaptureCharge`, `RefundCharge` or `VoidCharge` (POST /global/v1/charges/{chargeId}/capture|refund|cancel) act on the charge. Read it with `GetCharge`.

Idempotency: the spec documents an optional `Idempotency-Key` header on CreateCharge, CaptureCharge, RefundCharge and VoidCharge. Send a unique key per logical write and reuse it on retries.
Errors: see https://developers.zip.co/page/charges-error-scenarios.md.
