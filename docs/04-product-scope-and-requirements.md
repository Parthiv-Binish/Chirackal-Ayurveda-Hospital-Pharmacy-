# 04 — Product scope and preliminary requirements

**Requirement status:** Draft for validation; not an approved SRS.

## 1. Product surfaces

1. Public website and contact/appointment enquiry.
2. Staff web application with role-specific modules.
3. Practitioner consultation interface.
4. Therapy scheduling and session interface.
5. Pharmacy sales and inventory interface.
6. Management reports.
7. Patient portal/app (later phase, subject to validation).

Avoid separate apps for every department. A single responsive staff application with permission-controlled modules is the preferred starting point.

## 2. Functional requirements

### Identity and access
- FR-001: The system shall authenticate individual staff accounts.
- FR-002: Authorized administrators shall manage users, groups and permissions.
- FR-003: The system shall record user, timestamp and action for sensitive changes.
- FR-004: Staff access shall be revoked promptly when employment/access ends.

### Patient and reception
- FR-010: Staff shall search for an existing patient before creating a new record.
- FR-011: The system shall generate a unique patient identifier.
- FR-012: Authorized staff shall register and update patient demographic/contact data.
- FR-013: The system shall support appointment and walk-in registration.
- FR-014: The system shall provide a configurable practitioner queue.
- FR-015: Duplicate candidates shall be flagged for authorized review, not automatically merged.

### Consultation and prescription
- FR-020: Authorized practitioners shall create and update consultation records.
- FR-021: Consultation records shall be linked to patient and practitioner.
- FR-022: Authorized practitioners shall create and approve prescriptions.
- FR-023: Prescription items shall support medicine instructions and quantity as defined by the clinical template.
- FR-024: Finalized clinical records shall not be silently overwritten; corrections shall be auditable.
- FR-025: Pharmacy staff shall access only the prescription information required for dispensing.

### Therapy
- FR-030: Authorized practitioners shall create therapy orders/plans.
- FR-031: Authorized staff shall schedule sessions against staff/resource availability.
- FR-032: Staff shall record attendance, completion, cancellation and permitted observations.
- FR-033: The system shall track remaining/planned sessions where the practitioner specifies a course.
- FR-034: Clinical plan changes shall require authorized practitioner action.

### Pharmacy and inventory
- FR-040: Pharmacy staff shall maintain a medicine/product catalogue.
- FR-041: The system shall record suppliers and purchase receipts.
- FR-042: Inventory shall be tracked by batch and expiry where applicable.
- FR-043: The system shall support prescription-linked dispensing and independent retail sales.
- FR-044: Each sale shall create traceable stock movements.
- FR-045: The system shall support returns, damaged/expired stock and authorized adjustments.
- FR-046: The system shall provide low-stock and expiry alerts.
- FR-047: The system shall support stock counts and variance reconciliation.

### Billing and reporting
- FR-050: The system shall create hospital and pharmacy bills.
- FR-051: The system shall record split/partial payments if the business requires them.
- FR-052: Refunds and discounts shall be permission-controlled and auditable.
- FR-053: Management shall view daily collection summaries by payment method and business area.
- FR-054: Authorized users shall export approved operational reports.

### Notifications and website
- FR-060: The system shall support appointment and therapy reminders subject to consent and channel availability.
- FR-061: Staff shall be able to record communication preferences and opt-outs.
- FR-062: The public website shall present verified establishment, practitioner, service, contact and location information.
- FR-063: Website appointment requests shall enter a staff-managed workflow; they shall not imply confirmed appointments until accepted.

## 3. Non-functional requirements

- NFR-001: Responsive layouts for desktop, tablet and mobile.
- NFR-002: Secure transport (HTTPS) and appropriate encryption at rest.
- NFR-003: Least-privilege access and server-side authorization.
- NFR-004: Audit trail for clinical, inventory, financial and permission changes.
- NFR-005: Automated backups with tested restoration procedures.
- NFR-006: Configurable session expiry and account recovery controls.
- NFR-007: Data export in practical, documented formats.
- NFR-008: Graceful handling of network interruption and duplicate submissions.
- NFR-009: No real patient data in development, demo or test fixtures.
- NFR-010: Monitoring, error reporting and documented support process.
- NFR-011: Date/time, currency, language and receipt formats configurable for the establishment.
- NFR-012: Accessibility and clear, low-training interfaces.

## 4. Explicit exclusions from initial scope

- Inpatient admission, beds, wards, nursing charts and discharge.
- Automated diagnosis, treatment recommendation or dose calculation.
- Manufacturing/production management for medicines unless the client confirms manufacturing activity and separate requirements.
- Online sale/delivery of medicines until licensing, prescription controls, fulfilment and legal obligations are reviewed.
- Insurance/TPA claims unless the client confirms this business need.
- ABDM integration until eligibility, consent model and integration requirements are assessed.

## 5. Acceptance approach

Each requirement must have a named owner, priority, test scenario and acceptance evidence. Clinical workflows require sign-off by the designated practitioner; pharmacy workflows by the responsible pharmacy lead; finance by management/accountant.
