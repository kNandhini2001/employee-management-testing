# Test Plan

## Objective and scope
Validate a fictional HR application against the requirements below. Exclude payroll, integrations, load testing and production security assessment.

## Assumed requirements
- R01: Active users authenticate with valid credentials; required fields, masked passwords, logout, protected routes and role-based access are enforced.
- R02: HR can create employees with unique mandatory IDs, names of 1–50 characters, department and valid email; cancel discards changes.
- R03: Directory supports exact ID, case-insensitive partial name, department and combined filters; empty or cleared filters show all records.
- R04: HR can update profiles; phone must contain 10 digits, email must be valid, name is mandatory and ID immutable. Employees cannot change department. Saved changes persist; cancel discards changes.
- R05: Employees request future working days within available balance; dates are mandatory and ordered, overlapping pending requests are rejected. HR approval deducts balance; rejection leaves it unchanged.

## Strategy
Functional positive and negative tests, boundary values for name length and leave balance. Smoke suite: first case of each module. Sanity suite after profile fixes: TC-031, TC-034, TC-039. Regression: all 50 cases. Reset fixtures before each independent test. Use synthetic accounts and data only.

## Entry and exit criteria
Entry: agreed requirements, available test build, test accounts and fixtures. Exit: all planned cases executed, critical defects resolved and retested, remaining risks accepted. These criteria are proposed, not achieved.

## Defect management
New → Assigned → In Progress → Fixed → Retest → Closed or Reopened. Record severity, priority, steps, expected and actual results, evidence and build.

## Risks
Unavailable test environment, changing requirements, incorrect role permissions and leave calculations. Current status: design only; no execution.
