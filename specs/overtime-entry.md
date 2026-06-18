# Overtime Entry Screen - Acceptance Criteria

## Objective

Allow site managers to record overtime worked by construction workers accurately and reliably from both desktop and mobile devices.

---

## Required Fields

* Worker
* Overtime Date
* Overtime Hours
* Reason
* Supervisor

All required fields must be completed before submission.

---

## Acceptance Criteria

### AC1

Given a valid worker exists,
When a site manager enters valid overtime details,
Then the record should be saved successfully.

### AC2

Overtime hours cannot be negative.

### AC3

Overtime hours cannot exceed the maximum allowed daily limit.

### AC4

The overtime date cannot be in the future.

### AC5

A reason is mandatory.

### AC6

The worker must exist and be active.

### AC7

Duplicate overtime entries for the same worker and date should trigger a warning.

### AC8

The system should confirm successful submission.

### AC9

The form should work on mobile devices.

### AC10

Temporary network failures should not silently lose data.

---

# Edge Cases

* Empty fields.
* Invalid worker.
* Negative hours.
* Zero hours.
* Extremely large values.
* Duplicate entries.
* Future dates.
* Network interruption.
* Session timeout.
* Double-click submit.

---

# Questions Before Development

1. Maximum overtime allowed per day?
2. Monthly overtime cap?
3. Should duplicate entries be blocked or merged?
4. Can overtime be edited?
5. Who can approve overtime?
6. Can past entries be modified?
7. What happens if offline submission fails?

---

# Test Scenarios

## Given

A valid worker exists.

## When

A supervisor submits 3 overtime hours.

## Then

The entry is stored successfully.

---

## Given

A duplicate overtime exists.

## When

Another submission is attempted.

## Then

The system warns the user.

---

## Given

Network interruption occurs.

## When

Submission fails.

## Then

The user receives a clear error and can retry.

---

# Launch Blockers

* Data loss.
* Incorrect calculations.
* Duplicate payments.
* Missing validation.
* Mobile submission failure.

# Version 2

* Offline mode.
* Bulk upload.
* GPS tagging.
* File attachments.
* Approval workflow.
