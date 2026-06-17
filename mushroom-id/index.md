---
layout: default
title: Privacy Policy
description: Mushroom ID privacy policy
---

# Privacy Policy - Mushroom ID

**Effective date:** June 17, 2026  
**Developer:** Mustapha Marir - solo developer based in Morocco  
**Contact:** [marirfam@gmail.com](mailto:marirfam@gmail.com)  
**App package:** `com.marirfam.mushroomid`

This document explains what Mushroom ID processes, what it does not collect intentionally, why certain data is handled, and which third parties are involved.

---

## 1. What Mushroom ID does not intentionally collect

- **No account data.** The app has no sign-up or login flow.
- **No personal profile data.** We do not ask for your name, address, phone number, or contacts.
- **No precise location for core scanning.** The app does not require location permission to identify mushrooms.
- **No cloud sync of your saved collection.** Saved identifications stay on your device unless a future version clearly states otherwise.
- **No sale of personal data.** We do not sell user data.

---

## 2. What Mushroom ID does process

### a) Mushroom scan images

When you use the scan feature:

1. The image is prepared on your phone.
2. It is sent over HTTPS to our backend proxy at `https://mushroom-id-worker.marirfam.workers.dev`.
3. The proxy verifies abuse-protection signals and forwards the image to NVIDIA's hosted multimodal model API for identification.
4. The identification result returns to your phone.

We process this only to provide the identification result you requested.

**We do not intentionally store scan images in our own database.**

### b) Play Integrity and abuse protection

To reduce abuse, the app may use Google Play Integrity when sending scan requests. A Play Integrity token can be sent with the request so the backend can verify that the app installation appears genuine.

We also apply anonymous rate limiting and service-protection checks to reduce automated misuse.

### c) Local collection storage

If you save a result to your collection, that saved entry is stored locally on your device using on-device storage. This local data can include:

- mushroom name
- scientific name
- caution badge
- habitat
- season
- field-note details such as cap, gills, and stem notes
- confidence
- saved image path
- saved date

This saved collection is not uploaded to our servers by default.

### d) Crash and diagnostics reporting

If enabled in a release, the app may use crash or diagnostics tooling to improve stability. This can include:

- stack traces
- app version
- device model
- operating system version

If Sentry is enabled in a release build, its privacy policy is here: [https://sentry.io/privacy/](https://sentry.io/privacy/)

### e) Firebase Remote Config

The app may use Firebase Remote Config to adjust certain app behavior remotely, such as runtime configuration values or emergency changes, without requiring a full app update.

Firebase privacy information: [https://firebase.google.com/support/privacy](https://firebase.google.com/support/privacy)

### f) Advertising

The codebase may include Google AdMob components even if ads are not currently active in your release. If ads are enabled in a future version, Google AdMob may process device-level identifiers and ad-performance signals according to Google's policies.

Google Ads policy: [https://policies.google.com/technologies/ads](https://policies.google.com/technologies/ads)

---

## 3. Third-party service providers

Third-party processors or infrastructure may include:

- **Cloudflare Workers** - secure proxying, request handling, and service protection
- **NVIDIA API / NVIDIA-hosted multimodal model endpoint** - AI-based mushroom identification
- **Google Play Integrity** - app authenticity verification and abuse reduction
- **Google Firebase Remote Config** - runtime configuration
- **Google AdMob** - ad serving and measurement, if ads are enabled in a future release
- **Sentry** - crash reporting, if enabled in a release

---

## 4. Important safety limitation

Mushroom identification is inherently uncertain. The app may return incorrect, incomplete, or ambiguous results.

**Do not use this app as the sole basis for deciding whether a mushroom is safe to eat.**  
Always verify results with trusted field guides, qualified experts, or local foraging resources before making consumption decisions.

---

## 5. Children

Mushroom ID is not directed to children under 13. We do not knowingly collect personal data from children.

---

## 6. Your choices

- You can stop all app-related processing by uninstalling the app.
- You can delete your saved local collection by clearing app data or uninstalling the app.
- You can reset your Android Advertising ID from Android privacy settings, if advertising features are ever enabled.
- In supported regions, you can review ad privacy choices through the app's **Privacy preferences** setting when available.

---

## 7. Legal basis and service providers

Depending on your region, data may be processed under one or more of the following bases:

- **Contractual necessity** - to return the identification result when you request a scan
- **Legitimate interest** - to protect the service from abuse and maintain app reliability
- **Consent** - where required for advertising personalization choices

---

## 8. Security

Data sent between the app and backend services is transmitted over HTTPS.

---

## 9. Changes to this policy

If this policy changes materially, we will update this page and revise the effective date shown at the top.

---

## 10. Contact

For privacy questions or requests, contact:

- **Email:** [marirfam@gmail.com](mailto:marirfam@gmail.com)
- **Subject line:** please include "Mushroom ID privacy"

---

*Mushroom ID is built and supported by one developer.*
