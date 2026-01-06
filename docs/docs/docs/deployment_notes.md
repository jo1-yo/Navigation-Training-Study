# Deployment Notes (Study Link + Code)

This project is distributed via study links and gated by study codes (not published on public app stores).

## How study links work (planned)
- Base URL: `https://<your-domain-or-host>/`
- Participant opens: `https://<host>/?study=<study_id>`
- App prompts for `study_code` and validates it before starting tasks

## How study codes are created (choose one approach)
Option A — Pre-generated codes
- Researcher generates a list of valid codes for a study
- Codes are stored server-side (hashed if possible)
- Participant enters code → server validates

Option B — Single shared code (simplest, less secure)
- One code per study condition/batch
- Useful for pilots; avoid for large studies

Option C — One-time codes
- Each participant gets a one-time code
- Code is invalidated after session start

## Data export (planned)
- Export endpoint: `/export` (researcher-only)
- Export formats: CSV/JSON
- Export includes timestamps, trial metadata, and event/sensor logs
