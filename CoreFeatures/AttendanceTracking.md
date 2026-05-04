---
title: Attendance Tracking
status: Review
last-updated: 2026-05-04
owner: Technical Writer
---

# Attendance Tracking

This document describes how the system captures, calculates and classifies attendance data for every employee session.

---

## Details Captured Per Session

Every check-in and check-out session records the following:

| Field | Description |
|---|---|
| **Login Timestamp** | Date and time of check-in |
| **Logout Timestamp** | Date and time of check-out |
| **Attendance Status** | Computed classification (Present, Late, Half-Day, Absent) |
| **Task Activity Logs** | Activity events recorded during the session |

---

## Attendance Status Logic

The system assigns one status per employee per working day, determined as follows:

| Status | Condition |
|---|---|
| **Present** | Checked in within the late login threshold AND work hours ≥ minimum minimum hours |
| **Late** | Checked in after the late login threshold but work hours ≥ minimum minimum hours |
| **Half-Day** | Working hours fall between the minimum half-day and minimum full-day thresholds |
| **Absent** | No check-in recorded by end of the working day |

> Thresholds are configured by your administrator under **Attendance Rules**. 
```
Default values:
Late threshold = 15 minutes after 09:00
Full-day minimum = 8 hours
Half-day minimum = 4 hours.
```
---

## Work Hour Calculation

Work hours per session are calculated as:

```
Work Hours = Logout Time − Login Time
```

This is a gross duration - it does not subtract breaks unless idle time tracking is configured to exclude gap periods exceeding the idle time threshold.

---


## Idle Time Detection

Idle time is identified when no activity event is recorded for a period exceeding the configured idle threshold.

Idle time affects:
- The employee's session activity log.
- The Idle Time component of the performance score.

> Activity events are captured from task logs and system interactions recorded during the session.

---

## Attendance Rate Calculation  

The attendance rate is computed as:

```
Attendance Rate (%) = (Days Present / Total Working Days) × 100
```

- **Days Present** includes both Present and Late statuses.
- **Total Working Days** excludes weekends and public holidays as configured by the admin.
- The rate is calculated for the current calendar month by default and visible on the employee dashboard.