---
name: zip-co-us-order-lifecycle
description: Authorize a Zip (US) BNPL order, confirm it, then capture, refund or void it and check its status.
api: openapi/zip-co-gateway-api-1-api-openapi.yml
operations:
  - ordersauthorize
  - ordersorderidconfirm
  - ordersassociate
  - ordersorderidcapture
  - ordersorderidrefund
  - ordersorderidvoid
  - ordersorderidstatus
generated: '2026-10-20'
method: generated
source: https://docs.us.zip.co/llms.txt
---
# Zip US order lifecycle

Base URL: `https://gateway.us.zip.co` (sandbox `https://gateway.sand.us.zip.co`, per the docs reference pages).

1. **Authorize**: `ordersauthorize` (POST /orders/authorize) creates the checkout context and returns the shopper redirect.
2. **Confirm**: once the shopper returns, call `ordersorderidconfirm` (POST /orders/{orderId}/confirm).
3. **Associate** (optional): `ordersassociate` (POST /orders/associate) attaches your own merchant order ID.
4. **Settle funds**: `ordersorderidcapture` captures. If you need to release uncaptured funds, use `ordersorderidvoid`. Use `ordersorderidrefund` after capture.
5. **Check**: `ordersorderidstatus` (GET /orders/{orderId}/status). It is read-only and safe to retry.

Rules: POST operations move money. Do not blind-retry them. Check the status first. The swagger form of these operations takes a `sync` query parameter and a `QP-Territory` header.
