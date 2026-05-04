---
title: FAQ - Employees
status: Review
last-updated: 2026-05-04
owner: Technical Writer
---

# FAQ - Employees

Answers to the most common questions employees have about using the Attendance Tracking system.

---

## Check-In and Attendance

**Why was I marked Absent when I checked in?**

Session not saved or page refreshed before confirmationn, causing the session not to be saved. Check your attendance record under **My Attendance** to see if a check-in exists for that day. If no record appears:

1. Contact your manager to log a manual attendance entry.
2. Provide your approximate login time and any context.

A manual entry will be flagged in the record but counted toward your attendance rate.

---

**Can I check in more than once a day?**

No, only one check-in per session/day is allowed

---

**I forgot to check out yesterday. What happens to my record?**

Your session is marked as incomplete and your work hours for that day cannot be calculated automatically. Contact your manager and provide the approximate time you left. Your manager can enter a manual check-out time from the Manager Dashboard. The correction will appear in your record within a few minutes.

---
**What should I do if the check-in button is not working?**

Refresh the page
Check your internet connection
Try logging in again

---

**Can I check in from any device?**

Yes, you can check in from any device with access to the dashboard (mobile/laptop), depending on system permissions.

---

## Attendance Records and Percentage

**How is my attendance percentage calculated?**

```
Attendance Rate (%) = (Days Present / Total Working Days) × 100
```

Days where you were marked **Present** or **Late** count as attended. **Absent** and incomplete sessions do not count. The total working days figure excludes weekends and public holidays as configured by your administrator.

---

**Why do I have a "Late" status when I was only a few minutes late?**

The late login threshold is configured by your administrator - it is typically 15 minutes after the work start time (e.g., if work starts at 09:00, any login after 09:15 is marked Late). Contact HR if you believe the threshold is set incorrectly for your role or shift.

---

**How far back can I see my attendance records?**

Your attendance records are available for the past 12 months. Use the date range filter in **My Attendance** to navigate to earlier dates.

---

## Performance Score

**How is my performance score calculated?**

Your score (0–100) is a weighted combination of five factors:

- **Attendance Rate** - Percentage of working days attended (highest weight).
- **Work Hours** - Average daily hours vs. expected minimum.
- **Late Login Count** - Frequency of late check-ins (negative impact).
- **Idle Time** - Gaps of inactivity during your sessions (negative impact).
- **Overtime Frequency** - How often you work beyond standard hours (positive impact).

The score updates nightly using a 30-day rolling window, so it reflects your recent behavioral trend rather than a single day's data.

---

**Why did my score drop this week?**

Click **Score Breakdown** on your dashboard to see which factors changed. Common causes of a score drop include:

- An increase in late logins.
- A day or more of absence.
- Sessions with unusually low work hours.

The breakdown includes a plain-language explanation of the top contributing factors.

---

**Can I dispute or appeal my performance score?**

The performance score is generated automatically from recorded attendance data. If you believe the underlying data is incorrect (for example, an attendance record that was not properly corrected), contact your manager or HR to correct the source record. The score will recalculate in the next nightly run.

---



## Account and Privacy

**What data does the system store about me?**

The system records: attendance check-in/out timestamps, GPS coordinates at check-in, face verification results (not raw photos), task logs, work hours, performance scores, and anomaly flags. See [Data Privacy and Security](../reference/data-privacy-and-security.md) for the full data inventory and retention policy.

---
**How do I keep my account secure?**
Use a strong password (mix of letters, numbers, symbols)
Do not share your login credentials with anyone
Always log out after using the dashboard

---

**How do I update my password?**

Go to **Profile → Settings → Change Password**. Enter your current password and your new password (minimum 8 characters, one uppercase, one number, one special character). Click **Save**.

---

## Related Docs

- [Employee User Guide](../user-guides/employee-user-guide.md)
- [Common Errors](./common-errors.md)
- [Performance Scoring](../features/performance-scoring.md)
- [Data Privacy and Security](../reference/data-privacy-and-security.md)
