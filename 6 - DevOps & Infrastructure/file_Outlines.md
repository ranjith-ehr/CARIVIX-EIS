24. system-architecture.md

- Full architecture diagram (annotated)
- Layer breakdown: Frontend → API Gateway → Flask Backend → Data Pipeline → ML Layer → Storage
- Request lifecycle walkthrough: employee check-in end-to-end
- Blueprint routing structure: which blueprint handles which domain
- WTForms validation layer: form types and validation rules
- Inter-service communication: REST, WebSocket (Socket.io), async job queues

---

25. cloud-deployment-guide.md

- GCP project setup: required APIs, IAM roles
- Cloud Run: Dockerfile requirements, env vars, scaling config, CPU/memory limits
- Cloud SQL: instance config, connection via Cloud SQL Auth Proxy, migration steps
- GPU Compute Engine VM: setup for face recognition service and LLM inference
- Memorystore: Redis instance creation, connection string format
- Environment variable reference table: all required vars per service

---

26. cicd-pipeline.md

- Pipeline overview diagram: GitHub → Actions → Docker → Artifact Registry → Terraform → Cloud Run
- GitHub Actions workflow file structure
+ Automated test gate: what must pass before build
- Docker image build and tagging convention
- Artifact Registry: image naming, retention policy
+ Terraform: modules used, state backend, apply process
- Rollback procedure: how to revert a failed deployment

---

27. monitoring-and-alerts.md

- Metrics collected: API latency, error rate, ML inference time, DB query time, active sessions
- Cloud Monitoring dashboard: key metrics panels
- Grafana: dashboard setup, data source config (Cloud Monitoring)
- Alert policies: threshold definitions per metric, notification channels (email, Slack)
- Log-based alerts: log filter patterns for critical errors
- Incident response runbook: detect → triage → escalate → resolve → post-mortem