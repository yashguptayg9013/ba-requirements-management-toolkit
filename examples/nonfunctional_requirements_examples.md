# Non-Functional Requirements — Worked Example

> Example domain: "Online Grocery Delivery — Checkout Module"

---

## Document Control

| Field | Value |
|-------|-------|
| **Project Name** | FreshCart Online Grocery Platform |
| **Document ID** | FC-NFR-002 |
| **Version** | 1.0 |
| **Date** | 2026-04-02 |
| **Author** | J. Carter, Business Analyst |
| **Status** | Approved |

---

## NFR Categories Checklist

- [x] Performance (response time, throughput)
- [x] Scalability (load, concurrent users, growth)
- [x] Availability & Reliability (uptime, failover)
- [x] Security (authentication, encryption, access control)
- [x] Usability & Accessibility (WCAG, ease of use)
- [ ] Maintainability (code quality, documentation)
- [x] Compatibility (browsers, devices, OS versions)
- [x] Compliance & Legal (industry regulations, data residency)
- [x] Data Retention & Privacy
- [ ] Disaster Recovery / Backup (covered in separate Infrastructure NFR doc)

---

## Non-Functional Requirements

| Req ID | Category | Requirement Description | Target / Threshold | Measurement Method | Priority |
|--------|----------|--------------------------|---------------------|---------------------|----------|
| NFR-001 | Performance | The checkout page shall load within 2 seconds on a 4G mobile connection | < 2 seconds at 95th percentile | Load testing via Lighthouse / WebPageTest | Must Have |
| NFR-002 | Performance | Payment processing (from "Place Order" click to confirmation) shall complete within 5 seconds | < 5 seconds at 95th percentile | Integration testing with payment gateway sandbox | Must Have |
| NFR-003 | Security | All payment data shall be transmitted using TLS 1.3 and shall not be stored on FreshCart servers (tokenization via PCI-compliant gateway) | 100% compliance | PCI-DSS audit, penetration testing | Must Have |
| NFR-004 | Scalability | The checkout module shall support 10,000 concurrent transactions during peak periods (e.g., holiday sales) without performance degradation | 10,000 concurrent users, < 2 sec page load | Load testing simulation | Must Have |
| NFR-005 | Availability | The checkout service shall maintain 99.95% uptime | < 4.4 hours downtime/year | Uptime monitoring (e.g., Datadog, Pingdom) | Must Have |
| NFR-006 | Usability & Accessibility | The checkout flow shall comply with WCAG 2.1 AA standards for screen reader compatibility and color contrast | Pass automated + manual accessibility audit | Accessibility audit tool (e.g., axe DevTools) + manual screen reader test | Must Have |
| NFR-007 | Compatibility | The checkout module shall function correctly on the latest two major versions of Chrome, Safari, Firefox, and Edge, and on iOS 16+/Android 12+ | 100% functional parity across listed platforms | Cross-browser testing (BrowserStack) | Should Have |
| NFR-008 | Data Retention & Privacy | Customer payment method tokens shall be retained only while the account is active; upon account deletion, tokens shall be purged within 30 days | 30-day purge SLA | Data retention audit log review | Must Have |

---

## Compliance & Regulatory Considerations

| Req ID | Regulation/Standard | Requirement |
|--------|---------------------|-------------|
| CR-001 | PCI-DSS | All cardholder data must be handled per PCI-DSS v4.0 requirements; FreshCart uses a tokenized payment gateway to minimize PCI scope |
| CR-002 | WCAG 2.1 AA | Checkout flow must be navigable via keyboard and compatible with screen readers (NVDA, VoiceOver) |
| CR-003 | CCPA/GDPR (where applicable) | Customers must be able to request deletion of stored payment data; deletion requests must be fulfilled within 30 days |

---

## Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1 | 2026-03-22 | J. Carter | Initial draft based on architecture review |
| 0.2 | 2026-03-30 | J. Carter | Added compliance section after legal review |
| 1.0 | 2026-04-02 | J. Carter | Approved by Engineering Lead and Compliance |
