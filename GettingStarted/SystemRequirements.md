---
title: System Requirements
status: published
last-updated: 2026-05-04
owner: Technical Writer
---

# System Requirements

Before using the Attendance Tracking system, verify that your device, browser, and network meet the requirements listed below. Both the web app and the mobile app have specific prerequisites to support GPS Access, and real-time notifications.

---

## Web Application

### Supported Browsers

| Browser | Minimum Version | Notes |
|---|---|---|
| Google Chrome | 110+ | Recommended |
| Mozilla Firefox | 110+ | Fully supported |
| Microsoft Edge | 110+ | Chromium-based only |
| Safari | 16+ | macOS and iOS |

> **Note:** Internet Explorer is not supported.

### Operating System

| OS | Minimum Version |
|---|---|
| Windows | 10 (64-bit) |
| macOS | Ventura (13.0) |
| Ubuntu / Debian Linux | 20.04 LTS+ |

### Hardware (Web)

| Component | Requirement |
|---|---|
| RAM | 4 GB minimum, 8 GB recommended |
| Display Resolution | 1280 × 720 minimum |

---

## Mobile Application

### Platform Support

| Platform | Minimum Version |
|---|---|
| Android | 11 |
| iOS | 15.0 |

### Required Device Permissions

The mobile app requires the following permissions to be granted before first use:

| Permission | Purpose |
|---|---|
| **Location (Precise)** | GPS-based location access |
| **Notifications** | Attendance alerts and reminders |



### Hardware (Mobile)

| Component | Requirement |
|---|---|
| GPS Chip | Required for location Access |
| Storage | 150 MB free space for app installation |

---

## Network Requirements

| Requirement | Detail |
|---|---|
| Connection Type | Wi-Fi or 4G/5G mobile data |
| Minimum Bandwidth | 2 Mbps |
| Recommended Bandwidth | 10 Mbps+ for smooth face verification |
| Firewall | Allow outbound HTTPS to the platform domain |
| VPN | Supported, GPS validation remains active regardless of VPN |

> If your organization uses a corporate proxy or firewall, ask your IT administrator to allowlist the platform API domain.

---

## Backend Dependencies

> This section is relevant to IT administrators and system integrators.

| Dependency | Version |
|---|---|
| PostgreSQL | 14+ |
| Redis | 7+ |
| Google Cloud Platform | Cloud Run, Cloud SQL, Memorystore, GPU Compute Engine |
| Python | 3.10+ |
| Node.js | 18+ |

---

## Not Supported

- Internet Explorer
- Android versions below 11
- iOS versions below 15
- Devices without a front-facing camera
- Devices without GPS (check-in requires location access)

<<<<<<< HEAD
=======
---

## Next Steps

- [Quick Start Guide](../1-Getting%20Started/3.%20quick-start-guide.md) - Set up your account and complete your first check-in.
- [Mobile App Guide](../2-userGuides/7.%20mobile-app-guide.md) - Step-by-step mobile installation and permission setup.
>>>>>>> f2070ddc19a4eecb6e21696ab94c0633cecbd09b
