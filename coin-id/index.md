---
layout: default
title: Privacy Policy
description: Coin ID privacy policy
---

# Privacy Policy — Coin ID

**Effective date:** April 30, 2026
**Developer:** Mustapha Marir — solo developer based in Morocco
**Contact:** [marirfam@gmail.com](mailto:marirfam@gmail.com)
**App package:** `com.marirfam.coinid`

This document describes what Coin ID collects, why, where it goes, and what your rights are. Plain English first; legal precision underneath.

---

## 1. What Coin ID does NOT collect

We lead with the things we deliberately *don't* do, because they're the most important.

- **No account, no email, no password.** Coin ID has no sign-up flow.
- **No personal data.** We don't ask for your name, age, address, phone number, contacts, or photo library.
- **No location.** We never request the location permission. We don't know where you are.
- **No analytics on your coin scans.** Your scan history is local to your device. We do not see what coins you've identified, what's in your collection, or how often you scan.
- **No cloud sync of your collection.** Your saved coins live in a local SQLite database on your phone. They never leave your device.
- **No selling or sharing of any user data.** We don't have a data broker pipeline because we don't have data to sell.

---

## 2. What Coin ID DOES process

### a) The image you capture during a scan

When you tap the scan button:

1. The image is compressed on your phone (target ~3.5 MB or smaller).
2. It is sent over HTTPS to our identification proxy at `https://coin-id-worker.marirfam.workers.dev` (a Cloudflare Worker we operate).
3. The proxy forwards the image to one of two AI providers — Cloudflare Workers AI (Llama 3.2 11B Vision) and/or Anthropic Claude Haiku 4.5 — for identification.
4. The identification result (coin name, year, country, mint mark, confidence) returns to your phone.

**The image is not stored.** Neither our proxy nor either AI provider retains it after the request completes. The proxy logs only request metadata (timestamp, request ID, latency, anonymous identification result for debugging) — never the image bytes.

**Anthropic's data retention:** Anthropic's enterprise/API terms specify that API content is not used to train models and is retained only as required for operational purposes. See [https://www.anthropic.com/legal](https://www.anthropic.com/legal).

**Cloudflare's data handling:** Cloudflare Workers AI processes inputs in-region without long-term retention. See [https://www.cloudflare.com/privacypolicy/](https://www.cloudflare.com/privacypolicy/).

### b) Play Integrity attestation

When you scan a coin, your phone generates a Play Integrity token via the Google Play Integrity SDK. We send this token to our proxy alongside the image. The proxy verifies the token to confirm your app installation is genuine (anti-abuse). The token contains no personal information about you.

### c) Anonymous rate-limit identifier

Our proxy rate-limits requests by hashing the Play Integrity attestation token. We never store the raw token, your device ID, or any persistent identifier across sessions.

### d) Crash and error reports (Sentry)

The app uses Sentry to capture crashes and unhandled exceptions. Sentry receives:

- A stack trace.
- The OS version, app version, device model.
- A randomly-generated install ID (rotates if you reinstall).

Sentry does **not** receive your scan history, your saved coins, your name, or any other personal info. See [https://sentry.io/privacy/](https://sentry.io/privacy/).

### e) Advertising (AdMob)

Coin ID is supported by ads from Google AdMob.

- Ad content is selected by AdMob.
- AdMob receives device-level signals (Android Advertising ID, language, country, screen size, broad app context) so it can serve and measure ads.
- In the EU/UK/Switzerland we present a Google UMP consent form on first launch where you choose between **personalized** and **non-personalized** ads. Outside those regions, ads default to non-personalized.
- You can change this choice anytime via **Settings → Privacy preferences**.

Google's data handling for AdMob: [https://policies.google.com/technologies/ads](https://policies.google.com/technologies/ads).

### f) Firebase Remote Config

We use Firebase Remote Config to toggle features without app updates (e.g., adjust ad frequency in an emergency). Firebase Remote Config sees your install ID, app version, and device model, but no personal data.

Firebase data handling: [https://firebase.google.com/support/privacy](https://firebase.google.com/support/privacy).

### g) Numista API (planned for v1.2+ catalog top-ups)

For now (v1.1) the entire coin catalog ships pre-bundled inside the app. No runtime requests to Numista happen on your device. If we ever switch to live Numista lookups (planned for v1.2), this section will be updated and you'll see it in the app's update notes.

---

## 3. Children

Coin ID is rated for general audiences. We do not knowingly collect data from children under 13 (under 16 in the EU) and we comply with COPPA / GDPR's child-data provisions. The app is appropriate for any age.

---

## 4. Your rights

Because we don't store personally identifying data, most data-rights requests don't apply — there's nothing under your name to delete or export. That said:

- **Delete your local data:** uninstall the app. SQLite + cached scrape data are removed by Android.
- **Withdraw ad-personalization consent (EU/UK/CH):** Settings → Privacy preferences.
- **Reset Advertising ID:** Android Settings → Privacy → Ads → Reset advertising ID.
- **Contact us** at [marirfam@gmail.com](mailto:marirfam@gmail.com) about anything else and we'll respond within 30 days.

---

## 5. Where data goes (legal basis under GDPR)

- **AI identification (image):** contractual necessity — to deliver the service you requested by tapping the scan button.
- **Play Integrity:** legitimate interest in preventing abuse.
- **Sentry crash reports:** legitimate interest in fixing app bugs.
- **AdMob personalized ads:** only with your consent (UMP form in EU/UK/CH).
- **AdMob non-personalized ads:** legitimate interest in funding free distribution.

Data is processed by:

- Anthropic, PBC (US) — for fallback identification
- Cloudflare, Inc. (US) — for hosting the proxy and primary AI
- Google LLC (US/EU) — for AdMob and Firebase
- Sentry, Inc. (US) — for crash reporting

We rely on the EU-US Data Privacy Framework or Standard Contractual Clauses for transfers from EEA users.

---

## 6. Changes to this policy

If we materially change what data we collect or how it's used, we'll bump the "Effective date" above and surface a notice in the app on the next launch. If we ever add account login, cloud sync, or any new third-party processor, that will trigger an update.

---

## 7. Contact

For privacy questions or data-rights requests:

- **Email:** [marirfam@gmail.com](mailto:marirfam@gmail.com)
- **Subject line:** include "Coin ID privacy" so it routes correctly.

This is a solo-developer app — replies come from Mustapha himself, usually within a few days.

---

*Coin ID is built and supported by one developer. Thank you for using the app.*
