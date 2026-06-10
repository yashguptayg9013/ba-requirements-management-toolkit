# 📋 BA Requirements Management Toolkit

A reusable, ready-to-use toolkit of templates and worked examples for Business Analysts to manage requirements throughout a project lifecycle — from capturing functional/non-functional requirements, to writing user stories, to tracking changes and clarifying accountability.

Fork this repo, copy the templates into your project, and adapt them to your context.

---

## 📁 Repository Structure

```
ba-requirements-management-toolkit/
│
├── README.md                          ← You are here
│
├── templates/
│   ├── user_story_template.md         ← Blank user story format
│   ├── functional_requirements_template.md   ← Blank FR specification
│   ├── nonfunctional_requirements_template.md ← Blank NFR specification
│   ├── change_request_log_template.md ← Blank change request register
│   └── raci_matrix_template.md        ← Blank RACI matrix
│
└── examples/
    ├── user_story_examples.md         ← Filled-in user story examples
    ├── functional_requirements_examples.md  ← Filled-in FR examples
    ├── nonfunctional_requirements_examples.md ← Filled-in NFR examples
    ├── change_request_log_example.md  ← Filled-in change log
    └── raci_matrix_example.md         ← Filled-in RACI matrix
```

---

## 🧭 When to Use Each Template

| Template | When to Use It | Typical Owner |
|----------|----------------|---------------|
| **User Story Template** | During backlog grooming or sprint planning, when breaking down features into deliverable increments for an Agile team | BA / Product Owner |
| **Functional Requirements Template** | During requirements elicitation, to document *what the system must do* — features, behaviors, business rules | BA |
| **Non-Functional Requirements Template** | Alongside FRs, to document *how well the system must perform* — performance, security, usability, scalability | BA / Architect |
| **Change Request Log** | Throughout the project, whenever scope, requirements, or deliverables change after baseline approval | BA / Project Manager |
| **RACI Matrix** | At project kickoff and whenever new activities/decisions need clear ownership | BA / Project Manager |

---

## 🛠 How to Use This Toolkit

1. **Copy the relevant template(s)** from `/templates` into your own project repo or document
2. **Reference the matching example** in `/examples` to see how it's filled out in a real scenario
3. **Adapt field names and structure** to your organization's standards (e.g., Jira fields, Confluence templates)
4. **Maintain version history** — every template includes a document history table; keep it updated

---

## 📐 Standards & Frameworks Referenced

- **BABOK v3** (Business Analysis Body of Knowledge) — for requirements classification and elicitation techniques
- **INVEST criteria** — for writing good user stories (Independent, Negotiable, Valuable, Estimable, Small, Testable)
- **Given/When/Then (Gherkin)** — for acceptance criteria
- **MoSCoW** — for prioritization (Must/Should/Could/Won't)
- **PMI / PMBOK** — for change control and RACI conventions

---

## 🤝 Contributing

Found a way to improve a template? Have a useful variant for a different industry (healthcare, fintech, retail)? Feel free to fork and submit a pull request with your additions.

---

## ⭐ Why This Toolkit

Most BA templates online are either too generic or buried in 40-page documents. This toolkit is:

- **Lightweight** — copy-paste ready, no bloat
- **Practical** — every template has a worked example
- **Markdown-native** — works in GitHub, Notion, Confluence, or any markdown-based tool
- **Framework-aligned** — follows recognized BA standards without being overly rigid

---

*If this toolkit helped you, consider giving it a ⭐ — it helps other BAs find it too.*
