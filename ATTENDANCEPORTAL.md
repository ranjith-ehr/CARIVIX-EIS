# CARIVIX EIS: Project Report

## 1. Executive Summary

### 1.1 Project Overview
CARIVIX EIS (Employee Information System) is a high-end, modern administrative portal designed for enterprise-grade employee management. It streamlines core HR processes into a visually stunning industrial interface, including attendance tracking, task management, leave requests and performance analytics.

### 1.2 Current Scope & Limitations
This report documents the **Basic Version** of the CARIVIX EIS project. Currently, the project scope encompasses the completed frontend architecture and UI/UX design implementation. The system is operating in a non-live state and is not yet connected to the live backend services. As such, data rendering and workflows are driven by local state management to simulate the final user experience.

---

## 2. Technical Architecture

### 2.1 Implemented Frontend Stack
The frontend has been built focusing on high performance and a robust developer experience:
* **Framework:** React 18+ utilizing Vite for fast development and bundling.
* **Language:** TypeScript is used throughout the application to ensure robust type safety.
* **Styling:** Tailwind CSS drives the custom design system, focusing on a "Corporate/Industrial" aesthetic characterized by glassmorphism and sharp edges.
* **Icons:** Lucide React provides a consistent, modern icon set across the platform.

### 2.2 State & Data Management (Client-Side)
To handle application state and simulate database interactions in this disconnected version, the application leverages the React Context API:
* **AuthContext:** Manages simulated user sessions, authentication states and role-based access.
* **DataContext:** Acts as the core engine handling CRUD operations, business logic and UI data synchronization.
* **NotificationContext:** Manages real-time alerts and user feedback across the system.

### 2.3 Planned Backend Services
While not yet integrated, the system architecture is designed to interface with the following backend services in the next development phase:
* **Firebase:** Will handle Authentication and Cloud Storage.
* **GCP Data Connect:** Will provide a typed, SQL-based interface via Cloud SQL for managing complex data relationships.
* **Supabase:** Integrated to leverage additional database capabilities.

---

## 3. User Personas & Interface Views

### 3.1 Admin Portal
The Admin Portal UI is designed to give management full visibility into the organization's health and personnel operations:
* **Employee Lifecycle:** Interfaces to create, update and manage comprehensive employee profiles.
* **Attendance Oversight:** Dashboards to monitor real-time check-ins, historical logs and GPS-based employee locations.
* **Leave Approval:** A dedicated view to review leave applications and trigger instant decisions.
* **Task Assignment & Reporting:** Modules to assign specific duties, monitor completion status and export organization metrics.

### 3.2 Employee Portal
The Employee Portal UI prioritizes self-service and daily task execution:
* **Daily Attendance:** Simple check-in/out interfaces with built-in location validation and "Late" status detection logic.
* **Identity Security:** Setup modules for Face ID (Biometric) secure authentication.
* **Task & Leave Management:** Interfaces to view assigned duties, submit completed tasks and apply for time off.
* **Career Progress:** Dashboards displaying performance metrics, daily streaks and manager feedback.

---

## 4. Key Processes & Workflows (Frontend Logic)

### 4.1 Attendance Tracking
1.  **Trigger:** Employees utilize the "Check In" and "Check Out" buttons on their dashboard.
2.  **Validation:** The frontend captures GPS coordinates and compares the current time against the application's configuration (`appConfig`).
3.  **Visibility:** The simulated record is pushed to the `DataContext` and rendered in the Admin's "Attendance Management" tab.

### 4.2 Leave Management Lifecycle
1.  **Request:** Employees fill out a form specifying the Date Range, Type and Reason for leave.
2.  **Notification:** The `DataContext` triggers a persistent notification targeting the Admin persona.
3.  **Review:** Admins navigate to the "Leave" tab to approve or reject the request.
4.  **Closing:** The Employee dashboard receives a real-time notification containing the decision.

### 4.3 Task Assignment & Completion
1.  **Assignment:** Admins generate a new task via the "Employee Management" dashboard.
2.  **Sync:** The task renders dynamically on the assigned employee's dashboard.
3.  **Action:** Upon completion, the employee triggers the "Submit Task" action.
4.  **Validation:** The system logs a `submittedAt` timestamp and fires a completion notification back to the Admin.

---

## 5. Specialized UI Modules

### 5.1 Intelligent Global Search
A centralized search bar uses keyword mapping to intelligently route users across the app:
* **Navigation Routing:** Searching terms like "Vacation" or "Holiday" redirects the user directly to the Leave management tab.
* **Data Filtering:** Searching for specific names instantly filters the global Employee Table.

### 5.2 Real-time Notifications
A robust, cross-role notification UI guarantees high visibility for critical actions:
* **Styling:** Utilizes type-based color coding: Success (green), Warning (amber) and Info (blue).
* **Storage:** Notifications persist in a "Notification Drawer" allowing users to review missed alerts.

---

## 6. Project Directory & Next Steps

### 6.1 Current Directory Structure
The foundational codebase is organized to support scalable development:
* `/src/components`: UI components organized by role (admin, employee) alongside shared utilities.
* `/src/context`: Centralized global logic and application state.
* `/src/dataconnect-generated`: Auto-generated SDK files designated for future GCP database interaction.
* `/src/api`: Modular API definitions for chat, biometrics and attendance integrations.

### 6.2 Development Roadmap
To transition this project from the Basic Version to a live deployment, the following workflow is required:
1.  **Schema Update:** Modify GCP Data Connect schemas to align with frontend data requirements.
2.  **Component Refinement:** Continue expanding modular UI components referencing the established design system.
3.  **Context Integration:** Bind the currently simulated UI actions to live `DataContext` methods connected to the backend APIs.
4.  **End-to-End Testing:** Validate live data flows utilizing ErrorBoundary components and console logging.