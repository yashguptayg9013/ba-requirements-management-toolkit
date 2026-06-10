# RACI Matrix — Worked Example

> Example domain: "FreshCart Online Grocery Platform — Checkout Module"

---

## Document Control

| Field | Value |
|-------|-------|
| **Project Name** | FreshCart Online Grocery Platform |
| **Document ID** | FC-RACI-001 |
| **Version** | 1.0 |
| **Date** | 2026-04-02 |
| **Owner** | J. Carter, Business Analyst |

---

## RACI Definitions

| Letter | Meaning | Description |
|--------|---------|--------------|
| **R** | Responsible | Does the work to complete the task |
| **A** | Accountable | Owns the outcome; signs off; only ONE accountable person per task |
| **C** | Consulted | Provides input before/during the task (two-way communication) |
| **I** | Informed | Kept up to date on progress/outcome (one-way communication) |

---

## Roles

| Abbreviation | Role |
|--------------|------|
| CDO | Chief Digital Officer |
| PO | Product Owner (Head of Retail/Checkout Product) |
| BA | Business Analyst |
| TL | Tech Lead / Architect |
| QA | QA Lead |
| CCB | Change Control Board |

---

## RACI Matrix

| Activity / Decision | CDO | PO | BA | TL | QA | CCB |
|----------------------|-----|----|----|----|----|----|
| Define business objectives | A | R | C | I | I | I |
| Requirements elicitation (workshops, interviews) | I | C | R | C | I | I |
| Functional Requirements Document sign-off | I | A | R | C | C | I |
| Non-Functional Requirements definition | I | C | R | A | C | I |
| Technical design & architecture | I | I | C | A | C | I |
| User story writing & backlog grooming | I | A | R | C | C | I |
| Sprint planning | I | A | C | R | C | I |
| UAT planning | I | A | R | C | R | I |
| UAT execution | I | C | C | C | A | I |
| Change request submission | I | C | R | C | C | I |
| Change request impact assessment | I | C | R | C | C | I |
| Change request approval | I | C | I | I | I | A |
| Go/No-Go decision for launch | A | R | C | C | C | I |
| Production deployment | I | I | I | A | C | I |
| Post-launch performance review | C | A | R | C | C | I |

---

## Validation Checklist

- [x] Every activity has exactly one "A"
- [x] Every activity has at least one "R"
- [x] No single role has an excessive number of "A"s — PO has the most (6), which is appropriate as Product Owner
- [x] "C" used selectively — e.g., QA consulted on NFRs and design, not on business objectives
- [x] "I" used for awareness — e.g., CDO informed of UAT execution but not directly involved
- [x] Reviewed and agreed by CDO, PO, TL, QA Lead, and CCB chair on 2026-04-02

---

## Notes

- The **Change Control Board (CCB)** consists of the CDO, PO, and TL collectively — but for "approval" decisions, the CCB acts as a single accountable body, hence "A" is attributed to "CCB" as a group rather than an individual
- This matrix should be revisited at the start of each major phase (e.g., moving from Discovery to Build, or Build to UAT) as roles and responsibilities may shift

---

## Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1 | 2026-03-25 | J. Carter | Initial draft |
| 1.0 | 2026-04-02 | J. Carter | Reviewed and approved by all listed roles |
