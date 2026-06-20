---
layout: default
title: Privacy Policy
description: Moth Identifier privacy policy
---

# Privacy Policy - Moth Identifier

**Effective date:** June 19, 2026  
**Developer:** Mustapha Marir - solo developer based in Morocco  
**Contact:** [marirfam@gmail.com](mailto:marirfam@gmail.com)  
**App package:** `com.marirfam.mothid`

This document explains what Moth Identifier collects, what it does not collect, why data is processed, and which third parties are involved.

---

## 1. What Moth Identifier does not collect

- **No account data.** The app has no sign-up or login flow.
- **No personal profile data.** We do not ask for your name, address, phone number, age, or contacts.
- **No precise location.** The app does not request location permission.
- **No cloud sync of your collection.** Saved moth identifications stay on your device.
- **No sale of personal data.** We do not sell user data.

---

## 2. What Moth Identifier does process

### a) Moth scan images

When you use the scan feature:

1. The image is prepared on your phone.
2. It is sent over HTTPS to our backend proxy at `https://moth-id-worker.marirfam.workers.dev`.
3. The proxy verifies app integrity and forwards the image to NVIDIA's hosted multimodal model API for moth identification.
4. The identification result returns to your phone.

We process this only to provide the identification result you requested.

**We do not intentionally store scan images in our own database.**

### b) Play Integrity attestation

To reduce abuse, the app uses Google Play Integrity when sending scan requests. A Play Integrity token is sent with the scan request so the backend can verify the app installation is genuine.

### c) Local collection storage

If you save a result to your collection, that saved entry is stored locally on your device using an on-device database. This local data can include:

- moth name
- sighting class
- scientific name
- moth group
- night context
- confidence
- saved image path
- saved date

This local collection is not uploaded to our servers.

### d) Crash and diagnostics reporting

We use Sentry to receive crash and error diagnostics so we can improve app stability. This may include:

- stack traces
- app version
- device model
- operating system version

Sentry privacy policy: [https://sentry.io/privacy/](https://sentry.io/privacy/)

### e) Advertising

The app includes Google AdMob SDK components. If ads are enabled in the future, AdMob may process device-level identifiers and ad-performance signals, including the Android Advertising ID, according to Google's policies.

Google Ads policy: [https://policies.google.com/technologies/ads](https://policies.google.com/technologies/ads)

### f) Firebase Remote Config

We use Firebase Remote Config to adjust certain app behavior remotely, such as ad settings or emergency configuration changes, without requiring a full app update.

Firebase privacy information: [https://firebase.google.com/support/privacy](https://firebase.google.com/support/privacy)

---

## 3. Children

Moth Identifier is not directed to children under 13. We do not knowingly collect personal data from children.

---

## 4. Your choices

- You can stop all app-related processing by uninstalling the app.
- You can delete your saved local collection by clearing app data or uninstalling the app.
- You can reset your Android Advertising ID from Android privacy settings.
- In supported regions, you can review ad privacy choices through the app's **Privacy preferences** setting.

---

## 5. Legal basis and service providers

Depending on your region, data is processed under one or more of the following bases:

- **Contractual necessity** - to return the identification result when you request a scan
- **Legitimate interest** - to protect the service from abuse and maintain app reliability
- **Consent** - where required for advertising personalization choices

Third-party processors may include:

- **Cloudflare** - request handling and backend delivery
- **NVIDIA API / NVIDIA-hosted multimodal model endpoint** - AI-based moth identification
- **Google Play Integrity** - app authenticity verification
- **Google Firebase Remote Config** - runtime configuration
- **Google AdMob** - ad serving and measurement
- **Sentry** - crash reporting

---

## 6. Security

Data sent between the app and backend services is transmitted over HTTPS.

---

## 7. Changes to this policy

If this policy changes materially, we will update this page and revise the effective date shown at the top.

---

## 8. Contact

For privacy questions or requests, contact:

- **Email:** [marirfam@gmail.com](mailto:marirfam@gmail.com)
- **Subject line:** please include "Moth Identifier privacy"

---

*Moth Identifier is built and supported by one developer.*
