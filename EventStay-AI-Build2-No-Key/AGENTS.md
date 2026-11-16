# EventStay AI — Build 2

## Purpose
Customer-facing prototype comparing illustrative hotel room scenarios while fetching actual NYC permitted events.

## Project structure
- `index.html`: responsive app, example pricing logic and keyless NYC Open Data fetch.
- `README.md`: local setup instructions, limitations and checklist.
- `AGENTS.md`: this file.

## Run
From this directory run `python3 -m http.server 8000` and visit `http://localhost:8000/`. Python 3 and internet required, no dependencies or API key.

## Data and costs
The publicly accessible NYC SODA API is `https://data.cityofnewyork.us/resource/tvpp-9vvx.json`. Anonymous requests are subject to lower limits. Direct per-request API charge: $0 for this prototype's eligible public endpoint usage; other project costs must be measured separately.

## Guardrails
- Never imply that real event records drive the fictional hotel rate estimator.
- Never claim this covers every NYC concert or convention.
- Do not commit API secrets or private PostHog configuration.
- Verify PostHog pageviews, clicks and replay separately on local app and Product Page.
- Keep `docs/index.html` as the PRD/Product Page when publishing.
