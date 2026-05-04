---
title: FAQ - Admins
status: Review
last-updated: 2026-05-04
owner: Technical Writer
---

# FAQ - Admins

Answers to the most common questions from system administrators and HR administrators managing the Attendance Tracking platform.

---



## Attendance Rules

**How do I configure the late login threshold?**

Go to **Admin Console → Attendance Rules**. Set the **Work Start Time** and **Late Login Threshold** (in minutes). Any login after `Work Start Time + Threshold` is marked Late. Click **Save Rules**.

Department-level overrides are available by selecting a department from the dropdown before saving.

---

**Can I configure different rules for shift workers?**

Yes, via department-level rule overrides. Create an attendance rule set with the appropriate work start time for the shift and apply it to the relevant department. Employees in that department will be evaluated against the department rules rather than the global defaults.

---

**What happens if an employee works on a weekend or public holiday?**

Weekend and public holiday sessions are recorded but excluded from attendance rate and performance score calculations by default. They appear in the attendance record as **Overtime Session** and are visible in reports. If weekend shifts are standard for a role, contact your DevOps team to configure weekend working days for the relevant department.

---

## Anomaly Detection

**What triggers an anomaly alert?**

The Isolation Forest model scores each day's attendance record against the employee's behavioral baseline. Records that score above the anomaly threshold are flagged. Common triggers include:

- Sudden consecutive absences after a long consistent streak.
- Login times that deviate significantly from the employee's established pattern.
- Work hour durations that are abnormally short or long.
- Location mismatches or simultaneous location detections.

The system does not apply fixed global thresholds - it evaluates deviation relative to each employee's individual history.

---

**How do I dismiss a false positive?**

1. Go to **Alerts → Anomaly Flags** and open the flagged alert.
2. Review the session data.
3. Select **Dismiss as False Positive** and enter a required explanation note.
4. Click **Submit**.

Dismissed false positives are collected and used as negative training examples in the next model retraining cycle, improving accuracy over time.

---

**Can I adjust how aggressively the system flags anomalies?**

Yes. Go to **Admin Console → Alert Configuration → Anomaly Sensitivity** and set the level to **Low**, **Medium** (default), or **High**.

- **Low** - Flags only the most significant deviations. Fewer alerts, lower false positive rate.
- **High** - Flags more subtle deviations. More alerts, higher sensitivity.

Changes apply to all future anomaly scoring. Existing alerts are not re-evaluated.

---

## Machine Learning Models

**How do I manually trigger a model retraining job?**

1. Go to **Admin Console → ML Models**.
2. Find the model you want to retrain.
3. Click **Retrain** and confirm.

The job is queued on Cloud Run Jobs and typically completes within 15–30 minutes. Status updates from **Queued → Training → Completed** are visible on the ML Models page.

---

**When should I manually trigger retraining?**

Manual retraining is recommended after:

- A large batch of employee additions (more than 10% of total employee count).
- Corrections to a significant number of historical attendance records.
- Sustained high false positive rates that have not been resolved by threshold adjustment.
- Organizational changes such as a shift in working hours policy.

Scheduled retraining runs automatically on the configured frequency. Manual retraining is a supplement, not a replacement.

---

**A model is showing a "stale model" warning. What should I do?**

A stale model warning appears when the last training date is more than 2 weeks before the current date. Trigger a manual retraining job from **Admin Console → ML Models** to clear the warning.

---

## User Management


**What happens to an employee's data when their account is deactivated?**

Deactivating an account immediately prevents login. All historical attendance records, performance scores, task logs, and audit entries are retained in the database and remain accessible in reports and audit logs for administrators. Face embeddings are scheduled for deletion 30 days after deactivation.

Deactivated accounts can be reactivated by an admin - historical data will be restored.

---

**How do I pull an audit log for a specific employee?**

1. Go to **Admin Console → Audit Logs**.
2. Use the **User** filter to search by employee name or email.
3. Apply a date range filter as needed.
4. Click **Export (CSV)** to download the filtered log.

Audit logs are retained for 12 months by default.

---

## Reports and Data

**How do I export a report for a large date range?**

For reports that exceed 5,000 rows, the system automatically emails the export to your registered admin email address rather than triggering a direct download. The email is typically delivered within 5 minutes. If it has not arrived after 10 minutes, check your spam folder.

---

**Can I schedule a report for a specific department only?**

Yes. When generating a report, apply the **Department** filter before clicking **Generate Report**. Then click **Schedule** to save the filtered report as a recurring scheduled delivery. Department filters are preserved in the schedule.

---

## Related Docs

- [Admin User Guide](../user-guides/admin-user-guide.md)
- [Anomaly Detection](../features/anomaly-detection.md)
- [Common Errors](./common-errors.md)
- [Data Privacy and Security](../reference/data-privacy-and-security.md)
