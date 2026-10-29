# Gaps — attested record vs. target role

## Executive summary

This file lists what the jobs I am targeting ask for that my verified record does not yet show. Each gap cites a real job posting or the U.S. government's occupation database, and each comes with a plan whose result someone else could check. Eight gaps were drafted; seven remain. The ones raised by more than one posting are Linux systems administration and years of experience in a reliability or platform role. One drafted gap, incident management, was removed by me because I have done that work. The postings also raised a question about my profile rather than my skills: none of the three is a new-grad role and none is fintech or e-commerce, so I widened my target profile.

**Status:** agent draft, 2026-10-29, with owner edits done: one row killed (with reason), one row rewritten in my own words.

## Sources

Three postings supplied by me. Requirements below are quoted from the postings. P1 and P2 were fetched from the employer's site on 2026-10-29; P3 was pasted as text (no URL or posting date), so its liveness is unchecked.

| ID | Role · Company | Location | Posted | Level asked | Sponsorship / authorization text | Pay (base) |
|---|---|---|---|---|---|---|
| P1 | Site Reliability Engineer II · Dentsply Sirona (req 84206) | Waltham, MA; in office "multiple days" | 2026-10-22 | "2-4 years of work experience in a Site Reliability Engineering/ Platform Engineering/ DevOps role or similar" | "All successful applicants must be eligible to work in the country the position is based." No sponsorship statement. | $115,000–$130,000 |
| P2 | Site Reliability Engineer II · Akamai (job 2687) | US remote (Cambridge, MA Flexbase) | 2026-03-30 | "2+ years of experience in Site Reliability Engineering" | No sponsorship statement; requisition fields: citizenship required = No, clearance required = No | $95,000–$171,000 |
| P3 | DevOps / Backend Engineer (Junior to Mid-Level) · Egofold (backed by Snail Inc.) | Culver City, CA; also open in San Francisco and New York (location chosen in the application, per me); hybrid, 1–2 days onsite per week | not stated (pasted text) | "Junior to Mid-Level"; "Professional backend engineering experience" (no year count) | No sponsorship statement | $110,000–$145,000 |

Occupation reference: O*NET-SOC **15-1299.08 Computer Systems Engineers/Architects** (local file `data/bls/compact/soc_occupation_compact.csv`; alternate titles include Cloud Engineer, Cloud Infrastructure Engineer, Cloud Platform Engineer; programming skill level 4.25, systems analysis 4.0). Agent judgment: this is the closest local SOC match for DevOps / platform / SRE titles; "DevOps" and "SRE" are not in the local alternate-title sample. Confirmed by me on 2026-10-29.

