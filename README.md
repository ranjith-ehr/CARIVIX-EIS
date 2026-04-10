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
│   │   ├── manager-user-guide.md
│   │   ├── admin-user-guide.md
│   │   ├── mobile-app-guide.md
│   │   └── chatbot-interaction-guide.md
│   │
│   ├── features/
│   │   ├── attendance-tracking.md
│   │   ├── face-recognition.md
│   │   ├── gis-location-validation.md
│   │   ├── performance-scoring.md
│   │   ├── anomaly-detection.md
│   │   ├── predictive-analytics.md
│   │   └── dashboards-and-reports.md
│   │
│   ├── api-reference/
│   │   └── api-reference.md          # OpenAPI 3.0 specification
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
    ├── data-engineering/
    │   ├── data-pipeline-overview.md
    │   ├── data-cleaning-rules.md
    │   └── database-schema.md
    │
    ├── machine-learning/
    │   ├── ml-models-reference.md
    │   ├── model-optimization.md
    │   └── nlp-chatbot-architecture.md
    │
    ├── backend-architecture/
    │   ├── system-architecture.md
    │   └── third-party-integrations.md
    │
    ├── devops-infrastructure/
    │   ├── cloud-deployment-guide.md
    │   ├── cicd-pipeline.md
    │   └── monitoring-and-alerts.md
    │
    └── testing/
        ├── testing-overview.md
        ├── api-testing-guide.md
<<<<<<< HEAD
        └── ml-model-testing.md 
=======
        └── ml-model-testing.md
>>>>>>> 98ea5c5420f84fb0fd55bfea407ec09581da09bf
```

---

## Document Count

| Section | Location | Count |
|---|---|---|
| Getting Started | docs | 3 |
| User Guides | docs | 5 |
| Core Features | docs | 7 |
| API Reference | docs | 1 |
| Troubleshooting & FAQs | docs | 3 |
| Reference | docs | 3 |
| Data Engineering | Internal Wiki | 3 |
| Machine Learning | Internal Wiki | 3 |
| Backend Architecture | Internal Wiki | 2 |
| DevOps & Infrastructure | Internal Wiki | 3 |
| Testing | Internal Wiki | 3 |
| **Total** | | **36** |

---

<<<<<<< HEAD
## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | Web App, React Native / TypeScript |
=======
## Tech Stack (System Being Documented)

| Layer | Technology |
|---|---|
| Frontend | Web App, React Native (Expo) / TypeScript |
>>>>>>> 98ea5c5420f84fb0fd55bfea407ec09581da09bf
| Backend | Flask (Python), Gunicorn/WSGI |
| Database | PostgreSQL (Cloud SQL), Redis (Memorystore) |
| ML Models | XGBoost, Logistic Regression, Isolation Forest, Time-Series |
| NLP / Chatbot | LLaMA 3 / Mistral, DistilBERT, spaCy, LangChain, FAISS/Pinecone |
| Face Recognition | Custom model on GPU Compute Engine |
| GIS | GPS geofencing, location anomaly detection |
| Cloud | Google Cloud Platform (Cloud Run, Cloud SQL, BigQuery ML, GCE) |
| CI/CD | GitHub Actions, Docker, Terraform, Artifact Registry |
| Monitoring | Cloud Monitoring, Grafana |

---

## Writing Guidelines

### Audience
<<<<<<< HEAD
- **docs** - Written for technically literate employees and HR. Assume familiarity with SaaS tools but not with infrastructure or ML internals. Link to Glossary when technical terms are unavoidable.
- **Internal Wiki** - Written for developers, ML engineers, and DevOps. Assuming full technical proficiency. Included code snippets, schema definitions, config examples and command references.



### Doc Status Labels
=======
- **docs** - Written for technically literate employees and HR. Assume familiarity with SaaS tools but not with infrastructure or ML internals. Avoid jargon; link to Glossary when technical terms are unavoidable.
- **Internal Wiki** - Written for developers, ML engineers, and DevOps. Assume full technical proficiency. Include code snippets, schema definitions, config examples, and command references.

### Style
- Use active voice and present tense throughout.
- Each doc starts with a one-sentence purpose statement.
- Procedures use numbered steps. Reference material uses tables.
- API reference follows OpenAPI 3.0 specification format.
- Screenshots and diagrams are stored in `/assets/images/` and referenced by relative path.

### Doc Status Labels
Use the following front-matter status tags in each document:

>>>>>>> 98ea5c5420f84fb0fd55bfea407ec09581da09bf
```
status: draft | review | published | deprecated
last-updated: YYYY-MM-DD
owner: [team or person]
```

---

## Contributing

1. Create a branch from `main` using the naming convention `docs/<doc-name>`.
2. Write or update the document following the Writing Guidelines above.
3. Submit a Pull Request with a short description of what changed and why.
4. Assign review to the relevant owner (HR, Engineering, or DevOps lead).
5. On approval, merge and update `last-updated` in the document front matter.

<<<<<<< HEAD
=======
### Adding a New Document
- Place it in the correct folder based on the audience split above.
- Add it to the structure table in this README.
- Link it from the relevant parent doc (e.g., add a "See also" reference).

---

## Key Contacts

| Role | Responsible For |
|---|---|
| Technical Writer | Overall KB structure, docs content |
| Backend Lead | API reference, system architecture docs |
| ML Engineer | ML models reference, optimization, chatbot architecture |
| DevOps Lead | Deployment, CI/CD, monitoring docs |
| HR Lead | Employee/manager user guides, FAQs |

>>>>>>> 98ea5c5420f84fb0fd55bfea407ec09581da09bf
---

## Related Resources

<<<<<<< HEAD
- **API Spec:** `docs-site/api-reference/api-reference.md` - OpenAPI 3.0 spec for all backend endpoints.
- **Glossary:** `docs-site/reference/glossary.md` - Definitions for all system-specific and ML/AI terms.
- **Release Notes:** `docs-site/reference/release-notes.md` - Version history and changelog.
=======
- **Source Document:** `Final_Draft_Attendance_Tracking.docx` - Original system design draft this KB is based on.
- **API Spec:** `docs-site/api-reference/api-reference.md` - OpenAPI 3.0 spec for all backend endpoints.
- **Glossary:** `docs-site/reference/glossary.md` - Definitions for all system-specific and ML/AI terms.
- **Release Notes:** `docs-site/reference/release-notes.md` - Version history and changelog.
>>>>>>> 98ea5c5420f84fb0fd55bfea407ec09581da09bf
