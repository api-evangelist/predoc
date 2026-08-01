---
name: Generate and download a patient clinical summary
description: Request a Predoc-generated clinical summary document for a patient and poll for it to become READY.
api: Predoc Partner API
base_url: https://partner-sandbox.predoc.ai/api/v1
operations:
  - AuthController_signIn_v1
  - PatientController_requestPatientClinicalSummary_v1
  - DocumentController_getPatientClinicalSummary_v1
---

# Generate and download a patient clinical summary

## 1. Authenticate
Call `AuthController_signIn_v1` (`POST /v1/auth/token`) with `client_id` + `secret_key`;
send the returned `access_token` as a bearer token. Refresh before the 5-minute expiry.

## 2. Request the clinical summary
Call `PatientController_requestPatientClinicalSummary_v1` for the patient. Optionally scope
the summary by requested document categories and a date range — these select the source
documents (the organization document-set delivery mode does not filter summary sources).
Capture the `patientSummaryRequestId` from the response.

## 3. Poll for the document status
Call `DocumentController_getPatientClinicalSummary_v1` with the `patientSummaryRequestId`
as the document ID. Status values progress through:
`QUEUEING` → `QUEUED` → `GENERATING` → `READY` (or `ERROR`).
When `READY`, download the summary via its `url`.

## Errors
- **401**: token missing/expired — re-authenticate.
- **404**: document/patient not found.
- `ERROR` status means generation failed; re-request the summary.
