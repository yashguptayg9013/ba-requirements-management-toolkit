# Change Request Log — Worked Example

> Example domain: "FreshCart Online Grocery Platform — Checkout Module"

---

## Document Control

| Field | Value |
|-------|-------|
| **Project Name** | FreshCart Online Grocery Platform |
| **Document ID** | FC-CRL-001 |
| **Version** | 1.3 |
| **Last Updated** | 2026-05-15 |
| **Owner** | J. Carter, Business Analyst |

---

## Change Request Log

| CR ID | Date Raised | Raised By | Description | Reason / Justification | Impact (Scope/Schedule/Cost) | Priority | Status | Decision Date | Approved By | Linked Req ID(s) |
|-------|-------------|-----------|--------------|------------------------|-------------------------------|----------|--------|----------------|-------------|------------------|
| CR-001 | 2026-04-10 | Marketing Team | Add support for percentage-based AND fixed-amount discount codes (originally only fixed-amount was scoped) | Upcoming campaign requires "20% off" promotions, which the current design doesn't support | Scope: Update FR-003 and discount calculation logic. Schedule: +3 days. Cost: Negligible (within sprint capacity) | High | Approved | 2026-04-12 | Patricia Lam (Product Owner) | FR-003, US-03-01 |
| CR-002 | 2026-04-18 | Customer Support Manager | Add a "Save delivery instructions for future orders" checkbox | Support tickets show 30% of customers re-enter the same delivery instructions every order | Scope: New field + persistence logic. Schedule: +2 days (Sprint 9). Cost: Minimal | Medium | Approved | 2026-04-20 | Patricia Lam (Product Owner) | FR-008, US-03-06 |
| CR-003 | 2026-04-25 | Finance Team | Add support for "Buy Now, Pay Later" (Klarna) as a payment method | Competitor analysis shows BNPL increases average order value by 18% | Scope: New payment integration — significant. Schedule: +4 weeks. Cost: +$22,000 (vendor integration fees + dev time) | High | Deferred | 2026-04-29 | David Reyes (CDO) | FR-005 |
| CR-004 | 2026-05-02 | QA Lead | Reduce checkout page load NFR target from 2 seconds to 1.5 seconds based on competitor benchmarking | Competitor benchmarking shows market leaders achieve 1.2–1.5 sec load times | Scope: NFR-001 update; may require image optimization work. Schedule: +1 week. Cost: Minimal | Medium | Under Review | — | — | NFR-001 |
| CR-005 | 2026-05-10 | UX Design Lead | Remove the "Leave at door" free-text field and replace with predefined dropdown options | Free text led to inconsistent driver instructions; drivers requested standardized options | Scope: Update FR-008 and US-03-06. Schedule: No change (within current sprint). Cost: None | Low | Approved | 2026-05-12 | Patricia Lam (Product Owner) | FR-008, US-03-06 |

---

## Impact Assessment Detail — CR-003 (Example of High Priority Assessment)

| Field | Detail |
|-------|--------|
| **CR ID** | CR-003 |
| **Current State** | Checkout supports credit/debit card and digital wallets only (FR-005) |
| **Proposed Change** | Integrate Klarna BNPL as an additional payment option at checkout |
| **Affected Requirements** | FR-005 (Payment methods) |
| **Affected User Stories** | US-03-03 (Payment selection) |
| **Schedule Impact** | +4 weeks — requires new vendor integration, sandbox testing, and compliance review for BNPL regulations |
| **Cost Impact** | +$22,000 (Klarna integration fees, developer time, compliance review) |
| **Risk if Not Approved** | Potential 18% lift in AOV not realized; competitive gap remains |
| **Risk if Approved** | Delays MVP launch by 4 weeks; introduces new third-party dependency and BNPL regulatory considerations (Reg Z disclosures) |
| **Recommendation** | Defer to Phase 2 — launch MVP on schedule with existing payment methods, prioritize BNPL as the first post-launch enhancement |

---

## Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | 2026-04-10 | J. Carter | Log created with CR-001 |
| 1.1 | 2026-04-20 | J. Carter | Added CR-002, CR-003 |
| 1.2 | 2026-05-02 | J. Carter | Added CR-004 |
| 1.3 | 2026-05-15 | J. Carter | Added CR-005; updated CR-003 status to Deferred with full impact assessment |
