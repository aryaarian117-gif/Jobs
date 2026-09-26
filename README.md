# Job Desk

Private job-search tracker for a biotech operations → business career move.

- **Live app:** published as a private Claude artifact (only the owner can open it).
- `tracker/index.html` — the app source. Tabs: **Matches** (listings scored for fit to the CV) and **Apply** (stage, applied / follow-up / interview dates, cover letter drafts, resume tailoring notes, timeline), **Passed** (jobs you x out; restorable), plus **Add a job**. Any application can go back to Matches or to Passed.
- `data/` — seed data written to the app's database: `profile.json` (CV summary + search criteria) and `jobs/*.json` (one file per listing).

Search criteria: Houston, TX or remote · base salary ≥ $100k (flag ranges within 5%) · business roles, ideally where they meet GMP manufacturing / MSAT.

Salary badges: **meets floor** (min ≥ $100k), **reaches $100k** (range spans it), **within 5%** (top ≥ $95k), **not posted**.
