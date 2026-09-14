# advent-light-table

Brilliantio Advent cover **priority cockpit** — Mastermind WA share (craft eye-on only; not list-ready).

## Live site

https://brilliantio.github.io/advent-light-table/

## Architecture (Paul 14 Sep HARD RULE)

- **GitHub Pages** hosts thin HTML + JSON only
- **Cloudinary** folder `advent-light-table/` serves all cover JPGs via `secure_url`
- Do **not** commit image blobs to this repo

## Files

| File | Purpose |
|------|---------|
| `index.html` | Gallery UI (grid, priority queue, drawer) |
| `cards.json` | Concept metadata, priority ranks, Linear links |
| `cloudinary-map.json` | Filename → Cloudinary `secure_url` map (James supplies) |

## CDN map follow-up

When James delivers the Cloudinary URL map:

1. Replace `cloudinary-map.json` `images` values with real `secure_url`s
2. Set `"status": "live"` and `"updatedAt"` ISO timestamp
3. Add any missing concept rows to `cards.json` (target: **17 concepts**, excluding Laugh-Off + Impossible Questions)
4. Commit + push — Pages redeploys automatically

## Desktop SoR

Local eye-on gallery remains at `/Users/pauljenkins/Desktop/advent-light-table/` (BRI-3898).
