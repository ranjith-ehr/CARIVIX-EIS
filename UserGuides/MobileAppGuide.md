---
title: Mobile App Guide
status: published
last-updated: 2026-05-04
owner: Technical Writer
---

# Mobile App Guide

This guide covers installation, permission setup, and all mobile-specific features of the Attendance Tracking app - built with React Native (Expo) for Android and iOS.

---

## Installation

### Android
1. Open the **Google Play Store**.
2. Search for **"CARIVIX - Attendance Tracker"**.
3. Tap **Install**. The app requires approximately 35 MB of storage.
4. Once installed, tap **Open**.

### iOS
1. Open the **App Store**.
2. Search for **"CARIVIX - Attendance Tracker"**.
3. Tap **Get** and authenticate with Face ID / Touch ID or your Apple ID password.
4. Once installed, tap **Open**.

> If the app is distributed internally (not via public app stores), your IT administrator will provide a direct installation link.

---

## Granting Required Permissions

On first launch, the app requests the following permissions. All three are required for full functionality.


### Location (Precise)
- **Purpose:** GPS-based validation at check-in.
- **When prompted:** Select **Allow While Using the App** (Android) or **Allow Once / Always** (iOS - select **While Using**).
- **If denied:** Go to device Settings → Privacy → Location Services → CARIVIX - Attendance Tracker → While Using.

> **Important:** Select **Precise Location** when given the option. 

### Notifications
- **Purpose:** Attendance reminders, anomaly alerts, and system announcements.
- **When prompted:** Tap **Allow**.
- **If denied:** Go to device Settings → Notifications → Attendance Tracker → Enable.

---

## Check-In
1. Tap **Check In** on the home screem.
2. Your work hours for the day will calculated from the Check In time.
3. 

## Check-Out

1. Tap **Check Out** on the home screen.
2. Your work hours for the day are displayed immediately after confirmation.

> If you forget to check out, the system will flag the session as incomplete. Contact your manager or HR to correct the record manually.

---

## Viewing Your Dashboard on Mobile

The mobile dashboard shows the same data as the web app, optimized for smaller screens:

| Section | Access |
|---|---|
| **Today's Status** | Visible on the home screen immediately after check-in |
| **Attendance Records** | Tap **My Attendance** in the bottom navigation |
| **Performance Score** | Tap **Performance** in the bottom navigation |
| **Notifications** | Tap the bell icon (top right) |


---

## Push Notifications

When notifications are enabled, the app delivers alerts in the following scenarios:

| Notification | Trigger |
|---|---|
| Check-In Reminder | Sent at a configured time if no check-in is recorded |
| System Announcement | Sent by your administrator for platform updates |

Tap any notification to open the relevant section of the app directly.

To manage notification preferences: **Profile → Settings → Notifications**.

---

## App Updates

The app updates automatically through the Play Store or App Store when a new version is available. If your organization distributes the app internally, your IT team will push updates via MDM.

Always keep the app updated to ensure compatibility with the latest backend features and security patches.

