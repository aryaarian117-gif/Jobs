# Job Desk

Private job-search tracker for a biotech operations → business career move.

- **Live app:** published as a private Claude artifact (only the owner can open it).
- `tracker/index.html` — the app source. Tabs: **Matches** (listings scored for fit to the CV) and **Apply** (stage, applied / follow-up / interview dates, cover letter drafts, resume tailoring notes, timeline), **Passed** (jobs you x out; restorable), plus **Add a job**. Any application can go back to Matches or to Passed.
- `data/` — seed data written to the app's database: `profile.json` (CV summary + search criteria), `watchlist.json` (companies whose career sites the daily search checks) and `jobs/*.json` (one file per listing).

Daily search sources: Indeed, ZipRecruiter, company career sites (Greenhouse, Lever, SmartRecruiters, Workable, Workday; needs those hosts allowed in the environment network settings), Gmail job-alert emails (needs the Gmail connector), and targeted web search.

Search criteria: Houston, TX or remote · base salary ≥ $100k (flag ranges within 5%) · business roles, ideally where they meet GMP manufacturing / MSAT.

Fit (0–100): hard gates first (location, pay, degree, seniority ≤ Associate Director, no commission sales, years), then Required qualifications 50 · Experience 15 · Preferred 15 · Direction 20. Capped at 75 when requirements come from a summary, 60 when unverified. Matches cutoff: 70.

Salary badges: **meets floor** (min ≥ $100k), **reaches $100k** (range spans it), **within 5%** (top ≥ $95k), **not posted**.
