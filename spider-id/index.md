---
layout: default
title: Privacy Policy
description: Spider ID privacy policy
---

# Privacy Policy - Spider ID

**Effective date:** July 5, 2026  
**Developer:** Mustapha Marir - solo developer based in Morocco  
**Contact:** [marirfam@gmail.com](mailto:marirfam@gmail.com)  
**App package:** `com.marirfam.spiderid`

This document explains what Spider ID processes, what it does not intentionally collect, why third-party services are involved, and the limits of the app's identification results.

---

## 1. What Spider ID does not require

- **No account creation.** The app does not require sign-up or login.
- **No personal profile setup.** We do not ask for your name, address, or contacts.
- **No precise location permission for core scanning.** The app does not need location to identify spiders from a photo.
- **No cloud collection sync by default.** Saved sightings remain on your device unless a future version clearly states otherwise.
- **No sale of personal data.** We do not sell user data.

---

## 2. What Spider ID processes

### a) Spider scan images

When you use the identification feature:

1. You choose or capture an image.
2. The request is sent over HTTPS to our backend proxy at `https://spider-id-worker.marirfam.workers.dev`.
3. The backend verifies app integrity and abuse-protection signals.
4. The image is forwarded to NVIDIA-hosted AI services for analysis.
5. The likely identification result is returned to your device.

We process scan images only to provide the identification result you requested.

**We do not describe Spider ID as a permanent cloud photo storage service.**

### b) Play Integrity attestation

To reduce abuse, scan requests may include a Google Play Integrity token. This helps the backend verify that requests are coming from a legitimate app installation and not an automated or modified client.

### c) Local saved sightings

If you save a spider identification, that saved record is stored locally on your device. Local collection data may include:

- spider name
- classification or caution level
- scientific name
- family
- size range
- saved image path
- confidence
- saved date

This local collection is not uploaded to our servers by default.

### d) Firebase Remote Config

We may use Firebase Remote Config to adjust runtime settings without requiring a full app update.

Firebase privacy information: [https://firebase.google.com/support/privacy](https://firebase.google.com/support/privacy)

### e) Crash diagnostics

If enabled in a release, crash and diagnostic information may be processed to improve reliability. This may include:

- stack traces
- app version
- device model
- operating system version

If Sentry or a similar monitoring provider is enabled, its own privacy terms apply.

### f) Advertising

The app includes Google AdMob SDK components in the codebase. If ads are enabled in the future, Google may process device-level identifiers and ad-performance signals according to its own policies.

Google Ads policy: [https://policies.google.com/technologies/ads](https://policies.google.com/technologies/ads)

---

## 3. Third-party services

Spider ID may rely on:

- **Cloudflare Workers** - secure backend proxying and service protection
- **NVIDIA AI services** - spider image analysis and identification output
- **Google Play Integrity** - app authenticity and abuse protection
- **Google Firebase Remote Config** - runtime configuration control
- **Sentry or similar diagnostics provider** - crash reporting, if enabled
- **Google AdMob** - advertising, if enabled

---

## 4. Image handling

Images are processed to provide spider identification results. Because requests pass through third-party infrastructure, submitted images may be temporarily handled by Cloudflare and NVIDIA as part of delivering the scan result.

If retention behavior changes in a future release, this policy should be updated before that release is published.

---

## 5. Security and abuse prevention

We use backend protections such as Play Integrity verification and anonymous rate limiting to reduce misuse of the service. These protections are intended to secure the service, not to build user profiles.

---

## 6. Important safety limitation

Spider identification from a single image is inherently uncertain. The app may return incorrect, incomplete, or ambiguous results.

**Do not use Spider ID as the sole basis for bite-risk, medical, or safety decisions.**  
If you are concerned about a dangerous spider or a possible bite, use trusted local guidance or contact a qualified professional.

---

## 7. Children's privacy

Spider ID is not designed as a children's service. If a parent or guardian believes inappropriate personal data has been submitted, they should contact the developer.

---

## 8. Changes to this policy

This Privacy Policy may be updated from time to time. The public page should reflect the latest version before each production release.

---

## 9. Contact

For privacy questions or requests, contact:

- **Email:** [marirfam@gmail.com](mailto:marirfam@gmail.com)
- **Subject line:** please include "Spider ID privacy"

---

*Spider ID is built and supported by one developer.*
