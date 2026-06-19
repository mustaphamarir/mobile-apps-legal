---
layout: default
title: Privacy Policy
description: Insect ID privacy policy
---

# Privacy Policy - Insect ID

**Effective date:** June 19, 2026  
**Developer:** Mustapha Marir - solo developer based in Morocco  
**Contact:** [marirfam@gmail.com](mailto:marirfam@gmail.com)  
**App package:** `com.marirfam.insectid`

This document explains what Insect ID processes, what it does not intentionally collect, why data is used, and which third parties are involved.

---

## 1. What Insect ID does

Insect ID helps users identify household, garden, and outdoor insects from photos. It may also provide practical guidance such as likely habitat, visible traits, and non-medical care suggestions for common bug bites.

The app is informational only. It is not a medical, pest-control, or emergency service.

---

## 2. What Insect ID does not intentionally collect

- **No account data.** The app has no login or sign-up flow.
- **No personal profile data.** We do not ask for your name, phone number, address, or contacts to use the core identification features.
- **No precise location permission for the core app.** The app does not require location permission to identify insects.
- **No cloud sync of your saved collection.** Saved insect results remain on your device unless a future version clearly states otherwise.
- **No sale of personal data.** We do not sell user data.

---

## 3. What Insect ID processes

### a) Scan images

When you use the identification feature:

1. You capture or choose an image on your phone.
2. The app sends the request over HTTPS to our backend proxy.
3. The proxy verifies abuse-protection signals and forwards the image to the configured AI provider.
4. The identification response is returned to your device.

We process the image only to provide the identification result you requested.

**We do not describe Insect ID as a permanent cloud photo storage service.**

### b) Device integrity signals

To reduce abuse, scan requests may include a Play Integrity attestation token or similar app/device legitimacy signal. This is used to help verify that scan traffic comes from a valid app installation.

### c) Local saved collection

If you save an identification, the saved record is stored locally on your device. This local data can include:

- insect common name
- scientific name or family
- classification label
- confidence
- saved image path
- saved date

This local collection is not intended to be uploaded to our servers.

### d) Service protection and rate limiting

We may process anonymous security and rate-limit signals to protect the backend from misuse, automated abuse, or excessive request volume.

### e) Crash and diagnostics reporting

If enabled in a release, crash and diagnostic information may be processed to improve app stability. This can include:

- stack traces
- app version
- device model
- operating system version

If Sentry is enabled for a given release, Sentry privacy information is available here: [https://sentry.io/privacy/](https://sentry.io/privacy/)

### f) Firebase Remote Config

We may use Firebase Remote Config to manage runtime settings without requiring a full app update.

Firebase privacy information: [https://firebase.google.com/support/privacy](https://firebase.google.com/support/privacy)

---

## 4. Third-party services

Insect ID may rely on these services:

- **Cloudflare Workers** - secure backend proxy and request handling
- **NVIDIA AI services** - AI-based insect image analysis
- **Google Play Integrity** - app authenticity verification and abuse reduction
- **Firebase Remote Config** - runtime configuration management
- **Sentry** - optional crash reporting and diagnostics, if enabled

Third-party providers may temporarily process submitted images or technical request data as part of delivering the identification result.

---

## 5. Image handling

Images submitted for scans are processed to provide insect identification results.

We do not state that user scan images are permanently stored in our own database. However, because requests pass through third-party infrastructure, submitted images may be temporarily processed by backend and AI providers as needed to complete the scan.

If retention behavior changes materially in the future, this policy should be updated before release.

---

## 6. Important limitations

Insect identification from a single image is inherently uncertain. Results may be incomplete, ambiguous, or wrong.

### Bug bite guidance

Any bite-related suggestions in the app are **non-medical guidance only**.

**Do not use this app as the sole basis for medical treatment, allergic reaction decisions, infestation response, or emergency action.**  
If symptoms are severe or urgent, contact a qualified medical professional or local emergency service.

---

## 7. Children

Insect ID is not directed to children under 13, and we do not knowingly collect personal data from children.

---

## 8. Your choices

- You can stop all app-related processing by uninstalling the app.
- You can delete locally saved entries by clearing app data or uninstalling the app.
- You can choose not to submit images for identification.

---

## 9. Security

Data sent between the app and backend services is transmitted over HTTPS.

---

## 10. Changes to this policy

This Privacy Policy may be updated from time to time. When material changes are made, the effective date on this page will be updated.

---

## 11. Contact

For privacy questions or requests, contact:

- **Email:** [marirfam@gmail.com](mailto:marirfam@gmail.com)
- **Subject line:** please include "Insect ID privacy"

---

*Insect ID is built and supported by one developer.*
