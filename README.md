# PARAS Estate Dashboards — Far East Bhd

Live site: https://fareast-paras.netlify.app (Netlify site "fareast-paras"). Copy of the Prosper build (paraslz/paras-estates); STANDARD.md is the house standard.

- `index.html` – portal: search and estate cards (reads `data/index.json`)
- `estate.html?e=<slug>` – shared dashboard template (reads `data/<slug>.json`)
- `group.html` – group summary, league table and action tracker
- `data/` – one JSON per estate, built from the latest PA and Agronomy reports (Drive folder "Far East Bhd")
- `kb/<slug>.txt` – report packs for the "Ask in Claude" box; `offline/<slug>.html` – downloadable copies

After any data change, from the repo root:
`python3 tools/build_index.py && python3 tools/build_kb.py && python3 tools/build_offline.py`, then commit and push. Netlify redeploys automatically.
