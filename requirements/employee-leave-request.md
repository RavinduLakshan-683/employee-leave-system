# Employee Leave Request — Functional Requirements

## Overview

This document defines the functional requirements for the employee leave request feature, based on the user story:
"As an employee, I want to submit a leave request so that I can obtain approval from my manager."

## Functional Requirements

### FR-001
The system shall allow an employee to select a leave type from a predefined list (e.g. annual, sick, unpaid).

### FR-002
The system shall allow an employee to enter a start date and an end date for the leave request.

### FR-003
The system shall allow an employee to provide a reason for the leave request.

### FR-004
The system shall automatically calculate and display the number of leave days requested, based on the selected start and end dates.

### FR-005
The system shall route the leave request to the employee's assigned manager.

### FR-006
The system shall display a confirmation message to the employee after the request has been successfully submitted.

## Acceptance Criteria

- The employee can select a leave type.
- The employee can enter a start date and end date.
- The employee can provide a reason.
- The system shows the number of leave days requested.
- The request is sent to the correct manager.
- The employee receives confirmation after submission.

## Dependencies

- Employee and manager records must already exist in the system.

## Open Questions

- Can employees submit half-day leave requests?
- Can employees attach supporting documents?