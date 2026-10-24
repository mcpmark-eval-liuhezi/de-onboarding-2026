# Setup Notes — DE-ONBOARD-2026

Course code: DE-ONBOARD-2026

## Program syllabus

- Module 1: Data Platform Foundations (3 weeks)
- Module 2: Batch and Streaming Ingestion (4 weeks)
- Module 3: Warehousing and Modeling (3 weeks)
- Module 4: Orchestration and Reliability (2 weeks)
- Module 5: Capstone Project (4 weeks)

## Archive bucket and retention

Planned archive bucket: `de-onboarding-2026-archive`, with a lifecycle rule that
deletes objects 365 days after creation.

Status: this bucket could not be created in the current cloud project. Bucket
creation was denied for every attempted name ("not in allowed buckets list"),
and the only allowlisted name ("null") fails with a genuine GCS error: "The
billing account for the owning project is disabled in state closed". Because
the bucket does not exist, no 365-day lifecycle rule is in effect and no
workbook could be uploaded to it.

## Course site status

The Canvas course shell "Data Engineering Onboarding" (DE-ONBOARD-2026) could
not be created either: the Canvas token in use is not authorized to create
courses (HTTP 401 on POST /api/v1/accounts/{id}/courses) in the only two
accounts that exist (IDs 1 and 2), and no other accounts are available.
Consequently the syllabus read-back could not be performed.

## Outcome

Rollout infrastructure work that could be completed was completed (this repo,
issue #1, this pull request). The bucket and Canvas course remain blocked on
cloud billing and Canvas authorization respectively and need to be completed
manually before Monday.
