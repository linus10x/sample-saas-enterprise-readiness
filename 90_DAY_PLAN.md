# SAMPLE: 90-day SaaS enterprise readiness plan

> **Illustrative sample by Kunjar Bhaduri, Bhaduri Advisory. Fictional organization and invented evidence only. No client relationship or confidential engagement material. Prepared with AI drafting assistance under my direction. Revised October 2, 2026 (America/Chicago).**

## Mandate and capacity

SpinCo is a fictional analytics spinout with partner feeds, automated reports, an early predictive feature and two or three engineers. The proposed mandate is to help close enterprise deals while making delivery and operations dependable. This is relevant to the [Sponsorship spinout CTO role](https://www.gofractional.com/job/fractional-cto-cmu7773s); it does not diagnose that company.

Assume 10-15 fractional leadership hours a week, an available engineering lead and 20-30 implementation hours a week from the existing team, agreed with the founder. That is about 130-195 leadership hours and 260-390 engineering hours across 13 weeks. The plan prioritizes within that capacity. Major SSO integration, a new tenant-isolation design or a data-platform rebuild requires a separate estimate. The founder approves the budget and customer commitments; engineering owns changes; sales supplies prospect requirements; the CTO coordinates and verifies.

Reserve two of the 10-15 CTO hours each week for hands-on technical development: a 45-minute review of a critical PR (tenant access, feed validation, rollback or model evaluation), a 45-minute pairing session with the engineering lead on one failing or missing test, and 30 minutes of mentoring and action follow-up. The remaining 8-13 leadership hours cover prioritization, prospects, roadmap and governance. Pairing also uses existing engineering capacity; it does not add another team. Keep a PR/test reference, the reasoning taught and a follow-up owner. By handoff, the engineering lead should independently reproduce the relevant negative test and explain the design decision. Record this as learning and control evidence, not merely meeting attendance.

By day 90, the selected enterprise requirements should have a verified answer or a clearly owned gap. The team should demonstrate release/rollback and recovery procedures, have a prioritized roadmap and know which security claims it can support. SOC 2, if commercially required, gets a scoped readiness plan agreed with an auditor. A Type II report depends on an examination of controls over an agreed period; this plan does not guarantee a report by day 90.

## Days 1-15: establish evidence and close urgent exposures

Review the last five available prospect questionnaires and the contracts that affect access, residency and recovery. Rank requirements by deal dependency, customer impact and implementation effort. Record missing artifacts rather than filling the answer bank with assumed controls.

Review production access, shared credentials and offboarding with the engineering lead. Revoke unnecessary access through the approved change process. Map services, feeds, vendor dependencies and tenant boundaries. Run the restore exercise below. Establish a baseline for feed freshness, failed jobs, deployment frequency and incidents. For the predictive feature, identify the target outcome, source rights, leakage risks and whether an evaluation exists.

Day-15 deliverables: an architecture/service map, evidence index, risk register and founder-approved backlog. Reserve immediate capacity for a failed restore, exposed credential or cross-tenant defect; revise other dates if needed.

## Days 16-45: implement the selected deal blockers

The team implements the top items in the agreed backlog. Typical candidates are named staff access/MFA, product roles and tenant checks, reviewed releases, tested rollback, feed contracts and freshness alerts. Choose work according to verified gaps; do not assume every item is a small configuration change.

The CTO attends selected prospect calls with sales and BI/data stakeholders, explains current capabilities, and records any new commitment before it enters the roadmap. For a predictive feature, establish a held-out, time-appropriate evaluation with product-approved quality thresholds, failure handling and model/data version records. Prevent target leakage and assess drift; do not ship on a training metric alone.

Day-45 acceptance: demonstrate the selected controls with negative tests, provide evidence for the corresponding questionnaire answers, and show which gaps remain. Founder and engineering lead approve the residual-risk register.

## Days 46-90: repeat the controls and hand over

Repeat release/rollback and incident exercises. Review access and backup evidence on the agreed cadence. Publish a two-quarter roadmap tied to enterprise needs, a capacity forecast, hiring priorities based on actual constraints, and the conditions for a permanent technology-leadership handover. The founder chooses hires; the CTO supplies role scorecards and an interview approach.

If SOC 2 is needed, define the system boundary and trust services categories with the audit firm, assess gaps, assign control owners and agree when controls are sufficiently implemented to begin the selected observation period. Do not start a nominal clock while key controls are missing. Only state a report date when the audit firm has agreed the schedule and dependencies.

Day-90 handoff: evidence index, questionnaires with verified/planned/unknown status, runbooks, accepted risk backlog, roadmap and hiring/transition plan. A blocker unresolved at day 90 remains a blocker.

## Evidence and acceptance register

| Priority candidate | Accountable owner | Acceptance | Evidence/status record |
|---|---|---|---|
| Production access | Engineering lead | Named users, MFA verified, departed user cannot access production | IAM export, tested revocation, scope/date |
| Tenant boundaries | Engineering lead | Cross-tenant access/write attempts denied in the selected critical paths | Test fixtures/results, covered endpoints |
| Release and rollback | Engineering lead | Reviewed change deployed, bad release rolled back within agreed target | PR/build/deploy IDs, exercise timings |
| Backups and recovery | Operations owner | Isolated restore meets approved RTO/RPO and data integrity checks | Backup ID, timed run, checks, exceptions |
| Partner feed reliability | Data owner | Invalid schema quarantined; stale feed alerts a named responder | Contract version, negative test, alert ticket |
| Incident response | Engineering lead | On-call person receives, acknowledges and contains a simulated failure | Exercise record, action owners |
| Predictive feature | Product owner with data lead | Held-out evaluation meets agreed thresholds; failing version blocked | Dataset provenance, split, metrics, model/data versions |
| Technical review and mentorship | CTO with engineering lead | Lead independently demonstrates a selected failure test and explains the implementation decision | PR/test IDs, pairing notes, learning/action follow-up within two weekly CTO hours |
| Customer security responses | Founder with sales | Each selected answer is verified, planned or unknown and approved for release | Evidence ID, control owner, verifier/date, expiry |

## Timed recovery exercise

1. Obtain approved RTO (time to recover) and RPO (tolerable data loss), scope, safe access and an exercise window. If targets are missing, report measured results and seek business approval instead of declaring success.
2. Select a specific backup ID and record its completion time, recovery point and integrity metadata. Capture known counts/checksums and business invariants for that same recovery point, or use a controlled snapshot with a known baseline. Record application/schema versions and required keys.
3. Restore into an isolated environment with restricted access. Disable outbound email, payment calls, production writes and scheduled jobs. Handle any real data under the customer's approved controls.
4. Start the timer at the agreed outage/recovery trigger and include environment preparation, restore, application start and verification. Compare with the recovery-point baseline, not today's changing production database.
5. Check referential integrity and selected critical business journeys. Measure RTO at usable recovery. Measure RPO from the assumed incident time to the recovered data point. Record skipped checks, manual steps, cost and failures; remove the restored environment according to policy.
6. Assign remediation, retest failures and obtain the owner's acceptance. A database restore alone does not demonstrate recovery of the whole service.

## SOC 2 mapping and boundaries

This is a preliminary mapping to the [AICPA Trust Services Criteria](https://www.aicpa-cima.com/resources/download/2017-trust-services-criteria-with-revised-points-of-focus-2022), not an auditor's assessment or an exhaustive control set. Common criteria support security; availability and confidentiality introduce additional criteria when those categories are in scope. SOC 2 is an attestation report, not a certification. Management describes the system and controls; a qualified CPA firm examines them.

| Evidence family | Indicative criteria area |
|---|---|
| Access and revocation | CC6, logical/physical access |
| Change review and deployment | CC8, change management |
| Monitoring and incident handling | CC7, system operations |
| Risk register | CC3, risk assessment |
| Vendor oversight | CC9, risk mitigation |
| Recovery/capacity evidence | A1, availability, if in scope |
| Confidential-data handling | C1, confidentiality, if in scope |

Durations and capacity are scenario assumptions. This document demonstrates an approach; it records no completed controls or actual enterprise certification.
