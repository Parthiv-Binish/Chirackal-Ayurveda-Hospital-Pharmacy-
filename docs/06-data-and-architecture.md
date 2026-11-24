# 06 — Preliminary data model and architecture

**Status:** Conceptual only. Final schema follows validated workflows and sample blank forms.

## 1. Architecture direction

Prefer a modular monolith initially: one backend, one relational database and clearly separated domain modules. This reduces operational complexity for a single establishment while preserving boundaries for future expansion.

Proposed stack for evaluation:
- Frontend: React + Vite, responsive staff and public interfaces.
- Backend: Python + FastAPI.
- Database: PostgreSQL.
- Authentication: secure server-managed sessions or a vetted identity solution.
- Private document storage: object storage with access controls.
- Background processing: queue/worker only where asynchronous tasks justify it.
- Hosting: managed or VPS-based production environment with monitoring and tested backups.

Technology choices remain subject to budget, support capacity, connectivity and deployment review.

## 2. Domain modules

- Organization and configuration.
- Identity, groups and permissions.
- Patient registry.
- Appointments and queue.
- Consultation and clinical records.
- Prescriptions.
- Therapy plans and sessions.
- Product/medicine catalogue.
- Suppliers and purchasing.
- Batch inventory and stock ledger.
- Pharmacy sales and dispensing.
- Hospital billing and payments.
- Pharmacy billing and payments.
- Notifications and consent/preferences.
- Audit, reporting and system operations.

## 3. Conceptual entities

| Domain | Candidate entities |
|---|---|
| Organization | Organization, Location, Department, BusinessConfiguration |
| Identity | User, Group, Permission, UserGroup, GroupPermission, AuditEvent |
| Patient | Patient, PatientContact, PatientIdentifier, ConsentRecord |
| OPD | Appointment, QueueEntry, Encounter, Practitioner |
| Clinical | ClinicalNote, Prescription, PrescriptionItem, Attachment |
| Therapy | TherapyOrder, TherapySession, Resource, StaffAssignment |
| Pharmacy | Product, ProductCategory, Supplier, Purchase, PurchaseLine |
| Inventory | StockBatch, StockMovement, StockCount, StockAdjustment |
| Sales | PharmacySale, PharmacySaleLine, DispensingRecord, Return |
| Finance | Bill, BillLine, Payment, Refund, Expense, CashClose |
| Messaging | Notification, Template, DeliveryAttempt, CommunicationPreference |

## 4. Key relationships and invariants

- One patient may have many appointments and encounters.
- One encounter belongs to one patient and one responsible practitioner.
- An encounter may create zero or more prescriptions and therapy orders.
- One prescription contains one or more prescription items.
- Prescription-linked dispensing must reference the relevant prescription/item where applicable.
- Retail sales must be possible without an encounter.
- One product may have multiple stock batches.
- Stock is changed through immutable or append-only stock movement records, not by silently overwriting a quantity.
- A sale may use multiple batches and a payment may be split across methods.
- Hospital and pharmacy bills should be separately identifiable even if management reporting consolidates them.
- Sensitive clinical data must be protected at API and database-access layers, not only hidden in the UI.

## 5. Data quality

- Use stable internal identifiers; do not use phone number as patient primary key.
- Store timestamps consistently and display in the establishment's local timezone.
- Preserve source references during migration.
- Flag duplicate candidates for human review.
- Define product units, pack sizes, conversion rules and price history.
- Validate batch and expiry data where applicable.
- Keep correction history for finalized clinical and financial records.

## 6. Deployment and continuity

Production must include TLS, secrets management, least-privilege database access, automated backups, restore tests, monitoring, patching and documented incident response. Define recovery point and recovery time objectives with the client. Provide a paper downtime process and reconciliation log; do not claim full offline capability unless it is designed and tested.

## 7. Future multi-branch support

Use an organization/location boundary in the data model, but do not build complex multi-tenant infrastructure unless the client confirms expansion plans. Enforce location scoping server-side.
