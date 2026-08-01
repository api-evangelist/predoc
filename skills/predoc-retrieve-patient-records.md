---
name: Request and retrieve a patient's medical records
description: Authenticate, submit a record-retrieval request for a patient, poll its status, then fetch the returned clinical documents.
api: Predoc Partner API
base_url: https://partner-sandbox.predoc.ai/api/v1
operations:
  - AuthController_signIn_v1
  - RequestController_createRecordRequestV2_v2
  - PatientController_getPatientRequests_v1
  - PatientController_getPatientDocuments_v1
---

# Request and retrieve a patient's medical records

Use the Predoc Partner API to retrieve a complete, normalized patient history.

## 1. Authenticate
Call `AuthController_signIn_v1` — `POST /v1/auth/token` with your `client_id` and
`secret_key`. Read `access_token` from the response and send it as
`Authorization: Bearer <access_token>` on every subsequent call. **Tokens expire after
5 minutes** — refresh before expiry rather than reusing a stale token.

## 2. Create the patient + record request
Call `RequestController_createRecordRequestV2_v2` with the patient's PII and the required
previous-provider information. V2 guards against creating duplicate patients with the same
PII. Capture the returned record/request ID. (Previous providers are required on ALL
requests as of Partner API v1.2.0.)

## 3. Track request status
Poll `PatientController_getPatientRequests_v1` for the patient to watch the request move
through its status states. Requests start in `Creating`/`Open` and progress as Predoc works
the retrieval; do not attempt updates once a request has advanced past `Open`.

## 4. Fetch the returned documents
When records are ready, call `PatientController_getPatientDocuments_v1` for the patient to
list documents, each downloadable via its `url` property. For specific clinical categories
use the granular endpoints (medications, lab tests, imaging, procedure notes, allergies,
vaccines, HIE docs).

## Conventions & errors
- Auth failures return **401** — re-authenticate.
- Unknown patient/resource returns **404**.
- Some operations return an explanatory `message` in the standard response object instead of
  failing hard (e.g. a locked patient). Always check `message`.
- Prefer webhooks (see the webhook-setup skill) over tight polling for record lifecycle events.
