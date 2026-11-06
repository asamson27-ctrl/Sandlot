# Sandlot — San Francisco

Source export of the published Sandlot pickup-baseball app, version 13, from Sites commit `64f7d75ef558367ac98e6fe59d63a1eb48718d47` (November 6, 2026).

Live site: https://sandlot-sf.asamson27.chatgpt.site/

## Development

Use Node.js 22.13 or newer. Run `npm ci`, then `npm run build`. Follow the local D1 migration instructions in README.md to apply the SQL files in `drizzle/` in numerical order, then run `npm run dev`. The existing README contains detailed runtime and local sign-in instructions.

## Hosting and data

This repository contains the application code, static photos and map assets, dependency lockfile, database schema and migrations, and build tooling. Generated build caches, installed dependencies, credentials, live database records, and user-uploaded photos are not included.

The app currently runs on Sites with Cloudflare D1 (`DB`) and R2 (`BUCKET`). Production sign-in relies on the Sites platform's trusted identity headers and sign-in routes. Moving production hosting to another provider requires configuring storage and authentication; GitHub Pages alone cannot run this full-stack app. The existing Sites deployment remains live. Pushing to GitHub does not automatically update that deployment.

See `public/photos/credits.txt` and the bundled license files for asset attribution.
