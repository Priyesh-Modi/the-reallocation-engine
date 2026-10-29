## 2026-10-29 — Setup exercise: personal search layer (search/)

### Executive summary

This is my log entry for the setup exercise that makes the job-search engine use my own record instead of a generic one. I built three files: my resume as structured data, my search profile (target role, visa timeline, locations, sponsorship), and a list of the skill gaps between my record and three real job postings. The AI drafted all three; I corrected them. I caught three errors in the resume extraction, removed one gap the AI got wrong, rewrote the gap that matters most to me, and corrected my target role after the postings I chose showed it was wrong.

### Run record

- **Built:** `search/resume.json` (attested), `search/profile.yml`, `search/gaps.md`. `search/private-notes.md` is gitignored, confirmed with `git check-ignore`. All files pass `node scripts/conformance.mjs`.
- **Where this entry lives:** the assignment asks for an entry in `logs/RUN_LOG.md`, but that file's header says students must not edit it and must add entries under `logs/runs/` instead, so the entry is here.

### Three attestation errors caught in resume.json

1. Summary claimed GCP and OCI cloud experience that no job or project supports — removed.
2. PanAgora co-op Azure Functions budget-enforcement work read as solo or led — restated as a team contribution; the $5K/month saving is marked as a team outcome.
3. Snowflake and Oracle listed as database skills I cannot defend — removed.

### Top gap

G7, backend service development (designing and building APIs). My professional work is cloud/DevOps with little backend work done by me alone. Closes when a public Python/FastAPI repo (API spec, tests, database, CI/CD) has passing CI and a documented deployment.

### Killed row

G4, incident management and troubleshooting. The agent read the absence of the words on my resume as absence of the experience; I did this work in my PanAgora co-op (API outages, LLM quota overruns; team member, and root-cause finder on some incidents). Follow-up: a highlight was added to resume.json so the record shows it.

### Corrected profile.yml fields

- `visa.ead_start_date` / `opt_end_date`: the first draft treated my OPT dates as fixed; they are the dates I *requested*, not approved EAD dates. Now marked `opt_dates_status: requested`, to be replaced with the EAD card dates once issued.
- `target_role.level` and `industry`: the first draft said new grad only, with fintech/e-commerce as primary sectors. None of my three target postings matched that (two SRE II roles asking 2+ years, one junior-to-mid; none fintech/e-commerce). Corrected to new-grad to early-career (0-3 years), fintech/e-commerce preferred, any sector except defense.

### Verification check

- **resume.json:** Yes — every job entry is traceable to something verifiable (offer letter, reference, or LinkedIn).
- **profile.yml:** Visa dates are requested, not approved, and are marked that way. STEM eligibility was confirmed by my DSO by email dated 2026-10-12, recorded in the profile.
- **gaps.md:** Every gap cites a posting fetched (Dentsply Sirona, Akamai) or pasted (Egofold) on 2026-10-29. Two postings were set aside under my own gates (Black Kite: "not eligible for visa sponsorship"; Booz Allen: "Secret clearance is required"). SOC 15-1299.08 was the agent's best match from the local O*NET file; I confirmed it. Egofold is listed in Culver City, CA but, by my account, the same posting is also open in San Francisco and New York (target metros; location chosen in the application); its liveness is unchecked because it was pasted without a URL.

### Gate

Attestation of resume.json and review of profile.yml and gaps.md by Priyesh Modi, 2026-10-29.
