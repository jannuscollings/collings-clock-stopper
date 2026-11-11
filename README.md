# Collings Clock Stopper — staging starter

A small Vite static app for a ten-second clock-stopping game. This starter uses placeholder branding and a **local-only leaderboard demonstration**. It is not yet production-ready or a shared leaderboard.

## Run locally

```sh
npm install
npm run dev
```

## Publish to GitHub

Create a **private** repository named `collings-clock-stopper` in the intended Collings GitHub organization, then run:

```sh
git init
git add .
git commit -m "Initialize Clock Stopper staging"
git branch -M main
git remote add origin <YOUR_PRIVATE_REPO_SSH_OR_HTTPS_URL>
git push -u origin main
git checkout -b develop
git push -u origin develop
```

## Render staging

1. Connect Render to the GitHub organization and grant this repo access.
2. In Render, create a new **Blueprint** from the GitHub repo. Render detects `render.yaml`.
3. Confirm staging is deploying from `develop`. Confirm the build logs and actual Render URL.
4. Share the staging URL only after testing it.

## Before release

- Implement a shared, server-validated leaderboard with database persistence; localStorage here is only an isolated demo.
- Decide ties, duplicate names, daily vs all-time leaderboard, abuse/rate limiting, and data retention.
- Replace colors and type with approved Collings brand assets.
- QA on iOS Safari/Android, keyboard inputs, and reset behavior.
