---
title: Employee User Guide
status: Review
last-updated: 2026-05-04
owner: Technical Writer
---

# Employee User Guide

This guide covers everything an employee needs to use the Attendance Tracking system - from daily check-in to reading performance scores and using the AI chatbot.

---

## Logging In and Session Management

1. Navigate to the web app or open the mobile app.
2. Enter your registered email and password.
3. Your session remains active for **8 hours**. 
4. To log out manually, click your profile icon (top right) and select **Check Out**.

> Do not share your credentials or leave an active session unattended on a shared device.

---

## Daily Check-In and Check-Out

### Check-In
1. From the dashboard, click **Check In**.
2. A timestamp confirmation appears on screen. Your status updates to **Present**.

### Check-Out
1. Click **Check Out** after the end of  your workday.
2. Your **work hours for the day** are calculated as: `Logout Time − Login Time`.
3. The result appears on your dashboard under **Today's Work Hours**.

### Attendance Status Logic

| Status | Condition |
|---|---|
| **Present** | Checked in within the allowed login window |
| **Late** | Checked in after the configured late login threshold |
| **Half-Day** | Work hours fall below the minimum full-day threshold |
| **Absent** | No check-in recorded for the day |

> The late login threshold and minimum work hours are configured by your administrator. Contact HR if you believe your status is incorrect.

---

## Viewing Your Attendance Records

1. Go to **My Attendance** from the left navigation menu.
2. Use the **date range picker** to filter records by day, week or month.
3. Each row shows: Date, Login Time, Logout Time, Work Hours and Status.
4. Click any row to expand the detail view.

### Attendance Percentage
Your attendance percentage is displayed on the dashboard and calculated as:

```
Attendance Rate = (Days Present / Total Working Days) × 100
```

This figure updates daily and reflects the current calendar month by default.

---

## Reading Your Performance Score

Your performance score is a composite metric updated on a rolling basis. It is visible on your dashboard under **Performance**.

### Score Components

| Factor | What It Measures |
|---|---|
| Attendance Rate | Percentage of working days attended |
| Work Hours | Average daily hours compared to expected hours |
| Idle Time | Time gaps with no recorded activity |
| Overtime | Frequency of sessions extending beyond standard hours |

--

## Notifications

Notifications appear in the bell icon (top navigation bar) and, if enabled, are also pushed to your mobile device.

| Notification Type | Trigger |
|---|---|
| Check-In Reminder | Sent if no check-in is recorded by a configured time |
| Performance Update | Sent when your score changes significantly |
| System Announcement | General platform updates from your administrator |

To manage notification preferences, go to **Settings → Notifications**.