# AI Use Disclosure — Setup Exercise: Your Search's Personal Layer

**Student:** Priyesh Modi · **Course:** INFO 7375 — Computational Skepticism for AI · **Date:** 2026-10-29

## Summary

I used an AI coding agent to extract my resume into structured data, draft my search profile from my intake answers, and draft a gap analysis from three job postings I chose. I did the attesting and correcting: I found and fixed three errors in the resume extraction, answered every profile question myself, killed one gap the agent got wrong, rewrote the gap that matters most to me in my own words, and confirmed the visa and occupation fields. The clearest place the AI failed was a gap it raised about incident management, which I had done in my co-op but had never written down.

## What the AI did

- **resume.json:** extracted my resume PDF into typed records (one per job, project, degree, certification, skill group; dates as year-month) and left fields it could not source as empty rather than guessing.
- **profile.yml:** drafted the file from my answers to the five intake questions and marked open items for me to decide (level, remote preference, what "good funding" means, DSO confirmation, whether OPT dates were approved).
- **gaps.md:** fetched the job postings I gave it, quoted their requirements, compared them with my attested resume, and drafted a gap table with evidence, what I have, and a plan with a checkable closing condition for each gap. It proposed an occupation (SOC) code from the repository's local O*NET file.
- **Gate checks:** it flagged that two postings I supplied failed my own rules — Black Kite ("not eligible for visa sponsorship") and Booz Allen ("Secret clearance is required"; defense) — and kept their requirements out of the evidence.
- **Log:** drafted the RUN_LOG entry from the session; I supplied the verification-check answers.
- **Formatting and validation:** ran the repository's conformance check on every file.

## What I did

- **Attestation of resume.json — three errors I identified and corrected:**
  1. The summary claimed GCP and OCI experience that none of my jobs or projects supports — removed.
  2. The PanAgora Azure Functions budget-enforcement work read as if I did it alone or led it. It was team work; I restated it as a team contribution and marked the $5K/month saving as a team outcome.
  3. Snowflake and Oracle were listed as skills I cannot defend in an interview — removed.
- **Profile:** answered all intake questions; decided level (new grad to early career), work arrangement, the Series B funding floor, and the defense exclusion; confirmed STEM eligibility with my DSO by email; confirmed the SOC code and OPT dates.
- **Gaps:** chose the postings (and replaced one after the agent showed it failed my gates), killed one row with a reason, and rewrote one row in my own words with my own plan and closing condition.
- **Decided what is public:** reviewed what goes into the tracked log and approved naming employers.

## What the AI could not do

- **It treated "not written down" as "not done."** The agent drafted a gap for incident management and troubleshooting ownership because neither word appears on my resume. I had done this work during my PanAgora co-op — handling API outages and LLM quota overruns, sometimes as part of the team and sometimes as the person who found the root cause. Only I knew that. I killed the row, and we added the work to my resume record so a screener can see it.
- **It could not tell whether my experience was solo or team work.** The resume said "Developed …" for the Azure Functions work, and the extraction kept that wording faithfully. Only I knew it was a team effort.
- **It could not judge which skills I can actually defend.** It extracted Snowflake and Oracle as skills because the resume listed them; whether I could back them up in an interview was my call.
- **It could not know my visa facts.** Whether my OPT dates were requested or approved, and whether my DSO had confirmed STEM eligibility, came from my documents, not from the agent.

## Where I checked the AI

- The agent's interpretations that I reviewed rather than accepted blindly: the SOC code (its best match from local data, which I then confirmed) and the unemployment buffer (read as "be employed by day 80 of 90").
- The agent assumed which posting my Booz Allen link was replacing; I made the final choice of postings (Dentsply Sirona, Akamai, Egofold).
- My own first rewrite of my top gap described an activity ("study backend development again and build more projects"). The agent pointed out that this had no checkable closing condition, and I restated it as an output: a public Python/FastAPI repo with an API spec, tests and a database, which closes when it has passing CI and a documented deployment.
