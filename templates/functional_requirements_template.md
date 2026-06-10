# Functional Requirements Template

> Use this template during requirements elicitation to document **what the system must do** — features, behaviors, business rules, and interactions. Each requirement should be atomic (one requirement = one testable statement), unambiguous, and traceable.

---

## Document Control

| Field | Value |
|-------|-------|
| **Project Name** | [Project name] |
| **Document ID** | [e.g., PROJ-FR-001] |
| **Version** | [Version number] |
| **Date** | [Date] |
| **Author** | [BA name] |
| **Status** | [Draft / In Review / Approved] |

---

## 1. Overview

[Brief description of the feature area or module these requirements cover]

---

## 2. Functional Requirements

| Req ID | Requirement Description | Priority (MoSCoW) | Source/Stakeholder | Acceptance Criteria Reference | Status |
|--------|--------------------------|--------------------|--------------------|-------------------------------|--------|
| FR-001 | [The system shall...] | [Must/Should/Could/Won't] | [Who requested this] | [Link to user story / AC] | [Draft/Approved] |
| FR-002 | [The system shall...] | | | | |
| FR-003 | [The system shall...] | | | | |

---

## 3. Business Rules

| Rule ID | Business Rule | Applies To (Req ID) |
|---------|---------------|---------------------|
| BR-001 | [Description of the business rule, e.g., "A discount cannot exceed 50% of order value"] | [FR-XXX] |
| BR-002 | | |

---

## 4. Requirement Writing Guidelines

When writing each requirement, ensure it is:

- **Atomic** — describes a single capability, not multiple
- **Unambiguous** — avoid vague terms like "user-friendly," "fast," "easy"
- **Verifiable** — can be tested with a pass/fail outcome
- **Traceable** — linked to a business need, stakeholder, and test case
- **Written in active voice** — "The system shall validate the email format" not "Email format should be validated"

### ❌ Poor Example
> "The system should handle errors well."

### ✅ Good Example
> "FR-014: The system shall display a specific error message when a user submits a form with a missing required field, identifying which field is missing."

---

## 5. Out of Scope

[List items explicitly excluded from this set of requirements to prevent scope ambiguity]

- [Item 1]
- [Item 2]

---

## Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1 | [Date] | [Name] | Initial draft |
