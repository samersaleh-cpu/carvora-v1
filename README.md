# CARVORA V1

CARVORA is a mobile-first vehicle intelligence web app built with plain HTML, CSS and JavaScript.

## V1 features
- Vehicle Profile
- Car Health Score
- Maintenance Tracker with add, edit and delete
- Smart Priorities generated from maintenance status and mileage
- Ownership Cost Calculator with monthly, annual and cost-per-km estimates
- LocalStorage persistence
- Public free ownership-cost calculator at `calculator.html`
- Clear Free / Pro product structure
- Responsive mobile-first interface
- No external dependencies or build step

## Run locally
Open `index.html` in a browser. No framework, package manager or build step is required.

## Public pages
- `index.html` — CARVORA dashboard
- `calculator.html` — public free ownership-cost calculator

## Deploy
A GitHub Actions workflow is included at `.github/workflows/pages.yml` for GitHub Pages deployment from `main`. GitHub Pages must be enabled for the repository with the Actions-based Pages source.

## Data and privacy
V1 stores vehicle, maintenance and calculator data locally in the user's browser using `localStorage`. There is no backend, account system or payment processing in V1.

## Product model
The Free experience provides the core dashboard and calculator. Pro is represented as product scaffolding only; no fake checkout or subscription flow is included.

## Roadmap
1. Multiple vehicles
2. Service history and cost analytics
3. Export / import
4. Reminder notifications
5. Authentication and cloud sync
6. Real Pro billing
7. Advanced vehicle-health recommendations

Health scoring and cost calculations are informational estimates and are not a mechanical diagnosis.