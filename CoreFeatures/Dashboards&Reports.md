---
title: Dashboards and Reports
status: published
last-updated: 2026-05-02
owner: Technical Writer
---

# Dashboards and Reports

The system provides real-time dashboards and on-demand or scheduled reports for employees and administrators. This document describes the available dashboard views, report types, filtering options, and export and scheduling capabilities.

---

## Dashboard Types

### Employee Personal Dashboard
Available to all employees after login. Displays data scoped to the logged-in user only.

| Widget | Description |
|---|---|
| **Today's Status** | Current attendance status (Present, Late, Absent) and check-in time |
| **Monthly Attendance Summary** | Present / Absent / Late counts for the current calendar month |
| **Attendance Rate** | Attendance percentage for the current month |
| **Work Hours Trend** | Daily work hours plotted over the last 14 days |
| **Performance Score** | Current score, classification, and 30-day trend sparkline |
| **Active Anomaly Flags** | Count of open anomaly flags on the account (if any) |
| **Notifications** | Latest system alerts and reminders |



### Admin System Dashboard
Available to Admin roles only. Provides platform-level health and configuration status.

| Widget | Description |
|---|---|
| **Active Users** | Current logged-in session count |
| **System Health** | API status, error rate, DB connection pool usage |
| **ML Model Status** | Last trained date and status for each model |
| **Recent Audit Events** | Last 10 audit log entries |


---

## Filtering Options

All dashboards and report views support the following filters:

| Filter | Available Values |
|---|---|
| **Date Range** | Today, This Week, This Month, Last 30 Days, Custom Range |
| **Status** | Present, Absent, Late, Half-Day |
| **Department** | All departments or specific department by Admin only |
| **Employee** | Individual employee search by  Admin only |
| **Anomaly Type** | Filter by specific anomaly category  Admin |

Filters can be combined. Applied filters persist within the session.

---

## Report Types

### Daily Attendance Summary
- Scope: All team members  or all employees (Admin).
- Content: Date, employee name, status, login time, logout time, work hours, late flag.
- Typical use: End-of-day attendance verification.

### Weekly Work Hours Report
- Scope: Team or individual.
- Content: Daily work hours per employee for the selected week, total weekly hours, deviation from expected.
- Typical use: HR overtime and compliance review.

### Monthly Performance Report
- Scope: Team or individual.
- Content: Performance scores, classification, score components (attendance rate, work hours, late logins, idle time), 30-day trend.
- Typical use: Monthly HR review and employee feedback sessions.

### Anomaly Summary Report
- Scope: Team or organization (Admin).
- Content: Anomaly type, employee, date, severity, resolution status, resolution action taken.
- Typical use: HR compliance and pattern review.

### Predictive Analytics Report
- Scope: Organization (Admin).
- Content: Attendance forecast (7 days), employee classification, absenteeism risk list.
- Typical use: Workforce planning and proactive HR intervention.

---

## Generating a Report

1. Go to **Reports** from the left navigation.
2. Select a report template.
3. Set the date range and any additional filters.
4. Click **Generate Report**.
5. Preview the report in-browser. For large datasets (more than 1,000 rows), generation may take up to 30 seconds.

---

## Exporting Reports

| Export Format | Best For |
|---|---|
| **CSV** | Further analysis in Excel or data tools |
| **PDF** | Sharing, printing, or archiving |

To export:
1. Generate the report.
2. Click **Export** in the top right of the report view.
3. Select **CSV** or **PDF**.
4. The file downloads immediately for reports under 5,000 rows. Larger exports are emailed to the logged-in user's address within 5 minutes.

---

## Scheduling Automated Reports

Admins can configure reports to deliver automatically on a recurring schedule.

1. Generate and preview the report.
2. Click **Schedule** (top right of report view).
3. Configure:

| Setting | Options |
|---|---|
| **Frequency** | Daily, Weekly (specify day), Monthly (specify date) |
| **Delivery Time** | Select time - default is 08:00 local time |
| **Format** | CSV or PDF |
| **Recipients** | One or more email addresses |

4. Click **Save Schedule**. The schedule appears under **Reports → Scheduled Reports**.
5. To edit or delete a schedule, go to **Scheduled Reports**, find the entry, and click **Edit** or **Delete**.

---

## Related Docs

- [Predictive Analytics](./predictive-analytics.md) - Forecast data shown in dashboards.
- [Anomaly Detection](./anomaly-detection.md) - Alert data shown in the manager dashboard.
- [Performance Scoring](./performance-scoring.md) - Score data shown in performance widgets.
- [Admin User Guide](../user-guides/admin-user-guide.md) - System dashboard and audit log access.
