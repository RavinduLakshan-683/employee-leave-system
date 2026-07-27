# Employee Leave Request — Functional Requirements

## Overview
This document defines the functional requirements for the employee leave
request feature, based on the user story and acceptance criteria in
Issue #ISSUE_NUMBER.

## Functional Requirements

FR1. The system shall allow an employee to select a leave type
     (e.g. annual, sick, unpaid).

FR2. The system shall allow an employee to enter a start date and an
     end date for the leave request.

FR3. The system shall allow an employee to enter a reason for the leave.

FR4. The system shall calculate and display the number of leave days
     requested, based on the selected start and end dates.

FR5. The system shall route the leave request to the employee's
     assigned manager.

FR6. The system shall send a confirmation to the employee once the
     request has been submitted successfully.

## Acceptance Criteria

- [ ] The employee can select a leave type.
- [ ] The employee can enter a start date and end date.
- [ ] The employee can provide a reason.
- [ ] The system shows the number of leave days requested.
- [ ] The request is sent to the correct manager.
- [ ] The employee receives confirmation after submission.

## Dependencies

- Employee and manager records must already exist in the system.

## Priority

High

## Open Questions

- Can employees submit half-day leave requests?
- Can employees attach supporting documents?