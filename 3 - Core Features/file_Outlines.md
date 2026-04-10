09. attendance-tracking.md

- Data captured per session: login time, logout time, GPS, face verification result
- Attendance status logic: Present / Absent / Late / Half-day rules
- Work hour calculation formula: Logout − Login
- Late login detection: threshold config and flagging logic
- Idle time identification: activity gap rules
- Edge cases: missed logout, duplicate records, timezone handling

---

10. face-recognition.md

- How facial embedding is generated and stored
- Enrollment process: steps, photo requirements, retry rules
- Verification at check-in: match threshold and confidence score
- Re-enrollment triggers (appearance change, repeated failure)
- Failure handling: fallback to manual check-in, alert generation
- Privacy note: where embeddings are stored, retention policy

---

11. gis-location-validation.md

- How geofencing works: polygon/radius definitions per office zone
- GPS check-in validation flow
- Checks performed: zone membership, travel distance plausibility, simultaneous location detection
- Alert types: outside zone, unrealistic travel, duplicate location
- Admin configuration: adding/editing geofence zones
- Accuracy limitations and edge cases (GPS drift, indoor locations)

---

12. performance-scoring.md

- Score components: attendance rate, work hours, late login count, idle time, overtime
- Weighting and normalization method
- Score range interpretation table (e.g., 0–40 = At Risk, 41–70 = Average, 71–100 = High Performer)
- How scores update: daily recalculation vs. rolling window
- Where scores appear: employee dashboard, manager view, ML input
- SHAP-based explanation: which factors influenced a score

---

13. anomaly-detection.md

- What qualifies as an anomaly (defined thresholds)
- Anomaly types: sudden absenteeism, suspicious login pattern, unrealistic work hours, location mismatch
- Isolation Forest model: how it scores records, decision threshold
- Anomaly lifecycle: detected → flagged → reviewed → resolved/dismissed
- Alert routing: who gets notified and when
- False positive handling and feedback loop

---

14. predictive-analytics.md

- What is forecasted: individual attendance trends, team availability
- XGBoost regression: input features, output (performance score prediction)
- Time-series forecasting: model type, forecast horizon, confidence interval
- Employee classification output: Consistent / Irregular / High-Risk categories
- How to read forecast charts on the dashboard
- Retraining triggers and data freshness requirements

---

15. dashboards-and-reports.md

- Dashboard types: Employee Personal, Manager Team, Admin System
- Available widgets: attendance heatmap, work hour trend, anomaly count, performance distribution
- Filtering options: date range, department, individual employee
- Report types: Daily Summary, Weekly Attendance, Monthly Performance, Anomaly Report
- Export formats: CSV, PDF
- Scheduled report configuration: frequency, recipients, format