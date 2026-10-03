# SAMPLE: evidence-backed questionnaire starter

> **Illustrative sample by Kunjar Bhaduri, Bhaduri Advisory. Fictional organization and invented evidence only. No client relationship or confidential engagement material. Prepared with AI drafting assistance under my direction. Revised October 3, 2026 (America/Chicago).**

Use the patterns below only after verifying the actual control. No row asserts that a control exists. Record scope, owner, evidence ID, verifier/date, release clearance and next review. Distinguish implemented and tested, implemented but untested, planned, and unknown. Planned dates require an accountable owner's agreement; auditor dates require the audit firm's agreement. Unresolved placeholders must never be sent to a prospect.

| Question | Verified answer pattern | If verification is missing | Evidence to check |
|---|---|---|---|
| SOC 2 Type II? | Identify the CPA firm, system scope and report period only if a report exists and sharing is permitted. | Say that no report is available. Describe only an approved readiness plan; state a projected date only when the audit firm has agreed it. | Report, scope, sharing terms, approved plan |
| Production access? | Describe actual SSO/MFA coverage, named users, exceptions and review cadence. | Identify the current method and gap; do not claim all staff are covered. | IAM export, MFA settings, access review and revocation test |
| Backup and recovery? | State protected systems, frequency, retention and latest tested recovery results against approved targets. | Distinguish configured backups from an untested restore. | Backup IDs/settings, timed exercise, RTO/RPO and integrity results |
| Release control? | Describe the demonstrated review, test, deployment and rollback workflow, including exceptions. | State the current process and owned implementation plan. | PR/build/deploy IDs, permissions and rollback exercise |
| Incident response? | Describe covered alerts, response ownership and exercised escalation. | List what is monitored and what remains untested. | Alert test, rota, exercise/incident record |
| AI training or retention? | State verified vendor contract terms and configured settings for each data flow. | Mark unknown and obtain a vendor/counsel answer before assurance. | Contract/version, configuration, subprocessor/data-flow register |
| Storage and deletion? | Identify actual regions, subprocessors, retention and tested deletion scope, including backups. | State the known scope and open gaps. | Data map, retention settings, deletion test and contractual terms |
| Tenant isolation? | Identify tested boundaries and covered endpoints. | State uncovered paths and planned tests without an isolation guarantee. | Negative-test results, authorization design and endpoint scope |

Example, entirely fictional: Q-03, backup question, status "implemented but restore untested," owner operations lead, evidence E-03 backup configuration, verifier/date not yet recorded, release answer "Daily backup jobs are configured; recovery time has not yet been demonstrated." An agreed future restore date may be added after the owner confirms it. This is a truthful answer even when a buyer would prefer a stronger control.
