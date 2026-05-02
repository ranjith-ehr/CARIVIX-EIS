# AI-Based Attendance Tracking & Employee Management System
## Knowledge Base - README

---

## Project Overview

This repository contains the full Knowledge Base (KB) for the **AI-Based Attendance Tracking and Employee Management System** - a platform that integrates machine learning, facial recognition, NLP, GIS, and cloud computing to automate and intelligently manage workforce attendance.

The KB is split into two destinations based on audience and sensitivity:

| Destination | Audience | Access |
|---|---|---|
| `docs` | Employees, HR, Managers | Public / Role-gated |
| `Internal Wiki` | Developers, ML Engineers, DevOps | Restricted |

---

## Repository Structure

```
/
├── docs-site/                        # Public-facing documentation (docs)
│   ├── getting-started/
│   │   ├── product-overview.md
│   │   ├── system-requirements.md
│   │   └── quick-start-guide.md
│   │
│   ├── user-guides/
│   │   ├── employee-user-guide.md
│   │   ├── admin-user-guide.md
│   │   ├── mobile-app-guide.md
│   │
│   ├── features/
│   │   ├── performance-scoring.md
│   │   └── dashboards-and-reports.md
│   │
│   ├── troubleshooting/
│   │   ├── common-errors.md
│   │   ├── faq-employees.md
│   │   └── faq-admins.md
│   │
│   └── reference/
│       ├── glossary.md
│       ├── release-notes.md
│       └── data-privacy-and-security.md
│
└── internal-wiki/                    # Internal documentation (restricted)
    └── testing/
        ├── testing-overview.md
        ├── api-testing-guide.md
        └── ml-model-testing.md 
```

---

## Tech Stack

| Layer | Technology |
|---|---|

---

## Writing Guidelines

### Audience
- **docs** - Written for technically literate employees and HR. Assume familiarity with SaaS tools but not with infrastructure or ML internals. Avoid jargon; link to Glossary when technical terms are unavoidable.
- **Internal Wiki** - Written for developers, ML engineers, and DevOps. Assume full technical proficiency. Include code snippets, schema definitions, config examples, and command references.


### Doc Status Labels
Use the following front-matter status tags in each document:

```
status: draft | review | published | deprecated
last-updated: YYYY-MM-DD
owner: [team or person]
```

---

## Related Resources
- **Glossary:** - Definitions for all system-specific and ML/AI terms.
- **Release Notes:**- Version history and changelog.
