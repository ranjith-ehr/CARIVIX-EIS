09. attendance-tracking.md

- Data captured per session: login time, logout time
- Attendance status logic: Present / Absent / Late / Half-day rules
- Work hour calculation formula: Logout − Login
- Late login detection: threshold config and flagging logic
- Idle time identification: activity gap rules
- Edge cases: missed logout, duplicate records, timezone handling

---

7. performance-scoring.md

- Score components: attendance rate, work hours, late login count, idle time, overtime
- Weighting and normalization method
- Score range interpretation table (e.g., 0–40 = At Risk, 41–70 = Average, 71–100 = High Performer)
- How scores update: daily recalculation vs. rolling window
- Where scores appear: employee dashboard, Admin view, ML input
- SHAP-based explanation: which factors influenced a score

---

8. dashboards-and-reports.md

- Dashboard types: Employee Personal, Admin System
- Available widgets: attendance heatmap, work hour trend, anomaly count, performance distribution
- Filtering options: date range, department, individual employee
- Report types: Daily Summary, Weekly Attendance, Monthly Performance, Anomaly Report
- Export formats: CSV, PDF
- Scheduled report configuration: frequency, recipients, format
