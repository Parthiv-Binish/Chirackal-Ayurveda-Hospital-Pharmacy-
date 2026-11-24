# 02 — Current-state assessment (AS-IS)

**Status:** Preliminary hypotheses; paper-based operation confirmed at high level.

## 1. Known operating model

The establishment includes outpatient Ayurveda care, treatment/therapy services and a pharmacy that handles both hospital-linked dispensing and retail sales. There are no inpatient admissions.

## 2. Likely current workflows to observe

These are discovery prompts, not assertions about the client's exact process.

### Patient and consultation
1. Patient arrives or contacts the establishment.
2. Reception identifies a returning patient or records a new patient.
3. Appointment/walk-in order is coordinated.
4. Practitioner conducts consultation.
5. Notes and prescription are recorded on paper.
6. Patient is directed to pharmacy and/or treatment scheduling.
7. Payment and follow-up instructions are recorded.

### Therapy
1. Practitioner determines whether a therapy is appropriate.
2. Therapy instructions and frequency/duration are documented.
3. Staff coordinate available room, equipment and therapist.
4. Session completion and observations are recorded.
5. Practitioner reviews progress and decides next steps.

The practitioner retains responsibility for clinical decisions. The system must not generate or recommend treatment protocols.

### Pharmacy
1. Sale begins from a prescription or independent retail request.
2. Staff identify product, quantity, price and (where relevant) batch.
3. Payment and receipt are handled.
4. Stock is updated in a register or other manual record.
5. Purchases, returns, damaged goods and expiry are reconciled.

## 3. Potential pain points to test

| Area | Discovery question |
|---|---|
| Patient lookup | How long does it take to find an old record? |
| Duplicate records | How are spelling/phone variations handled? |
| Consultation | Which notes are mandatory and who may read them? |
| Prescription | Are medicines handwritten, pre-printed or standardized? |
| Treatment | How are sessions, availability and completion tracked? |
| Pharmacy | Is stock recorded per item, batch and expiry? |
| Dual sales | How are prescription dispensing and walk-in retail distinguished? |
| Billing | Are hospital and pharmacy receipts separate? |
| Reconciliation | How are cash, UPI and card collections matched? |
| Follow-up | Who contacts patients and how is consent recorded? |
| Reporting | Which daily/monthly figures does management need? |
| Continuity | What happens when internet or power fails? |

## 4. Evidence collection

Request blank templates or de-identified examples of:
- Patient registration and consultation registers.
- Prescription format.
- Therapy/treatment register and schedule.
- Hospital bill/receipt.
- Pharmacy sales bill.
- Medicine stock and purchase register.
- Supplier invoice fields.
- Expense and daily collection register.
- Appointment book and follow-up list.

Do not copy identifiable patient details into this repository or development/test environments.

## 5. AS-IS deliverable

After the site visit, replace hypotheses with:
- Swimlane workflow diagrams.
- Register/form inventory.
- Role and responsibility matrix.
- Current process time and volume estimates.
- Exception and failure scenarios.
- Pain points ranked by frequency, impact and effort.
