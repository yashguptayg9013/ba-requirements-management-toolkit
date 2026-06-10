# Non-Functional Requirements (NFR) Template

> Use this template to document **how well the system must perform** — quality attributes such as performance, security, usability, scalability, reliability, and compliance. NFRs are often forgotten but are frequently the cause of project failure if not defined early.

---

## Document Control

| Field | Value |
|-------|-------|
| **Project Name** | [Project name] |
| **Document ID** | [e.g., PROJ-NFR-001] |
| **Version** | [Version number] |
| **Date** | [Date] |
| **Author** | [BA name] |
| **Status** | [Draft / In Review / Approved] |

---

## NFR Categories Checklist

Use this checklist to ensure no category is overlooked during elicitation:

- [ ] Performance (response time, throughput)
- [ ] Scalability (load, concurrent users, growth)
- [ ] Availability & Reliability (uptime, failover)
- [ ] Security (authentication, encryption, access control)
- [ ] Usability & Accessibility (WCAG, ease of use)
- [ ] Maintainability (code quality, documentation)
- [ ] Compatibility (browsers, devices, OS versions)
- [ ] Compliance & Legal (industry regulations, data residency)
- [ ] Data Retention & Privacy
- [ ] Disaster Recovery / Backup

---

## Non-Functional Requirements

| Req ID | Category | Requirement Description | Target / Threshold | Measurement Method | Priority |
|--------|----------|--------------------------|---------------------|---------------------|----------|
| NFR-001 | Performance | [The system shall...] | [e.g., < 3 seconds] | [e.g., load testing tool, 95th percentile] | [Must/Should] |
| NFR-002 | Security | | | | |
| NFR-003 | Usability | | | | |
| NFR-004 | Scalability | | | | |
| NFR-005 | Availability | | | | |

---

## Writing Guidelines

NFRs must be **measurable**, not aspirational. Each NFR should answer: "How would we test/verify this?"

### ❌ Poor Example
> "The system should be fast and secure."

### ✅ Good Example
> "NFR-007: The system shall encrypt all data in transit using TLS 1.3, verified via automated security scanning before each release."

> "NFR-012: The system shall support 5,000 concurrent users with page load times under 3 seconds at the 95th percentile, verified through load testing prior to launch."

---

## Compliance & Regulatory Considerations

| Req ID | Regulation/Standard | Requirement |
|--------|---------------------|-------------|
| CR-001 | [e.g., GDPR, HIPAA, PCI-DSS, WCAG 2.1] | [Specific requirement] |

---

## Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1 | [Date] | [Name] | Initial draft |
