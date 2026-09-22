# Functional Requirements

## 1. Purpose

This document defines the initial functional requirements for the AI-Powered OJT Management & Risk Prediction System.

Requirement IDs are designed to remain stable so they can later be traced to:
- use cases;
- user stories;
- API endpoints;
- UI screens;
- source-code modules;
- test cases;
- UAT scenarios.

---

# 2. Authentication and Access Control

## FR-AUTH-001 — User Login
The system shall allow an active user to authenticate using valid credentials.

## FR-AUTH-002 — Invalid Login Handling
The system shall reject invalid login attempts and return a non-sensitive error message.

## FR-AUTH-003 — Role-Based Access
The system shall restrict protected functions according to the authenticated user's assigned role and permissions.

## FR-AUTH-004 — Logout
The system shall allow an authenticated user to terminate the current session.

## FR-AUTH-005 — Current User Context
The system shall provide the authenticated user's identity and role to authorized frontend functions.

## FR-AUTH-006 — Disabled Account
The system shall prevent a disabled account from authenticating.

---

# 3. Student Profile and Academic Data

## FR-STU-001 — View Student Profile
The system shall allow authorized users to view a student's OJT-relevant profile.

## FR-STU-002 — Update Own Profile
The system shall allow a student to update permitted fields of their own profile.

## FR-STU-003 — Academic Information
The system shall store academic information required for OJT eligibility and risk assessment.

## FR-STU-004 — OJT Eligibility Status
The system shall determine or display the student's current OJT eligibility status based on configured business rules.

## FR-STU-005 — Lecturer Assignment
The system shall allow authorized staff to assign a lecturer/advisor to a student.

## FR-STU-006 — Student Search
The system shall allow authorized staff to search students by supported criteria.

## FR-STU-007 — Student Filtering
The system shall allow authorized staff to filter students by OJT status, risk level, lecturer, cohort, or other supported operational attributes.

---

# 4. OJT Plan Management

## FR-OJT-001 — Create OJT Plan
The system shall allow an eligible student to create an OJT plan.

## FR-OJT-002 — Edit Draft OJT Plan
The system shall allow a student to edit an OJT plan while it is in an editable state.

## FR-OJT-003 — Submit OJT Plan
The system shall allow a student to submit a complete OJT plan for review.

## FR-OJT-004 — Validate Required Fields
The system shall validate required OJT plan fields before submission.

## FR-OJT-005 — Review OJT Plan
The system shall allow an authorized lecturer or coordinator to review a submitted OJT plan.

## FR-OJT-006 — Approve OJT Plan
The system shall allow an authorized user to approve a submitted OJT plan.

## FR-OJT-007 — Reject OJT Plan
The system shall allow an authorized user to reject a submitted OJT plan and record a reason.

## FR-OJT-008 — OJT Plan Status History
The system shall retain a traceable history of significant OJT plan status changes.

## FR-OJT-009 — Company Information
The system shall store the company information associated with an OJT plan.

## FR-OJT-010 — OJT Period
The system shall store expected OJT start and end dates.

---

# 5. Progress and Milestone Management

## FR-PROG-001 — View OJT Progress
The system shall allow authorized users to view a student's OJT progress.

## FR-PROG-002 — Create Milestone
The system shall allow authorized users to define OJT milestones.

## FR-PROG-003 — Update Milestone
The system shall allow authorized users to update permitted milestone information.

## FR-PROG-004 — Mark Milestone Complete
The system shall allow an authorized actor to mark a milestone as completed.

## FR-PROG-005 — Identify Overdue Milestone
The system shall identify a milestone as overdue when its due date has passed and it is not complete.

## FR-PROG-006 — Progress Update
The system shall allow a student or authorized staff member to record a progress update.

## FR-PROG-007 — Progress History
The system shall preserve historical progress updates.

## FR-PROG-008 — Deadline Visibility
The system shall display relevant OJT deadlines and milestone due dates.

---

# 6. Risk Prediction

## FR-RISK-001 — Generate Risk Prediction
The system shall allow an authorized process to generate an OJT delay risk prediction for an eligible student.

## FR-RISK-002 — Risk Score
The system shall store the numeric risk score returned by the prediction service.

## FR-RISK-003 — Risk Level
The system shall map the risk score to a configured risk level.

