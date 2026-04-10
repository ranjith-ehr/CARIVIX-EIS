16. data-pipeline-overview.md

- Pipeline stages: Raw Ingestion → Cleaning → Transformation → Feature Engineering → ML-Ready Output
- Data formats at each stage: Parquet/CSV → cleaned DataFrame → scaled feature matrix
- Tools used per stage: Pandas, Scikit-learn (Min-Max scaler), custom Python/R scripts
- Trigger mechanism: scheduled jobs vs. event-driven ingestion
- Error handling in the pipeline: retry logic, dead-letter queue behavior
- Data lineage: how to trace a metric back to raw source

---

17. data-cleaning-rules.md

- Missing login/logout: detection logic and imputation or exclusion rules
- Duplicate record removal: deduplication key definition
- Invalid timestamp correction: rules for out-of-order or future-dated entries
- Logical consistency check: login must precede logout
- Format standardization: timestamp format, timezone normalization
- Cleaning output: clean record flags, rejection log schema

---

18. api-reference.md (OpenAPI/Swagger style)

- OpenAPI 3.0 spec header: base URL, auth scheme (JWT Bearer)
- Blueprints covered: session_bp, attendance_bp, task_bp, activity_bp
- Per endpoint: GET/POST/PUT/DELETE, path, path/query/body parameters, request schema, response schema (200/400/401/404/500), example request + response
- Authentication: token acquisition, expiry, refresh flow
- Rate limiting headers
- Error response envelope schema

---

19. database-schema.md

- PostgreSQL tables: employees, attendance_logs, performance_scores, anomaly_flags, task_logs
- Per table: column name, data type, constraints, description
- Foreign key relationships and ER diagram reference
- Redis usage: session token storage, cache key patterns, TTL values
- Index definitions for performance-critical queries
- Migration versioning note

---

20. third-party-integrations.md

- GCP services table: service name, purpose, how the system uses it
- Cloud Run: backend API and ML job hosting
- Cloud SQL: managed PostgreSQL config
- BigQuery ML: batch ML job execution
- GPU Compute Engine: face recognition and LLM inference
- Memorystore (Redis): session and cache layer
- Cloud Monitoring + Grafana: metrics and alerting setup
- Terraform: IaC configuration overview