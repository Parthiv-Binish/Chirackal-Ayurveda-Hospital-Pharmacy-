# 05 — Roles, security and privacy

## 1. Proposed groups

Use group-based access control with permissions assigned to groups. A user may belong to more than one group only when approved and justified.

| Group | Intended access |
|---|---|
| Owner / management | Business-wide dashboards, configuration and approvals |
| System administrator | User, security and technical configuration; no default clinical access |
| Reception | Patient registration, appointments, queue and permitted billing |
| Practitioner | Assigned patient encounters, clinical notes, prescriptions and therapy orders |
| Therapist / treatment staff | Assigned therapy schedule and minimum necessary patient/treatment instructions |
| Pharmacist | Product catalogue, stock, purchases, prescription dispensing and pharmacy sales |
| Accounts | Bills, payments, refunds and financial reports; no unrestricted clinical notes |
| Auditor (read-only) | Approved audit and reports within assigned scope |

The actual staff roles and legal responsibilities must be confirmed with the client. Avoid shared logins.

## 2. Sensitive-data safeguards

- Collect only data necessary for care and business operations.
- Document purpose, notice and applicable consent/legal basis for each processing activity.
- Restrict medical history and consultation notes to authorized clinical users.
- Restrict pharmacy access to the information needed to dispense.
- Do not expose clinical details in ordinary WhatsApp/SMS reminders.
- Use private file storage and time-limited access links for documents.
- Keep audit logs protected from ordinary staff modification.
- Define retention, correction, export and deletion procedures with legal advice.
- Use encryption in transit and at rest, managed secrets and secure backups.
- Review access periodically and immediately disable obsolete accounts.

## 3. Audit events

At minimum log:
- Login failures and account/security changes.
- Patient record creation and sensitive updates.
- Consultation and prescription creation/finalization/correction.
- Therapy order and session changes.
- Stock receipts, sales, returns and adjustments.
- Bill, discount, refund and payment changes.
- Permission changes, exports and access to particularly sensitive records.

Logs should identify actor, timestamp, record reference, action and reason where appropriate. Avoid putting full medical notes or secrets into logs.

## 4. Privacy and compliance review

Assess applicable Indian data protection law and rules in force at implementation time, health-record obligations, consumer protection, IT security requirements and any sector-specific rules. Obtain qualified legal/compliance advice; this document is not legal advice.

ABDM/ABHA support must be optional and implemented only after checking current programme requirements, consent flows, facility/professional onboarding and interoperability specifications.

## 5. Operational security

- Enforce strong authentication; consider MFA for privileged users.
- Use secure password hashing and rate limiting.
- Apply server-side authorization on every API operation.
- Protect against CSRF/XSS/SQL injection and insecure direct object references.
- Separate production, staging and development environments.
- Never commit API keys, credentials, patient exports or database dumps.
- Test backup restoration and incident response.
- Maintain a breach/incident escalation and notification procedure.
