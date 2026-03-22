# RS3 Archaeology Material Counter

An [Alt1 Toolkit](https://runeapps.org/alt1) plugin for tracking archaeology materials in RuneScape 3 via chatbox reading.

## Features

- **ChatBox Reading** — Automatically detects materials from chat messages (normal finds, auto-screener, familiar, porter/imp-souled, bank)
- **Fortune Perk & Balarak** — Correctly handles 2x and 4x multipliers
- **Artefact Calculator** — Plan restorations with material requirements and XP totals (data fetched from RS Wiki)
- **Live Rate Tracker** — Mats/hr with sparkline graph and elapsed time
- **Progress Bars** — Visual goal progress behind each material row
- **Alt1 Overlay Notifications** — Goal completion alerts on the game screen
- **Dig Site Auto-Detect** — Filters materials based on detected dig site from chat
- **Time-to-Goal Estimates** — ETA for each material goal based on current rates
- **Compact Mode** — Minimal UI for smaller windows
- **Session History** — Logs past sessions with breakdowns and rates
- **Sound Alerts** — Audio chime on material find and goal completion
- **Material Pinning** — Pin favorite materials to the top of the list
- **Collection Log** — Track progress across artefact collections
- **CSV Export** — Export material data to spreadsheet
- **Search & Filter** — Find materials quickly with Ctrl+F or filter by quantity/goals

## Install

### From GitHub Pages

Click the link below inside Alt1's built-in browser, or paste it into Alt1's URL bar:

```
alt1://addapp/https://YOUR_USERNAME.github.io/rs3-arch-mat-counter/appconfig.json
```

Replace `YOUR_USERNAME` with your GitHub username.

### Local Testing

```bash
python -m http.server 8080 --bind 127.0.0.1
```

Then add to Alt1:

```
alt1://addapp/http://localhost:8080/appconfig.json
```

## Files

| File | Purpose |
|------|---------|
| `index.html` | Complete self-contained plugin (HTML + CSS + JS) |
| `appconfig.json` | Alt1 app manifest |
| `icon.png` | App icon |

## Tech

- Single-file HTML — no build step, no dependencies beyond Alt1's CDN scripts
- Material and artefact data fetched live from the [RS3 Wiki API](https://runescape.wiki/api.php) with localStorage caching
- Web Audio API for sound alerts
- Alt1 overlay API for in-game notifications

## License

MIT
