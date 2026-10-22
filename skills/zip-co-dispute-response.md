---
name: zip-co-dispute-response
description: List Zip Global disputes, upload evidence files and submit evidence, or accept a dispute.
api: openapi/zip-co-gateway-api-openapi.yml
operations:
  - ListDisputes
  - GetDispute
  - UploadFile
  - DownloadFile
  - DeleteFile
  - SubmitEvidence
generated: '2026-10-20'
method: generated
source: https://docs.us.zip.co/docs/disputes.md
---
# Zip dispute response

1. `ListDisputes` (GET /global/v1/disputes) lists disputes. It filters by MerchantId, Status and OpenedAfter/OpenedBefore and pages with Limit/StartingAfter.
2. `GetDispute` (GET /global/v1/disputes/{disputeId}) returns a single dispute.
3. `UploadFile` (POST /global/v1/disputes/{disputeId}/files/{category}) uploads evidence from a blob URL. `DownloadFile` and `DeleteFile` manage files that are already attached.
4. `SubmitEvidence` (POST /global/v1/disputes/{disputeId}/evidence) submits the case.

To concede a dispute, POST /global/v1/disputes/{disputeId}/accept moves it to lost. That operationId (`AcceptDispute`) is duplicated in the swagger by POST /merchant-disputes/close. Bind it by path, and confirm with a human first because it cannot be undone.
