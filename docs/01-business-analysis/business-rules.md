# Business Rules

## 1. Purpose

This document defines high-level business rules for the OJT management domain. Rules will be refined during detailed requirement analysis.

---

## 2. Student and OJT Rules

### BR-001
A student must have a valid system account before accessing protected OJT functions.

### BR-002
A student can only edit their own editable OJT information unless an authorized staff member performs the action.

### BR-003
A student must satisfy configured OJT eligibility requirements before an OJT plan can reach final approval.

### BR-004
An OJT plan must contain all mandatory information before submission.

### BR-005
Only authorized lecturers or coordinators can approve or reject an OJT plan.

### BR-006
A submitted OJT plan must retain its review history.

### BR-007
OJT milestones must belong to a valid OJT period or student OJT plan.

### BR-008
A milestone is overdue when its due date has passed and it is not marked completed.

### BR-009
Progress updates must record creation time and actor.

---

## 3. Risk Rules

### BR-010
Risk prediction must only use data available at the time the prediction is generated.

### BR-011
Each risk prediction must store the prediction time.

### BR-012
Each risk prediction must be associated with the student being assessed.

### BR-013
Risk classification thresholds must be configurable or centrally defined.

### BR-014
Authorized users must be able to view a human-readable explanation of the main risk factors.

### BR-015
AI risk output must not automatically make final academic decisions.

### BR-016
A new prediction must not silently overwrite historical predictions.

### BR-017
If required prediction inputs are missing, the system must clearly indicate that risk assessment is unavailable or incomplete.

---

## 4. Intervention Rules

### BR-018
Only authorized staff can create official intervention records.

### BR-019
Each intervention must be associated with a student.

### BR-020
An intervention must have an owner.

### BR-021
An intervention must have a status.

### BR-022
Changes to intervention status should be traceable.

### BR-023
An intervention may reference the risk prediction that triggered or supported it.

### BR-024
Closing an intervention should allow an outcome or resolution note to be recorded.

---

## 5. Access Control Rules

### BR-025
Students must not access private records of other students.

### BR-026
Lecturers can access students assigned to them according to authorization rules.

### BR-027
OJT Coordinators can access operational OJT information required to manage the program.

### BR-028
Administrators can manage system-level accounts and configuration according to granted permissions.

### BR-029
Management reporting should expose aggregated information unless individual-level access is explicitly authorized.

---

## 6. Audit Rules

### BR-030
Critical workflow actions must record actor and timestamp.

### BR-031
Approval, rejection, risk prediction, and intervention events must be traceable.

### BR-032
Audit records must not be editable by normal end users.
