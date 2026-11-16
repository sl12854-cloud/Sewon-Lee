# EventStay AI Build 2 — No-key NYC Events API

## Run locally on Mac
1. Unzip this folder.
2. Open Terminal, type `cd ` (with a space), drag this folder into Terminal, then press Enter.
3. Run: `python3 -m http.server 8000`
4. Open http://localhost:8000/ in Chrome or Safari.
5. Select **New York City**, set a near-future date (within one month), and click **Fetch real NYC events**.
6. Take a screenshot with real records visible and add it to your Product Page.

## What is real vs sample?
- Real: NYC permitted-event records from https://data.cityofnewyork.us/resource/tvpp-9vvx.json
- Sample: fictional hotels, hotel prices, event-demand factors in the original comparison.
- New York live permitted events are fetched separately and DO NOT affect the hotel price estimates.
- NYC public permit dataset does NOT cover all conferences, concerts or festivals.
- No API key and no paid API required (basic calls are rate-limited).
- This is **API integration**, not AI forecasting.

## Install PostHog (separate Build 2 requirement)
Paste your PostHog web snippet inside the `<head>` of this local `index.html` AND `docs/index.html` (Product Page). Enable/verify pageview, click and Session Replay; mask sensitive input. Never upload private credentials. The `real_events_search_completed` event is sent if PostHog is installed and an API search succeeds.

## Publish
For the class GitHub repository, keep `docs/index.html` (PRD + Product Page) untouched while copying this file to `docs/prototype/index.html`, or keep this folder locally and showcase a screenshot of the local app. Note: GitHub Pages can serve static HTML but cannot host a Python backend; this version uses a keyless browser-to-API call.

## Test checklist
- [ ] New York + next-week date returns real API data (possibly zero results)
- [ ] Chicago selection explains NYC-only limitation
- [ ] Sample hotels still work
- [ ] Product Page shows screenshot or recording
- [ ] PostHog verified on both pages
- [ ] PRD v2, AGENTS.md and build log updated
