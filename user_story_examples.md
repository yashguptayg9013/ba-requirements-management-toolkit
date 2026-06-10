# User Story Examples

> Two worked examples showing the User Story Template filled out for a fictional "Online Grocery Delivery" feature.

---

## Example 1

## Story Identification

| Field | Value |
|-------|-------|
| **Story ID** | US-03-01 |
| **Epic** | EP-03: Checkout & Payments |
| **Title** | Apply a discount code at checkout |
| **Priority** | Must Have |
| **Story Points** | 5 |
| **Status** | Ready |

---

## Story Statement

**As a** returning customer,
**I want to** enter a discount code during checkout,
**so that** I can receive a price reduction on my order before payment.

---

## Description / Context

The marketing team frequently runs promotional campaigns with unique discount codes. Customers receive these codes via email or social media. Currently there is no field for entering a code, so customers cannot redeem promotions, leading to support complaints and abandoned carts.

---

## Acceptance Criteria (Given/When/Then)

```
Scenario 1: Valid discount code applied
Given I am on the checkout page with items in my cart
When I enter a valid, active discount code and click "Apply"
Then the discount amount is deducted from my order total
And the applied code is displayed with an option to remove it

Scenario 2: Invalid discount code
Given I am on the checkout page
When I enter a discount code that does not exist or has expired
Then I see an error message: "This code is invalid or has expired"
And my order total remains unchanged

Scenario 3 (Edge case): Code already used by this customer
Given I have previously used a single-use discount code
When I attempt to apply the same code again
Then I see a message: "This code has already been used on your account"
And the discount is not applied
```

---

## Definition of Done (DoD)

- [x] Code developed and peer-reviewed
- [x] Unit tests written and passing
- [x] Acceptance criteria validated by QA
- [x] Accessibility checked (if UI-facing)
- [ ] Documentation updated
- [ ] Product Owner sign-off

---

## Dependencies

| Dependency Type | Description |
|-----------------|-------------|
| Blocked by | None |
| Blocks | US-03-02 (Order summary display with discounts) |
| Related to | US-02-05 (Promotions management for marketing team) |

---

## Notes / Open Questions

- Should discount codes stack with loyalty points? (Confirmed with PO: No, only one discount type per order for MVP)
- Need to confirm max code length with backend team (assumed 20 characters)

---

## Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1 | 2026-03-12 | J. Carter | Initial draft |
| 0.2 | 2026-03-14 | J. Carter | Added edge case for reused codes after PO feedback |

---
---

## Example 2

## Story Identification

| Field | Value |
|-------|-------|
| **Story ID** | US-05-02 |
| **Epic** | EP-05: Order Tracking |
| **Title** | Receive real-time delivery status updates |
| **Priority** | Should Have |
| **Story Points** | 8 |
| **Status** | Backlog |

---

## Story Statement

**As a** customer who has placed an order,
**I want to** receive real-time updates on my delivery status,
**so that** I know when to expect my groceries and can plan accordingly.

---

## Description / Context

Customer surveys show that "not knowing when delivery will arrive" is the #1 complaint. This story introduces push notifications tied to delivery driver status updates from the existing logistics partner API.

---

## Acceptance Criteria (Given/When/Then)

```
Scenario 1: Order status changes to "Out for Delivery"
Given my order has been packed and assigned to a driver
When the driver marks the order as "Out for Delivery" in the logistics app
Then I receive a push notification: "Your order is on its way! Estimated arrival: [time]"

Scenario 2: Delivery delay
Given my order is "Out for Delivery"
When the estimated arrival time changes by more than 15 minutes
Then I receive an updated notification with the new estimated time

Scenario 3 (Edge case): Push notifications disabled
Given I have disabled push notifications on my device
When my order status changes
Then the status update is still visible in the "My Orders" section of the app
And no push notification is sent
```

---

## Definition of Done (DoD)

- [ ] Code developed and peer-reviewed
- [ ] Unit tests written and passing
- [ ] Acceptance criteria validated by QA
- [ ] Accessibility checked (if UI-facing)
- [ ] Documentation updated
- [ ] Product Owner sign-off

---

## Dependencies

| Dependency Type | Description |
|-----------------|-------------|
| Blocked by | Logistics partner API webhook integration (Tech spike required) |
| Blocks | None |
| Related to | US-05-01 (Order status page) |

---

## Notes / Open Questions

- Confirm with logistics partner whether webhook supports sub-15-minute granularity
- Consider SMS fallback for customers without the app installed (raised as a future enhancement)

---

## Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1 | 2026-03-18 | J. Carter | Initial draft, pending tech spike |
