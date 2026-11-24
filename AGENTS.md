
# EventStay AI — AGENTS.md

## Project Overview

EventStay AI helps travelers understand how local events
may influence hotel prices and compare accommodation
options across different travel dates.

## Primary User

Travelers searching for affordable hotel accommodations.

## Core Workflow

Select destination, month and trip length → See the best check-in dates →
Compare crowd levels, weather, festivals and price levels day by day →
Open flights and hotels with the chosen dates.

## Tech Stack

- HTML
- CSS
- JavaScript
- NYC Open Data API
- PostHog Analytics
- GitHub Pages

## Project Structure

- docs/index.html: Product Page and PRD
- docs/prototype/index.html: Interactive application
- docs/prototype.png: Prototype screenshot
- AGENTS.md: Project instructions

## Run Locally

1. Clone or download the repository.
2. Open docs/prototype/index.html in Chrome or Safari.
3. Select a city and travel dates.
4. Click Compare stays.
5. Test the NYC Open Data API if available.

## Deployment

1. Open the GitHub repository.
2. Update docs/prototype/index.html.
3. Commit changes to the main branch.
4. Go to Settings > Pages.
5. Set Source to Deploy from a branch.
6. Select main and /docs.
7. Save and wait for deployment.
8. Visit the public URL and test the application.

## Data sources (all keyless, called from the browser)

The prototype (docs/prototype/index.html) is a best-travel-dates finder for Ibiza, Seoul and New York City.

- Weather: Open-Meteo. Forecast API for the next 16 days; Archive API (2016–2025, ±3-day window) for the 10-year average of later dates.
- Public holidays: Nager.Date (https://date.nager.at/api/v3/PublicHolidays/{year}/{ES|KR|US}). Ibiza also uses the Balearic regional holidays (county ES-IB).
- NYC events: NYC Open Data. Live permits (tvpp-9vvx, about the next month) and historical permits (bkfu-528j, the same weekday last year) are counted per day for permits with street closures or large public formats.
- Festivals: a curated list in the CITIES object. Recurring dates are marked "Typical dates" and must be confirmed each year.
- Flights and hotels: deep links to Google Flights and Booking.com with the dates filled in. No real prices on the page yet; a real flight API needs a secret key and a server-side proxy.
- Crowd and hotel price levels are EventStay estimates (season tables per city × weekend, festival, holiday and NYC permit effects). Keep them labeled as estimates.
- Serve over http (for example `python3 -m http.server` in docs/) rather than opening the file directly.

## Engineering Rules

- Never expose API keys or private credentials.
- Keep hotel prices labeled as illustrative data.
- Test the application after each deployment.
- Keep changes small and easy to review.
- Document known limitations and failures.

## Limitations

Hotel prices are illustrative rather than real-time.
NYC Open Data does not include every local event.
The application does not support hotel booking or payments.
