---
name: Configure webhooks for record lifecycle events
description: Register a webhook endpoint so Predoc pushes real-time notifications when records are retrieved, processed, or ready for review.
api: Predoc Partner API
base_url: https://partner-sandbox.predoc.ai/api/v1
operations:
  - AuthController_signIn_v1
  - WebhookConfigurationController_createWebhookConfiguration_v1
  - WebhookConfigurationController_listWebhookConfigurations_v1
---

# Configure webhooks for record lifecycle events

Push beats polling — register a webhook so Predoc notifies you when a patient's records
are retrieved, processed, or ready for review.

## 1. Authenticate
Call `AuthController_signIn_v1` (`POST /v1/auth/token`); send the returned `access_token`
as a bearer token (5-minute expiry, refresh as needed).

## 2. Create the webhook configuration
Call `WebhookConfigurationController_createWebhookConfiguration_v1` with your receiving
endpoint URL. Predoc will POST notifications to it across the record lifecycle
(retrieved → processed → ready for review).

## 3. Verify and manage
- List existing configs with `WebhookConfigurationController_listWebhookConfigurations_v1`.
- Update with `WebhookConfigurationController_updateWebhookConfiguration_v1`.
- Remove with `WebhookConfigurationController_deleteWebhookConfiguration_v1`.

## Handling deliveries
On each notification, look up the patient/request and fetch newly-available documents via
`PatientController_getPatientDocuments_v1`. Return 2xx quickly from your endpoint and process
asynchronously. Re-authenticate on **401**.