## FR-RISK-004 — Prediction Timestamp
The system shall store the date and time at which each prediction is generated.

## FR-RISK-005 — Prediction History
The system shall preserve historical risk predictions.

## FR-RISK-006 — Missing Input Handling
The system shall identify when required prediction inputs are unavailable.

## FR-RISK-007 — Prediction Trigger
The system shall support prediction generation through a defined trigger such as manual request, scheduled process, or significant data update.

## FR-RISK-008 — Risk Factor Explanation
The system shall provide authorized users with understandable information about relevant factors contributing to a prediction.

## FR-RISK-009 — Model Version
The system shall record the model version associated with each stored prediction.

---

# 7. Recommendation

## FR-REC-001 — Generate Recommendation
The system shall provide recommended intervention actions when sufficient risk context is available.

## FR-REC-002 — Recommendation Context
The system shall associate recommendations with relevant risk factors or student conditions.

## FR-REC-003 — Recommendation Visibility
The system shall display recommendations only to roles authorized to view them.

## FR-REC-004 — Human Decision
The system shall allow authorized staff to decide whether to use, modify, or ignore a recommendation.

---

# 8. Intervention Management

## FR-INT-001 — Create Intervention
The system shall allow authorized staff to create an intervention for a student.

## FR-INT-002 — Intervention Owner
The system shall require an intervention to have an assigned owner.

## FR-INT-003 — Intervention Status
The system shall maintain an intervention status.

## FR-INT-004 — Intervention Notes
The system shall allow authorized users to add notes to an intervention.

## FR-INT-005 — Link Risk Prediction
The system shall allow an intervention to reference a related risk prediction.

## FR-INT-006 — Update Intervention
The system shall allow authorized users to update an intervention.

## FR-INT-007 — Close Intervention
The system shall allow an authorized user to close an intervention and record an outcome.

## FR-INT-008 — Intervention History
The system shall preserve intervention status and activity history.

---

# 9. Dashboard and Monitoring

## FR-DASH-001 — Student Dashboard
The system shall provide a dashboard showing information relevant to the logged-in student.

## FR-DASH-002 — Lecturer Dashboard
The system shall provide a dashboard showing assigned students, progress, and risk information relevant to the lecturer.

## FR-DASH-003 — Coordinator Dashboard
The system shall provide a dashboard showing program-level OJT status and risk information.

## FR-DASH-004 — Administrator Dashboard
The system shall provide an administration view for supported system-management tasks.

## FR-DASH-005 — High-Risk Student List
The system shall provide authorized staff with a view of students currently classified as high risk.

## FR-DASH-006 — Dashboard Filtering
The system shall allow supported dashboard data to be filtered using relevant operational criteria.

---

# 10. Reporting

## FR-REP-001 — OJT Status Summary
The system shall provide a summary of students by OJT status.

## FR-REP-002 — Risk Distribution
The system shall provide a summary of students by risk level.

## FR-REP-003 — Milestone Summary
The system shall provide milestone completion and overdue information.

## FR-REP-004 — Intervention Summary
The system shall provide summary information about intervention status and outcomes.

## FR-REP-005 — Export
The system shall support export of selected report data in at least one common format in a later MVP iteration.

---

# 11. Administration

## FR-ADM-001 — User Management
The system shall allow authorized administrators to view and manage user accounts.

## FR-ADM-002 — Role Management
The system shall support assignment of supported system roles.

## FR-ADM-003 — Account Status
The system shall allow authorized administrators to enable or disable accounts.

## FR-ADM-004 — Reference Data
The system shall allow authorized users to manage supported reference data.

## FR-ADM-005 — Risk Threshold Configuration
The system shall support centrally defined risk thresholds.

---

# 12. Auditability

## FR-AUD-001 — Audit Critical Actions
The system shall record critical workflow actions.

## FR-AUD-002 — Audit Actor
An audit record shall identify the actor where applicable.

## FR-AUD-003 — Audit Timestamp
An audit record shall contain a timestamp.

## FR-AUD-004 — Audit Protection
Normal users shall not be able to edit audit records.

---

# 13. Requirement Status

All requirements in this document are initially marked **Draft** until validated through later analysis and implementation.

No requirement should be interpreted as final regulatory or university policy without stakeholder validation.