Postings considered and set aside (they fail my profile's own rules, so their requirements are not used as evidence):
- Black Kite, Junior DevOps Engineer, Boston: "This position is not eligible for visa sponsorship" (fails the sponsorship gate).
- Booz Allen Hamilton, DevOps Engineer R0249846, Lexington MA: "Secret clearance is required" (fails the citizenship / clearance / defense exclusion).

Observations about the postings themselves (not skill gaps):
- None of the three is a new-grad role or a fintech / e-commerce company. P1 and P2 are level II roles asking for 2+ years; P3 is junior-to-mid. My profile says new grad, fintech and e-commerce. **Resolved 2026-10-29:** profile updated to new-grad to early-career (0-3 years), with fintech / e-commerce preferred rather than required.
- P3 is listed in Culver City, CA; the same posting is also open in San Francisco and New York, both target metros, with the location chosen during the application (my account; the pasted text names only Culver City).
- P2 was posted seven months ago; still listed with no end date, but not confirmed live.

## Gap table

| # | Gap | Evidence the target demands it | What I have | Plan to close it (closes when …) |
|---|---|---|---|---|
| G1 | Go programming | P1: "Programming language proficiency (Go, C++, Python)". P2 accepts "Python or Go"; P3 accepts "Python, Go, or a comparable backend programming language". So only P1 might require Go, and P1 may mean any one of the three. | Python, C#, PowerShell, Bash. No Go in any role or project. | Write and publish a small Go tool used by my own infrastructure (e.g. a Prometheus exporter or a Kubernetes controller) with tests and CI. **Closes when** the public repo has a tagged release with passing CI; then add it to `resume.json` projects. |
| G2 | Hands-on Google Cloud (GKE, Cloud SQL, IAM) | P1: "Cloud architecture (GCP, AWS)". | GCP is listed in my skills with no services; no job or project used it (GCP was removed from my summary during attestation for this reason). AWS and Azure are evidenced. | Redeploy the MERN platform project to GKE + Cloud SQL with Terraform, in a public repo. Optionally pass Google Associate Cloud Engineer. **Closes when** the repo shows a working `terraform apply` for GKE and Cloud SQL (README with output and a teardown), or a Google credential with a verification URL exists. |
| G3 | GitOps deployment (Flux / ArgoCD) | P1: "CI/CD pipelines (Github Actions, Flux, ArgoCD)". | Jenkins, GitHub Actions, Azure DevOps pipelines (push-based). No pull-based GitOps tool in any role or project. | Add ArgoCD to the G2 cluster so deploys come only from a git repo; demonstrate a sync and a rollback. **Closes when** the public repo contains the ArgoCD Application manifests and a README walkthrough of a rollback. |
| G5 | Linux systems administration | P2: "Have experience with Linux systems administration". P3: "Practical experience with databases, Linux environments, Git, cloud platforms, and containerization technologies such as Docker". | Bash scripting (BitBlue); Packer golden images for build agents (PanAgora). No role states Linux administration explicitly. | Pass a performance-based Linux exam (LFCS or RHCSA). **Closes when** the credential ID is verifiable on the issuer's site. |
| G6 | Datadog | P1: "Monitoring and observability (Datadog, Grafana)". | Grafana (PanAgora, Epicure), Prometheus (Epicure), Log Analytics (PanAgora). No Datadog. | Instrument the G2 cluster with the Datadog agent and build a service dashboard and monitors. **Closes when** screenshots and the monitor definitions (as code) are in the public repo. |
| G7 | Backend service development (designing and building APIs) — *rewritten in my own words* | P3: "Professional backend engineering experience with demonstrated ability to independently develop and maintain production-quality software"; "designing and integrating APIs and backend services". This is the gap that really matters to me. | My work experience is mostly around cloud / DevOps, with very little backend work done by me alone in a professional environment. I have done backend and full-stack projects, but I have lost touch with it. (Those projects are not on my resume and are not in this record yet.) | Study backend development again and build more projects around it. I will build a Python/FastAPI service with an API spec, tests and a database, deployed through CI/CD. **Closes when** the public repo has passing CI and a documented deployment. |
| G8 | Two-plus years in an SRE / platform role | P1: "2-4 years of work experience in a Site Reliability Engineering/ Platform Engineering/ DevOps role or similar". P2: "2+ years of experience in Site Reliability Engineering". | About 26 months in DevOps roles: BitBlue full-time (2023-08 to 2024-08, ~13 months), PanAgora co-op (2026-01 to 2026-08, ~8 months), Epicure internship (2023-01 to 2023-05, ~5 months). Only ~13 months full-time; no SRE title. | No project closes this; it closes with documents. **Closes when** employment verification letters (dates and duties) for BitBlue and PanAgora are on file, making "2+ years DevOps" defensible to a screener. Until then, the claim is "~2 years including co-op and internship." |

## Owner edits

- **Killed row — G4, Incident management and troubleshooting ownership.** The agent read the absence of the words "incident" and "on-call" on my resume as absence of the experience: I did incident management and troubleshooting during my PanAgora co-op, it was simply never written down because it is a basic, assumed part of the job.
  - Removed row, kept for the record: evidence was P1 "Incident management", "Troubleshooting"; P2 "the ability to troubleshoot complex infrastructure issues"; P3 "take ownership of technical problems from investigation through resolution".
  - Follow-up done 2026-10-29: because a screener only sees what is written, a PanAgora highlight now records the work in `resume.json` (incident response for API outages and LLM quota overruns; team member, and root-cause finder on some incidents).
- **Rewritten row — G7, Backend service development.** Restated in my own words: my professional experience is cloud / DevOps, with very little backend work done by me alone; I have backend and full-stack projects but have lost touch with it.
