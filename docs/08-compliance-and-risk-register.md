# 08 — Compliance and risk register

**Important:** This is a project checklist, not legal advice. Requirements must be checked against current law, licences and the establishment's actual activities.

## 1. Areas requiring verification

### Clinical establishment
- Confirm registration status and establishment category under applicable Kerala clinical-establishment rules.
- Confirm applicable minimum standards for the Ayurveda facility.
- Verify practitioner qualifications and professional registration.
- Confirm displayed registration details and required records.

### Pharmacy
- Identify the exact products sold and activities performed.
- Verify applicable retail/dispensing permissions, responsible personnel and premises requirements.
- Confirm whether the pharmacy is a separate licensed entity or part of the hospital.
- Confirm rules for prescription-only products, records, storage, returns and online orders.
- If any medicine is manufactured, repackaged or relabelled, obtain a separate specialist licensing/GMP assessment. Do not assume ordinary retail permissions cover manufacturing.

### Tax and finance
- Confirm GST applicability, invoice fields, HSN/tax treatment and accounting requirements with the client's accountant.
- Confirm whether hospital and pharmacy books/cash counters are separate.
- Define receipt numbering, refunds, discounts and record retention.

### Data protection and cybersecurity
- Assess applicable Indian data protection law/rules and commencement/transition provisions at implementation.
- Define privacy notice, consent/other lawful basis, data-subject request handling, retention and breach response.
- Review health-data confidentiality, access logging and vendor contracts.
- Confirm backup location, access, encryption and deletion process.

### Digital health interoperability
- Evaluate ABDM/ABHA only if the client wants it and the establishment meets current onboarding and technical requirements.
- Do not make ABHA mandatory for ordinary system use without a valid basis and approved workflow.

## 2. Risk register

| Risk | Impact | Mitigation |
|---|---|---|
| Incorrect assumptions about services | High | Site validation and practitioner sign-off |
| Wrong patient record selected | High | Patient search, confirmation and audit |
| Unauthorized clinical access | High | Least privilege, server-side checks, access reviews |
| Prescription transcription error | High | Practitioner approval and clear source-of-truth |
| Batch/expiry mismatch | High | Receiving checks and stock counts |
| Untraceable stock edits | High | Stock ledger and authorized adjustments |
| Payment/reconciliation errors | Medium/High | Immutable transaction history and daily close |
| Network/power outage | Medium/High | Downtime paper process and reconciliation |
| Poor staff adoption | High | Co-design, training and staged rollout |
| Data migration errors | High | Mapping, sampling, reconciliation and sign-off |
| Unapproved medical claims | High | Practitioner review and content approval |
| Scope/cost growth | Medium/High | Prioritized backlog and change control |

## 3. Go-live gates

Do not go live until:
- Client approves workflows and role matrix.
- Clinical lead approves consultation, prescription and therapy templates.
- Pharmacy lead approves catalogue, batch, dispensing and return process.
- Management/accountant approves billing and daily reconciliation.
- Access controls and audit events pass testing.
- Backup restoration is demonstrated.
- Staff training and downtime procedures are complete.
- Data migration is reconciled and formally accepted.
- Applicable legal/licensing questions are resolved by qualified advisers.
