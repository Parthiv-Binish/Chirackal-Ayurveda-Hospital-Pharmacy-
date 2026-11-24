# 03 — Proposed operating model (TO-BE)

## 1. Design principles

- One patient identity shared across hospital encounters and prescription-linked pharmacy activity.
- Independent retail pharmacy sales remain possible without creating a clinical encounter.
- Consultation, treatment and pharmacy workflows remain distinct but connected.
- Clinical content is authored and approved by an authorized practitioner.
- Every stock movement and financial transaction is traceable.
- Staff see only the information required for their duties.
- Common tasks should work quickly on a shared desktop/tablet.
- Provide a documented manual downtime procedure and safe later reconciliation.

## 2. Patient journey

1. Search by patient number, phone or approved identity fields.
2. Match an existing patient or create a new record.
3. Register appointment or walk-in visit.
4. Add patient to the practitioner queue.
5. Practitioner records consultation, assessment and plan.
6. Practitioner issues and signs/approves prescription where applicable.
7. Patient may proceed to pharmacy, therapy scheduling, both or neither.
8. Record charges and payment in the correct billing context.
9. Schedule follow-up and send communications only under recorded preferences/consent.

## 3. Consultation and prescription

A consultation should capture encounter date/time, practitioner, relevant history, observations, assessment/diagnosis as entered by the practitioner, advice, plan and follow-up. The exact template must be approved by the clinical lead.

Prescription items should capture product/medicine, practitioner instructions, dose/route/frequency/duration where applicable, quantity and directions. Do not hardcode clinical rules or infer doses. Corrections should be auditable; preserve the original signed/approved version according to the approved record policy.

## 4. Therapy workflow

- Practitioner creates a therapy order or plan.
- Authorized staff schedule sessions based on practitioner instructions and resource availability.
- Each session records scheduled time, assigned staff, attendance, completion status and permitted observations.
- Missed, cancelled and rescheduled sessions have reasons and audit history.
- Changes to clinical instructions require practitioner authorization.
- Progress review and plan closure are recorded by authorized clinical personnel.

No inpatient admission, bed/ward management or discharge module is included in the initial scope. Day-care workflow remains an open question.

## 5. Pharmacy workflow

### Prescription-linked dispensing
- Retrieve an authorized prescription or verify the presented prescription.
- Check product, prescribed quantity and dispensing status.
- Select eligible stock batch using configured business rules.
- Record quantity dispensed, substitution/short supply where legally and clinically permitted, staff member and timestamp.
- Generate pharmacy bill/receipt and update stock.

### Independent retail sale
- Create a retail sale without requiring a hospital consultation.
- Search catalogue/barcode if available.
- Select product, quantity, price and batch.
- Record customer details only when needed and lawfully collected.
- Bill, collect payment and decrement stock.

### Inventory
- Record purchase receipt, supplier, invoice, product, batch, expiry, quantity and cost.
- Track stock ledger movements: purchase, sale, return, transfer, adjustment, damage and expiry.
- Require reason and authorization for adjustments.
- Provide low-stock and near-expiry alerts.
- Support physical stock count and reconciliation.

## 6. Billing and finance

Keep hospital service billing and pharmacy billing configurable as separate bill types, even if management later wants consolidated reporting. Record line items, discounts with authorization, taxes where applicable, payment method, refunds and receipt references. Avoid treating a bill as paid until the payment record is confirmed.

Daily close should summarize opening cash (if used), collections by payment method, refunds, expenses, cash counted and variance. Confirm accounting and GST requirements with the client's accountant.

## 7. Exceptions and downtime

Define procedures for duplicate patients, wrong patient selection, prescription correction, partial dispensing, out-of-stock medicines, returns, cancelled appointments, missed therapy sessions, payment reversal, printer failure and network outage. Paper downtime records should have a controlled reference and be reconciled by authorized staff when service returns.
