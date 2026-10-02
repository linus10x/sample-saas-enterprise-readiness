# SAMPLE 90-day fractional CTO plan: taking an internal analytics tool to an enterprise-ready SaaS spinout

> **Sample / illustrative. The company described is fictional ("SpinCo"). Nothing here is based on a real client, engagement or confidential material.** Prepared by Kunjar Bhaduri, Bhaduri Advisory, October 2, 2026, with AI drafting assistance under my direction. Assumes about 10 to 15 hours a week of fractional time alongside a small in-house team.

## Starting point (assumed)
An analytics platform built inside a services firm for its own use: automated reporting, partner data feeds, an early predictive feature. Two or three engineers. Enterprise prospects are asking security questions the team can't yet answer with evidence.

## The goal by day 90
1. Every enterprise security question answered with evidence, not promises.
2. Releases, backups and incidents handled by process, not heroics.
3. A roadmap and hiring plan the founders can take to their board.
4. If prospects need it: SpinCo on a dated track to SOC 2 Type II, with the gap assessment done. **No claim of SOC 2 compliance or certification until an auditor's report exists.**

## Days 1 to 15: see it as it is
- Codebase and architecture review; list single points of failure, with one owner per item.
- Access review: who can reach production, how, with what MFA. Remove shared accounts.
- **Backups: run a real restore into a clean environment and time it.** Many teams find out here that recovery has never been tested.
- Data pipeline review: every partner feed listed with its owner, schedule, failure behaviour and a data contract.
- Read the last 5 security questionnaires from prospects; build the answer bank from what is true today.
- Deliverable: a one-page risk register ranked by "blocks an enterprise deal" first.

## Days 16 to 45: fix what blocks deals
- CI/CD: every change through pull request, tests, review and an automated deploy with rollback.
- Observability: alerts on the jobs customers depend on (feed ingestion, report generation, model scoring), not just CPU.
- Incident response: severity levels, on-call, a written post-incident review template.
- Access controls and auditability: SSO for staff, role-based access in the product, an audit log of admin actions.
- Data protection: encryption at rest and in transit confirmed; retention and deletion rules written down.
- AI feature: an evaluation set with pass thresholds before any model or prompt change ships; record model and prompt versions with each prediction.
- Join prospect calls with BI and data stakeholders to answer technical questions directly.

## Days 46 to 90: make it durable
- SOC 2 track (if needed): pick the trust services criteria in scope, choose an audit firm, start the observation window. Map existing controls (below).
- Roadmap: the next two quarters, tied to the enterprise deals in the pipeline.
- Team plan: which roles to hire first (usually a senior platform engineer before more feature engineers), interview loop, and when to convert fractional leadership into a permanent hire.
- Hand-off pack: architecture decision records, runbooks, the risk register with owners.

## Control map: what the work above produces, mapped to SOC 2 common criteria (track-to, not a claim)
| Work item | Evidence it produces | Related SOC 2 area |
|---|---|---|
| Access review, SSO, MFA, no shared accounts | Access list, quarterly review record | CC6 logical access |
| CI/CD with review and approvals | PR history, deploy log | CC8 change management |
| Alerting, on-call, incident reviews | Alert config, incident tickets, post-incident reviews | CC7 system operations |
| Tested restore, quarterly drill | Timed restore record | A1 availability |
| Risk register with owners | Register and review dates | CC3 risk assessment |
| Vendor list with data-use terms (incl. model vendors) | Vendor register | CC9 risk mitigation (vendors) |
| Encryption, retention, deletion rules | Configuration screenshots, policy | C1 confidentiality |

## Restore drill (the one-hour test I'd run in week 1)
1. Pick yesterday's backup of the production database.
2. Restore it into an isolated environment. Start a timer.
3. Run three known queries and compare results with production.
4. Record: time to restore, data loss window, anything that had to be done by hand.
5. If the restore fails or takes longer than the business can tolerate, that becomes item 1 on the risk register.

## Limits
Fictional company; durations are planning assumptions. SOC 2 timelines depend on the auditor and the observation window chosen.
