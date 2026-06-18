# Test Strategy

## 1. Five Most Critical Flows

### Priority 1: Attendance and Overtime to Payroll

This is the most critical flow because attendance and overtime directly determine how much a worker gets paid. If this breaks, workers may lose wages they have already earned.

**Who gets hurt:** Construction workers and payroll operators.

---

### Priority 2: Salary Configuration to Payslip

Changes in salary should correctly appear in future payslips. Incorrect calculations can lead to underpayment or overpayment.

**Who gets hurt:** Workers, HR, and finance teams.

---

### Priority 3: Employee Onboarding

A new employee should be created successfully and become available for attendance and payroll processing.

**Who gets hurt:** New workers and HR.

---

### Priority 4: Employee Exit

When an employee leaves, payroll should stop while historical records remain available.

**Who gets hurt:** HR and finance.

---

### Priority 5: Employee Profile Updates

Changes to employee information such as salary or designation should persist and update dependent modules.

**Who gets hurt:** HR and payroll teams.

## 2. Worst Consequence for Each Critical Flow

### Attendance and Overtime to Payroll

**Worst case:** A worker's attendance or overtime is not recorded correctly.

**Who gets hurt:** The construction worker.

**Consequence:** They receive less salary than they earned and may struggle to meet monthly expenses.

---

### Salary Configuration to Payslip

**Worst case:** Salary updates do not appear in the next payroll cycle.

**Who gets hurt:** Workers and payroll operators.

**Consequence:** Incorrect salaries are paid, requiring manual corrections and reducing trust in the system.

---

### Employee Onboarding

**Worst case:** A newly hired worker is not properly registered.

**Who gets hurt:** The new worker and HR team.

**Consequence:** Attendance and payroll cannot be processed correctly.

---

### Employee Exit

**Worst case:** An exited employee remains active in payroll or important records are lost.

**Who gets hurt:** HR and finance teams.

**Consequence:** Incorrect payments and inaccurate business records.

---

### Employee Profile Updates

**Worst case:** Changes to employee details do not propagate to dependent systems.

**Who gets hurt:** HR, payroll operators, and employees.

**Consequence:** Future payroll calculations become inaccurate and require manual intervention.

## 3. What I Will Automate vs. Test Manually

The goal is to protect the most critical business processes without creating a slow development workflow.

### Automated Testing

I would automate:

* Employee onboarding.
* Attendance and overtime submission.
* Salary updates and payslip generation.
* Employee exit process.
* Critical API endpoints.
* Smoke tests for application startup and core functionality.

These features directly affect worker payments and are frequently used. Automating them reduces the risk of production issues and gives developers confidence when making changes.

### Manual Testing

I would perform manual testing for:

* User interface appearance.
* Mobile responsiveness.
* Rare administrative workflows.
* Exploratory testing for newly added features.
* Complex scenarios requiring human judgment.

Manual testing is useful for finding unexpected issues that automated tests may not cover.

### Keeping CI Fast

The development team is concerned about long test execution times. To address this:

* Run fast smoke and API tests on every pull request.
* Run core business flow tests before merging.
* Schedule longer regression suites to run periodically.
* Keep automated tests independent and avoid unnecessary duplication.

This approach provides protection for critical payroll and attendance flows while maintaining a development process that remains efficient for both experienced and new developers.


## 4. What I Will Deliberately NOT Test and Why

A good test strategy is about making choices. Trying to automate everything would make the test suite slow, expensive to maintain, and less useful for the team.

### I will not automate:

#### Cosmetic UI changes

Small visual differences such as spacing, colors, or font changes will not be a priority unless they affect usability.

**Reason:** They do not directly impact worker payments or critical business operations.

---

#### Rare administrative features

Features that are used infrequently and have low business impact will initially be tested manually.

**Reason:** Automation effort is better spent on high-risk payroll and attendance flows.

---

#### Every possible browser and device combination

I would verify that the application works on common platforms but would not attempt exhaustive compatibility testing in the early stages.

**Reason:** The team has limited resources, and protecting core functionality provides greater value.

---

#### Unlikely edge cases with very low business impact

Some unusual scenarios can be covered through exploratory testing instead of permanent automation.

**Reason:** Maintaining tests for extremely rare situations may create unnecessary overhead.

---

## Why These Decisions Matter

The primary responsibility of this HRMS is to ensure that workers are paid accurately and on time. Every testing decision should support that goal. By focusing automation on critical business flows and using manual testing where appropriate, the team can maintain fast development cycles while reducing the risk of production failures that affect workers and payroll operations.



