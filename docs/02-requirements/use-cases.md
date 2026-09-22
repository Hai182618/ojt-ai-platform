# Use Cases

## UC-01 — Login

**Primary Actor:** User

**Preconditions**
- User account exists.
- User account is active.

**Main Flow**
1. User opens the login page.
2. User enters credentials.
3. System validates credentials.
4. System identifies the user's role.
5. System creates an authenticated session/token.
6. System redirects the user to the appropriate application area.

**Alternative Flow**
- Invalid credentials → authentication is rejected.
- Disabled account → access is denied.

**Postconditions**
- Authenticated user context is established.

---

## UC-02 — Submit OJT Plan

**Primary Actor:** Student

**Preconditions**
- Student is authenticated.
- Student is permitted to create or edit an OJT plan.

**Main Flow**
1. Student opens OJT Plan.
2. Student enters company and OJT information.
3. Student saves the plan.
4. Student selects Submit.
5. System validates required fields.
6. System records submission time.
7. System changes plan status to Submitted.
8. Lecturer/coordinator can view the submitted plan.

**Alternative Flow**
- Required information missing → system blocks submission and displays validation errors.
- Student not eligible → system blocks final submission according to business rules.

**Postconditions**
- Submitted plan is ready for review.

---

## UC-03 — Review OJT Plan

**Primary Actor:** Lecturer / OJT Coordinator

**Preconditions**
- Reviewer is authenticated.
- OJT plan status is Submitted.
- Reviewer has permission.

**Main Flow**
1. Reviewer opens submitted plan.
2. Reviewer checks plan information.
3. Reviewer selects Approve or Reject.
4. If rejected, reviewer records a reason.
5. System records actor and timestamp.
6. System updates the plan status.
7. Student can view the result.

**Postconditions**
- Plan becomes Approved or Rejected.
- Review history is preserved.

---

## UC-04 — Update OJT Progress

**Primary Actor:** Student

**Supporting Actor:** Lecturer

**Preconditions**
- Student has an active OJT record.

**Main Flow**
1. Student opens progress section.
2. Student records progress information.
3. Student updates supported milestone information.
4. System validates the update.
5. System stores the update with timestamp.
6. Authorized staff can view the updated status.

**Postconditions**
- Current progress state is updated.
- Historical update remains traceable.

---

## UC-05 — Generate Risk Assessment

**Primary Actor:** System / Authorized Staff

**Preconditions**
- Student exists.
- Required prediction inputs are available.
- A deployable AI model is available.

**Main Flow**
1. System gathers current eligible student features.
2. System sends features to the prediction component.
3. Prediction component returns risk score.
4. System maps score to risk level.
5. System generates or retrieves explanatory factors.
6. System stores prediction, model version, and timestamp.
7. Authorized users can view the result.

**Alternative Flow**
- Required inputs missing → prediction is not generated; missing information is reported.
- Prediction service unavailable → error is recorded and no false prediction is displayed.

**Postconditions**
- New historical risk assessment exists.

---

## UC-06 — Review High-Risk Students

**Primary Actor:** Lecturer / OJT Coordinator

**Preconditions**
- User is authenticated and authorized.

**Main Flow**
1. User opens risk-monitoring dashboard.
2. System shows students and current risk levels.
3. User filters or sorts the list.
4. User selects a student.
5. System displays progress, current risk, risk factors, and relevant history.
6. User decides whether intervention is required.

**Postconditions**
- User has enough contextual information to make an intervention decision.

---

## UC-07 — Create Intervention

**Primary Actor:** Lecturer / OJT Coordinator

**Preconditions**
- User is authorized.
- Student exists.

**Main Flow**
1. User opens student detail.
2. User selects Create Intervention.
3. User records intervention type/action.
4. User assigns an owner.
5. User optionally links the intervention to a risk prediction.
6. System creates the intervention.
7. System records timestamp and creator.
8. Intervention becomes trackable.

**Postconditions**
- Active intervention exists for the student.

---

## UC-08 — Close Intervention

**Primary Actor:** Lecturer / OJT Coordinator

**Preconditions**
- Intervention exists.
- User is authorized to update it.

**Main Flow**
1. User opens intervention.
2. User reviews current status.
3. User records outcome/resolution.
4. User closes intervention.
5. System records actor and timestamp.

**Postconditions**
- Intervention is marked Closed.
- Outcome remains available historically.

---

## UC-09 — Monitor OJT Program

**Primary Actor:** OJT Coordinator

**Preconditions**
- Coordinator is authenticated.

**Main Flow**
1. Coordinator opens dashboard.
2. System displays OJT status summary.
3. System displays risk distribution.
4. System displays overdue milestones.
5. System displays open interventions.
6. Coordinator filters by supported criteria.
7. Coordinator opens relevant student or cohort details.

**Postconditions**
- Coordinator obtains operational visibility across the OJT program.

---

## UC-10 — Manage User Account

**Primary Actor:** Administrator

**Preconditions**
- Administrator is authenticated and authorized.

**Main Flow**
1. Administrator opens user management.
2. Administrator searches/selects a user.
3. Administrator updates permitted account attributes.
4. Administrator assigns supported role or status.
5. System validates changes.
6. System saves the update.
7. Critical changes are audited.

**Postconditions**
- User account reflects the approved configuration.
