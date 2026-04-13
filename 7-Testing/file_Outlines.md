28. testing-overview.md

- Testing strategy: what is tested, at which stage (unit, integration, E2E, ML)
- Test types matrix: Functional / API / UI / ML / Regression - tools, scope, trigger
- Coverage targets per module
+ Test environment setup: local vs. staging
- How to run the full test suite
- CI test gate: which tests block deployment

---

29. api-testing-guide.md

- Postman collection structure: folders per blueprint, environment variables
+ Auth setup in Postman: JWT token retrieval and variable injection
- Test case structure: endpoint, input, expected status, expected response fields
+ Rest Assured: test class structure, assertion examples
+ Common failure patterns and what they indicate
- How to add a new test case for a new endpoint

---

30. ml-model-testing.md

- Input validation tests: schema checks, range checks, null handling per model
- Output range verification: expected output bounds per model
- Anomaly detection accuracy: precision/recall benchmarks, test dataset description
- Model consistency tests: same input → same output across runs (seed control)
- Regression test trigger: conditions that require re-running the full ML test suite
- How to interpret test failure: model drift vs. data issue vs. code bug