# Employee Leave Request — Functional Requirements

## Overview
This document defines the functional requirements for the employee leave request module. It outlines the core submission flow, automated validations, approval workflows, and notification systems required to process employee time-off requests efficiently.

## Core Functional Requirements

### 1. Submission & Data Entry
* **FR1 (Leave Type):** The system shall allow an employee to select a leave type from a predefined list (e.g., Annual, Sick, Unpaid, Casualty, Parental, Bereavement).
* **FR2 (Date & Duration Selection):** 
  * The system shall allow an employee to select a start date and an end date.
  * The system shall support **half-day leave options** (e.g., First Half / Second Half) for single-day or partial-day requests.
* **FR3 (Reason & Supporting Documents):** 
  * The system shall allow the employee to enter a text reason for the leave.
  * The system shall allow employees to **attach supporting documents** (e.g., medical certificates, official notices) in PDF, PNG, or JPEG formats up to 5 MB.
  * *Constraint:* Supporting documents shall be mandatory for specific leave types (e.g., Sick leave exceeding 2 consecutive days).

### 2. Automated Calculations & Validations
* **FR4 (Leave Day Calculation):** The system shall automatically calculate and display the net working days requested, excluding weekends and official company holiday calendars.
* **FR5 (Balance Check):** The system shall display the employee’s available leave balance in real-time and block submission if the requested days exceed the accrued balance (unless "Unpaid Leave" is selected).
* **FR6 (Overlap Prevention):** The system shall validate that the selected date range does not overlap with an existing pending or approved leave request for the same employee.

### 3. Workflow & Approvals
* **FR7 (Routing & Hierarchy):** Upon submission, the system shall route the request to the employee's assigned direct manager for review. If the direct manager is unavailable or on leave, the request shall automatically escalate after 48 hours to the secondary approver or HR administrator.
* **FR8 (Manager Actions):** The system shall provide the manager with an interface to **Approve**, **Reject** (with a mandatory reason), or **Request Modification**.

### 4. Notifications & History
* **FR9 (Notifications):** 
  * The system shall send an immediate email and in-app notification to the manager upon request submission.
  * The system shall send a confirmation notification to the employee upon submission and an update notification once the manager acts on the request.
* **FR10 (Leave History & Cancellation):** The system shall allow employees to view their leave request history and cancel upcoming approved requests prior to the start date, automatically restoring their leave balance.

## Acceptance Criteria

- [ ] Employee can select leave type, start/end dates, and half-day options.
- [ ] Employee can upload supporting attachments when required.
- [ ] System automatically calculates net business days excluding holidays/weekends.
- [ ] System displays real-time remaining leave balances during request entry.
- [ ] System prevents duplicate/overlapping date submissions.
- [ ] System routes requests to the correct direct manager with automatic escalation rules.
- [ ] Manager can Approve, Reject (with reason), or request changes.
- [ ] Automated email/in-app notifications are sent at each stage of the approval pipeline.
- [ ] Employees can cancel upcoming booked leaves and receive restored balances.

## Dependencies & Integrations

* **User Management:** Employee and line-manager reporting structures must exist in the system.
* **Holiday Calendar:** Company holiday and weekend schedules must be configured for accurate day calculations.
* **Notifications:** Email gateway / push notification service integration.

## Resolved Questions & Edge Cases

* **Half-Day Requests:** Supported via a toggle/dropdown when the start and end dates match.
* **Document Uploads:** Supported and enforced dynamically based on the leave policy rule set.
* **Retroactive Requests:** Sick leave can be submitted up to 3 business days retroactively.