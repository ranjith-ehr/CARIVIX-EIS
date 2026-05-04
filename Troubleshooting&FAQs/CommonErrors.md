---
title: Common Errors
status: Review
last-updated: 2026-05-04
owner: Technical Writer
---

# Common Errors

This document lists the most common errors encountered across the system, organized by module, with their likely causes and resolution steps.

---

## Authentication Errors

| Error Code | Message | Likely Cause | Resolution |
|---|---|---|---|
| `INVALID_CREDENTIALS` | Email or password is incorrect. | Wrong email or password entered. | Re-enter credentials. Use **Forgot Password** if needed. |
| `TOKEN_EXPIRED` | Your session has expired. Please log in again. | JWT token has passed the 8-hour expiry. | Log in again or use the token refresh endpoint. |
| `TOKEN_INVALID` | Authentication token is invalid. | Token is malformed or was used after logout. | Log in again to obtain a new token. |
| `ACCOUNT_LOCKED` | Your account has been locked after multiple failed login attempts. | 5 or more consecutive failed login attempts. | Contact your administrator to unlock the account. |
| `ACCOUNT_INACTIVE` | This account has been deactivated. | Account was deactivated by an admin. | Contact your HR team or administrator. |

---

## Check-In and Check-Out Errors

| Error Code | Message | Likely Cause | Resolution |
|---|---|---|---|
| `ALREADY_CHECKED_IN` | You have already checked in today. | A check-in record exists for today. | Proceed to check-out when the workday ends. Contact HR if you need to correct a duplicate. |
| `NO_ACTIVE_CHECKIN` | No active check-in found for today. | Check-out attempted without a prior check-in. | Contact your manager to log a manual attendance record. |
| `GPS_TIMEOUT` | Location could not be determined. Please check your GPS settings. | GPS lock failed - device location services may be off or signal is poor. | Enable precise location permission. Move closer to a window and retry. |
| `SESSION_INCOMPLETE` | Your previous session was not properly closed. | A prior check-in has no corresponding check-out. | Contact your manager or HR to correct the open session. |

---

## API Errors

| HTTP Status | Error Code | Message | Cause | Resolution |
|---|---|---|---|---|
| `400` | `BAD_REQUEST` | The request could not be understood. | Malformed JSON body or invalid parameter type. | Review the request body against the API reference. |
| `401` | `UNAUTHORIZED` | Authentication required. | Missing or invalid `Authorization` header. | Include a valid Bearer token in the request header. |
| `403` | `FORBIDDEN` | You do not have permission to perform this action. | Authenticated user's role does not have access. | Verify the required role for the endpoint in the API reference. |
| `404` | `NOT_FOUND` | The requested resource was not found. | Invalid record ID or resource does not exist. | Confirm the ID is correct. |
| `422` | `VALIDATION_ERROR` | One or more fields failed validation. | Missing required fields or field format mismatch. | Check the `details` field in the response for field-level errors. |
| `429` | `RATE_LIMIT_EXCEEDED` | Too many requests. Please wait before retrying. | Exceeded 60 requests/minute per user. | Back off and retry after the time indicated in `X-RateLimit-Reset`. |
| `500` | `INTERNAL_SERVER_ERROR` | An unexpected error occurred. Please try again. | Unhandled server-side exception. | Retry after a few seconds. If persistent, contact your administrator. |


---

## Mobile App Errors

| Error | Likely Cause | Resolution |
|---|---|---|
| **Camera permission denied** | App does not have camera access. | Go to device Settings → Apps → Attendance Tracker → Permissions → Camera → Allow. |
| **Location permission denied** | App does not have location access. | Go to device Settings → Privacy → Location → Attendance Tracker → While Using. |
| **App crashes on check-in** | Outdated app version or low device memory. | Update the app to the latest version. Close background apps to free memory. |
| **Offline - check-in unavailable** | Device has no internet connection. | Connect to Wi-Fi or mobile data before attempting check-in. |
| **Notification not received** | Notification permission denied, or app is in battery-saver mode. | Enable notifications in device settings and disable battery optimization for the app. |

---

## Data and Report Errors

| Error | Likely Cause | Resolution |
|---|---|---|
| **Attendance record shows Absent - I checked in** | Login credentials or Record is missing | Check your session detail in My Attendance. Contact HR for a manual correction if the record is missing. |
| **Work hours show 0 for a completed day** | Logout was not recorded - session is incomplete. | Contact your manager to log a manual check-out time. |
| **Report export failed** | Export request timed out (large dataset). | Wait a few minutes - large exports are emailed automatically. Check your inbox. |
| **Scheduled report not received** | Email address is incorrect, or email went to spam. | Verify the recipient address in Scheduled Reports settings. Check your spam folder. |
| **Performance score not updating** | Score recalculation runs nightly. Score from yesterday will reflect today's data the following morning. | Wait until the next morning. If still not updated after 24 hours, contact your administrator. |

---

## Related Docs

- [FAQ - Employees](./faq-employees.md)
- [FAQ - Admins](./faq-admins.md)
- [API Reference](../api-reference/api-reference.md)
