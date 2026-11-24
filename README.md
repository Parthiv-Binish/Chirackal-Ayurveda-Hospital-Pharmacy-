# Chirackal Ayurveda Hospital & Pharmacy

**Business and digital transformation study**  
**Location:** Muttom, Thodupuzha, Idukki, Kerala, India  
**Project type:** Client engagement — discovery and planning  
**Status:** Preliminary study; operational validation pending

## Purpose

This repository is the documentation source of truth for studying and planning a complete digital transformation of Chirackal Ayurveda Hospital & Pharmacy. The engagement covers the hospital, its pharmacy, public digital presence, internal operations and patient-facing services.

The project must be driven by verified business workflows. It is not a commitment to build every proposed application or feature before requirements, compliance, budget and operational constraints are validated.

## Confirmed discovery baseline

| Topic | Current understanding | Status |
|---|---|---|
| Client | Chirackal Ayurveda Hospital & Pharmacy | Confirmed in project discovery |
| Relationship | Client project | Confirmed |
| Establishment scope | Hospital + pharmacy | Confirmed |
| Current operations | Paper-based | Confirmed at high level |
| Desired outcome | Complete digital transformation | Confirmed |
| Inpatient facility | No inpatient facility | Confirmed |
| Clinical service model | Consultations + Ayurveda treatments/therapies | Confirmed at high level |
| Pharmacy operating model | Hospital-linked dispensing + independent retail sales | Confirmed at high level |
| Day-care/observation arrangements | Unknown | Site validation required |
| Whether hospital and retail pharmacy share entity, licence, counter and stock | Unknown | Site validation required |
| Staff, patient volumes, branches, infrastructure | Unknown | Site validation required |

## Study principles

1. Validate the real establishment and its processes before designing software.
2. Separate confirmed facts, public-source leads, assumptions and recommendations.
3. Minimize collection of patient-identifiable information during discovery.
4. Design role-based access, auditability, backups and privacy into the system.
5. Prioritize reliable core workflows over unnecessary application count.
6. Plan for connectivity interruptions and practical staff adoption.
7. Treat clinical decisions and treatment protocols as practitioner-owned; software supports documentation and workflow, not diagnosis.
8. Do not assume inpatient, bed, ward or discharge workflows: the client has confirmed there is no inpatient facility.

## Proposed documentation

- [Business discovery and feasibility](docs/01-business-discovery.md)
- [Current-state and problem assessment](docs/02-current-state-assessment.md)
- [Proposed operating model and workflows](docs/03-proposed-operating-model.md)
- [Product scope and requirements](docs/04-product-scope-and-requirements.md)
- [Roles, permissions and security](docs/05-roles-security-and-privacy.md)
- [Data model and architecture](docs/06-data-and-architecture.md)
- [Website and patient experience](docs/07-website-and-patient-experience.md)
- [Compliance and risk register](docs/08-compliance-and-risk-register.md)
- [Delivery roadmap](docs/09-delivery-roadmap.md)
- [Site discovery checklist](docs/10-site-discovery-checklist.md)

## Important status note

This is a preliminary study based on project discovery answers and limited public research leads. It is **not** a verified operational audit, legal opinion, clinical assessment, final SRS, or approved implementation specification. Public directory listings and service descriptions must be checked directly with the client before they are treated as facts.

## Next milestone

Conduct a structured site visit with management, doctor/practitioner, reception, therapy staff and pharmacy representatives. Validate the checklist in [10 — Site discovery checklist](docs/10-site-discovery-checklist.md), collect blank/sample operational forms with no patient identifiers, and update the study before freezing requirements.

## Repository structure

```text
.
├── README.md
└── docs/
    ├── 01-business-discovery.md
    ├── 02-current-state-assessment.md
    ├── 03-proposed-operating-model.md
    ├── 04-product-scope-and-requirements.md
    ├── 05-roles-security-and-privacy.md
    ├── 06-data-and-architecture.md
    ├── 07-website-and-patient-experience.md
    ├── 08-compliance-and-risk-register.md
    ├── 09-delivery-roadmap.md
    └── 10-site-discovery-checklist.md
```
