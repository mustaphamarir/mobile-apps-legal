# Legal & privacy — Mustapha Marir mobile apps

Public-facing legal documents (privacy policies, terms) for the mobile
apps I publish on Google Play. Hosted via GitHub Pages so each app's
Play listing has a stable URL.

## Apps

| App | Privacy policy |
|---|---|
| Coin ID | [/coin-id/](https://mustaphamarir.github.io/mobile-apps-legal/coin-id/) |

## Adding a new app

1. Create a directory `<app-slug>/` at the repo root
2. Drop `index.md` inside with the policy content
3. Add the row to the table above
4. Push — GitHub Pages rebuilds in ~30 seconds

The URL pattern is always `https://mustaphamarir.github.io/mobile-apps-legal/<app-slug>/`.

## Why this is a single repo

- One GitHub Pages site, one DNS / CDN setup
- Each app gets a clean per-app URL via subdirectory
- Adding a new app = creating a new folder
- Updating a policy = bumping the effective date + `git push`
- Free forever on GitHub's `*.github.io` hosting
