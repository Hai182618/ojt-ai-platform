# User Stories and Acceptance Criteria

## US-STU-001 — View My OJT Status

**As a** student  
**I want** to view my current OJT status  
**So that** I know what I need to do next.

### Acceptance Criteria

**AC-01**
Given I am an authenticated student  
When I open my dashboard  
Then I can see my current OJT status.

**AC-02**
Given I have upcoming milestones  
When I open my dashboard  
Then I can see their due dates and completion status.

---

## US-STU-002 — Submit OJT Plan

**As a** student  
**I want** to submit my OJT plan  
**So that** it can be reviewed by the university.

### Acceptance Criteria

**AC-01**
Given all mandatory fields are valid  
When I submit my OJT plan  
Then the status changes to Submitted.

**AC-02**
Given a mandatory field is missing  
When I submit my OJT plan  
Then submission is blocked and the missing field is identified.

**AC-03**
Given the plan has been submitted  
When I reopen it  
Then I can see its submission status.

---

## US-LEC-001 — View Assigned Students

**As a** lecturer  
**I want** to view students assigned to me  
**So that** I can monitor their OJT progress.

### Acceptance Criteria

**AC-01**
Given I am an authenticated lecturer  
When I open my dashboard  
Then I see students assigned to me.

**AC-02**
Given a student is not assigned to me and I have no additional permission  
When I attempt to access restricted details  
Then access is denied.

---

## US-LEC-002 — Prioritize High-Risk Students

**As a** lecturer  
**I want** to identify high-risk students  
**So that** I can prioritize intervention.

### Acceptance Criteria

**AC-01**
Given assigned students have risk assessments  
When I filter by High risk  
Then only authorized high-risk students are displayed.

**AC-02**
Given I open a high-risk student  
When risk explanation is available  
Then I can see the current risk level and relevant contributing factors.

**AC-03**
The UI must not describe the prediction as a guaranteed outcome.

---

## US-LEC-003 — Create Intervention

**As a** lecturer  
**I want** to record an intervention  
**So that** support actions are traceable.

### Acceptance Criteria

**AC-01**
Given I am authorized to manage the student  
When I create an intervention with required fields  
Then the intervention is stored successfully.

**AC-02**
Given owner is missing  
When I attempt to create the intervention  
Then creation is blocked.

**AC-03**
Given an intervention is created  
Then creator and creation time are recorded.

---

## US-COORD-001 — Monitor Program Status

**As an** OJT Coordinator  
**I want** a program-level dashboard  
**So that** I can monitor OJT operations efficiently.

### Acceptance Criteria

**AC-01**
When I open the coordinator dashboard  
Then I can see student counts by relevant OJT status.

**AC-02**
When risk data exists  
Then I can see risk distribution.

**AC-03**
When overdue milestones exist  
Then I can identify affected students.

---

## US-COORD-002 — Review Student Risk

**As an** OJT Coordinator  
**I want** to review current and historical risk assessments  
**So that** I can understand whether risk is changing.

### Acceptance Criteria

**AC-01**
Given multiple predictions exist  
When I open risk history  
Then predictions are shown with timestamps.

**AC-02**
Each prediction displays or retains its model version.

**AC-03**
A new prediction does not overwrite prior predictions.

---

## US-ADM-001 — Disable User Account

**As an** administrator  
**I want** to disable an account  
**So that** an unauthorized or inactive user cannot sign in.

### Acceptance Criteria

**AC-01**
Given an active account exists  
When I disable the account  
Then future authentication attempts for that account are rejected.

**AC-02**
The account status change is auditable.

---

## US-AI-001 — Generate Risk Prediction

**As an** authorized staff user  
**I want** the system to estimate OJT delay risk  
**So that** I can identify students who may require attention.

### Acceptance Criteria

**AC-01**
Given all required prediction inputs are available  
When prediction is triggered  
Then the system stores a risk score, risk level, model version, and timestamp.

**AC-02**
Given required inputs are missing  
When prediction is triggered  
Then the system does not fabricate a risk score.

**AC-03**
Given the prediction succeeds  
Then authorized users can view an explanation where available.

**AC-04**
The system does not automatically approve, reject, penalize, or grade a student based only on the AI prediction.
