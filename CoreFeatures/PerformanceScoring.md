---
title: Performance Scoring
status: Review
last-updated: 2026-05-04
owner: Technical Writer
---

# Performance Scoring

The performance score is a composite metric that measures an employee's attendance behavior over time. It is updated on a rolling basis and serves as both a personal indicator and an input to the system's machine learning models.

---

## Score Components

The score is built from five factors, each weighted and normalized before being combined into the final score (0–100).

| Factor | What It Measures | Impact |
|---|---|---|
| **Attendance Rate** | Percentage of working days the employee was present (Present or Late) | High |
| **Work Hours** | Average daily work hours compared to the expected minimum | High |
| **Late Login Count** | Frequency of late check-ins within the scoring window | Medium |



> Overtime is a positive contributor - it reflects additional time committed. It does not offset other negative factors but adds to the overall score.

---

## Scoring Window

| Setting | Default |
|---|---|
| **Calculation frequency** | Daily  |
| **Display on dashboard** | Current score + 30-day trend sparkline |

The 30-day rolling window means the score responds gradually to behavioral changes - a single missed day does not immediately collapse the score, and consistent improvement is reflected over 2–4 weeks.