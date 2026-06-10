# Functional Requirements — Worked Example

> Example domain: "Online Grocery Delivery — Checkout Module"

---

## Document Control

| Field | Value |
|-------|-------|
| **Project Name** | FreshCart Online Grocery Platform |
| **Document ID** | FC-FR-002 |
| **Version** | 1.0 |
| **Date** | 2026-04-02 |
| **Author** | J. Carter, Business Analyst |
| **Status** | Approved |

---

## 1. Overview

This document covers the functional requirements for the Checkout Module, which handles cart review, discount application, payment processing, and order confirmation for the FreshCart mobile and web platforms.

---

## 2. Functional Requirements

| Req ID | Requirement Description | Priority (MoSCoW) | Source/Stakeholder | Acceptance Criteria Reference | Status |
|--------|--------------------------|--------------------|--------------------|-------------------------------|--------|
| FR-001 | The system shall display a summary of all items in the cart, including item name, quantity, unit price, and subtotal, before proceeding to payment | Must Have | Head of Customer Experience | US-03-00 | Approved |
| FR-002 | The system shall allow users to adjust item quantities or remove items directly from the checkout summary screen | Must Have | Head of Customer Experience | US-03-00 | Approved |
| FR-003 | The system shall allow users to enter a single discount code, validate it against active promotions, and apply the discount to the order subtotal | Must Have | Marketing Team | US-03-01 | Approved |
| FR-004 | The system shall calculate and display delivery fees based on the customer's delivery address and selected delivery time slot | Must Have | Operations Team | US-03-02 | Approved |
| FR-005 | The system shall support payment via credit/debit card, digital wallet (Apple Pay/Google Pay), and stored payment methods | Must Have | Finance Team | US-03-03 | Approved |
| FR-006 | The system shall display an order confirmation screen with order number, estimated delivery window, and itemized receipt upon successful payment | Must Have | Head of Customer Experience | US-03-04 | Approved |
| FR-007 | The system shall send an order confirmation email and push notification within 2 minutes of successful checkout | Should Have | Customer Support Manager | US-03-05 | Approved |
| FR-008 | The system shall allow users to add delivery instructions (e.g., "Leave at door") as free text, limited to 200 characters | Could Have | Customer feedback survey | US-03-06 | Draft |

---

## 3. Business Rules

| Rule ID | Business Rule | Applies To (Req ID) |
|---------|---------------|---------------------|
| BR-001 | A discount code cannot reduce the order subtotal below $5.00 | FR-003 |
| BR-002 | Free delivery is automatically applied for orders over $75, overriding any calculated delivery fee | FR-004 |
| BR-003 | Only one discount code may be applied per order | FR-003 |
| BR-004 | Orders cannot be placed for delivery time slots that are fewer than 2 hours from the current time | FR-004 |

---

## 4. Out of Scope

- Subscription/recurring order functionality (covered in a separate FR document: FC-FR-005)
- Loyalty points redemption at checkout (planned for Phase 2)
- Split payment across multiple payment methods

---

## Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1 | 2026-03-20 | J. Carter | Initial draft based on stakeholder workshops |
| 0.2 | 2026-03-28 | J. Carter | Added business rules after Finance review |
| 1.0 | 2026-04-02 | J. Carter | Approved by Product Owner and Operations lead |
