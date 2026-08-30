# Timewarrior Dashboard

Interactive analytics dashboard for [Timewarrior](https://timewarrior.org) time-tracking data.

## Quick Start

**View on GitHub Pages:**

1. Push this repo to GitHub
2. Go to **Settings → Pages** → select `main` branch, root folder → Save
3. The dashboard opens at `https://<user>.github.io/<repo>/`

**Local:**

```bash
python3 -m http.server 8080
# Open http://localhost:8080
```

## How It Works

The dashboard (`index.html`) automatically loads `all-time.json` on open. No manual file upload needed — just open the page and the data renders immediately.

### Features
- **Overview** — stats, activity heatmap, charts, tag bars
- **Sessions Log** — searchable/sortable table with CSV/JSON export
- **Goals & Insights** — daily/weekly targets, productivity analysis
- **Themes** — Nordic Emerald, Cyberpunk Neon, Steel Slate

## Generating Data

```bash
timew aggregate all-time report --annotations --finalized --color --bw > all-time.json
```

Or copy your Timewarrior JSON export into `all-time.json`.
