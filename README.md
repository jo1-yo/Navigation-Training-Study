# Navigation Training Study App (Code-Gated)

A controlled-access, link-based research web app for navigation-training studies. Participants receive a study link and enter a study code to start standardized, trial-based tasks. The system logs sensor and event streams with timestamps for downstream behavioral analysis.

## Study Flow
1. Researcher distributes a unique study link
2. Participant enters a study code
3. System runs standardized tasks (trial-based)
4. Events + sensor streams are logged with timestamps
5. Data are exported as CSV/JSON for analysis
6. (Optional) Admin view supports monitoring completion / dropout

> This project is intentionally **not publicly deployed**; access is restricted via study codes to preserve experimental control.

## What’s in this repo
- `docs/` — study design notes, logging schema, and deployment notes
- `sample_data/` — example (synthetic) exports for demonstration
- `analysis/` — (optional) QC checks and analysis notebooks/scripts

## Tech Stack (edit this to match)
- Frontend: (e.g., React / Next.js / plain JS)
- Backend: (e.g., Node.js / Express)
- Storage: (e.g., MongoDB / file export)

## Data & Privacy
- No real participant data should be committed to this repository.
- Use synthetic or anonymized examples only (see `sample_data/`).

## Quickstart (edit to match your setup)
```bash
# install
npm install

# run locally
npm run dev
