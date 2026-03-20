# Presque Cool — App Store

App catalog for [WVW (World Vibe Web)](https://wvw.dev/), the distributed app store for vibe-coded apps.

## What is this?

This repo hosts the `apps.json` file that declares all Presque Cool apps to WVW. The WVW indexer fetches this file every 6 hours to update the store listing.

## How it works

1. `apps.json` follows the [WVW apps schema](https://wvw.dev/apps.schema.json)
2. This repo is registered in [wvw.dev/stores.json](https://github.com/nicedoc/wvw.dev/blob/master/stores.json)
3. WVW pulls `apps.json` from this repo on a regular cycle

## Adding or updating an app

Edit `apps.json` and follow the existing structure. Required fields per app:

- `id` — kebab-case identifier
- `name` — display name
- `subtitle` — one-liner tagline
- `description` — short description
- `category` — array of [valid WVW categories](https://github.com/nicedoc/wvw.dev/blob/master/DISTRIBUTE.md)
- `platform` — `"Web"` for all current apps
- `price` — `"Free"` for all current apps
- `github` — public repo URL
- `homepage` — live URL

Optional: `icon`, `iconEmoji`, `longDescription`, `features`, `language`.

## Icons

When `icon` is `null`, WVW auto-generates a skeuomorphic icon using the `iconEmoji` fallback. To use a custom icon, set `icon` to a direct URL (PNG or SVG, 512x512 recommended).

## Links

- Store: [presque.cool](https://presque.cool/)
- WVW: [wvw.dev](https://wvw.dev/)
- Distribution spec: [DISTRIBUTE.md](https://github.com/nicedoc/wvw.dev/blob/master/DISTRIBUTE.md)
