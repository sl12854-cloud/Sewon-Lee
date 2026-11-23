
# EventStay AI — AGENTS.md

## Project Overview

EventStay AI helps travelers understand how local events
may influence hotel prices and compare accommodation
options across different travel dates.

## Primary User

Travelers searching for affordable hotel accommodations.

## Core Workflow

Select destination and dates → View local events →
Compare illustrative hotel prices → Explore alternative dates.

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
