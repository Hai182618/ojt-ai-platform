# Stakeholder Analysis

## 1. Purpose

This document identifies the main stakeholders of the AI-Powered OJT Management & Risk Prediction System and describes their responsibilities, needs, concerns, and expected system interactions.

---

## 2. Stakeholder Summary

| Stakeholder | Type | Primary Interest | Influence |
|---|---|---|---|
| Student | Primary User | Complete OJT successfully and on time | Medium |
| Lecturer / Academic Advisor | Primary User | Monitor assigned students and intervene when needed | High |
| OJT Coordinator | Primary User / Process Owner | Manage OJT operation across students and lecturers | Very High |
| Administrator | Supporting User | Manage accounts, roles, configurations, and system integrity | High |
| University Management | Business Stakeholder | Monitor OJT performance and institutional outcomes | High |
| Company Supervisor | External Stakeholder | Provide progress or evaluation information when applicable | Medium |
| IT / System Operations | Supporting Stakeholder | Ensure system availability, security, and deployment | Medium |

---

## 3. Detailed Stakeholder Analysis

### 3.1 Student

**Goals**
- Register and maintain OJT information.
- Submit OJT plans.
- Track milestones and deadlines.
- View progress status.
- Receive risk warnings and recommended actions.
- Complete OJT on time.

**Pain Points**
- Unclear deadlines or required steps.
- OJT information distributed across multiple channels.
- Late feedback.
- Difficulty knowing whether current progress is sufficient.

**System Needs**
- Personal dashboard.
- OJT plan management.
- Progress and milestone tracking.
- Notifications.
- Risk status and explanation.
- Recommended next actions.

---

### 3.2 Lecturer / Academic Advisor

**Goals**
- Monitor assigned students.
- Detect students needing support.
- Review student progress.
- Record interventions.
- Follow intervention outcomes.

**Pain Points**
- Manual checking of multiple students.
- Lack of consolidated progress information.
- Difficulty prioritizing which student needs attention first.
- No clear history of previous interventions.

**System Needs**
- Assigned-student dashboard.
- Risk filtering and sorting.
- Student detail page.
- Risk explanation.
- Intervention creation and tracking.
- Student progress history.

---

### 3.3 OJT Coordinator

**Goals**
- Manage OJT operations across the university or department.
- Monitor all active OJT students.
- Identify systemic issues.
- Coordinate lecturers and interventions.
- Produce operational reports.

**Pain Points**
- Fragmented student information.
- Manual reporting.
- Limited visibility across cohorts.
- Difficulty detecting risk early.

**System Needs**
- Central dashboard.
- Student and cohort monitoring.
- High-risk student list.
- Lecturer assignment visibility.
- Reports and analytics.
- Intervention monitoring.
- Configurable OJT periods and milestones.

---

### 3.4 Administrator

**Goals**
- Maintain system users and permissions.
- Configure system-level settings.
- Support secure system operation.

**System Needs**
- Account management.
- Role-based access control.
- System configuration.
- Audit log access.
- Reference/master data management.

---

### 3.5 University Management

**Goals**
- Understand overall OJT performance.
- Monitor completion and delay trends.
- Support policy and resource decisions.

**System Needs**
- Aggregated reports.
- Trend dashboards.
- OJT completion and delay metrics.
- Risk distribution by cohort or period.

University Management is not expected to modify operational student records directly.

---

### 3.6 Company Supervisor

**Goals**
- Confirm or provide information about student OJT progress where integration or direct participation is available.

**Potential System Needs**
- Submit or confirm evaluation information.
- Provide feedback.
- Confirm attendance or milestone completion.

This stakeholder is considered a future or optional integration participant in the first release.

---

## 4. Stakeholder Conflicts

Potential conflicts include:

### Student Privacy vs Management Visibility
Students require privacy, while lecturers and coordinators need enough information to manage OJT risk.

**Resolution principle:** role-based access control and least-privilege data access.

### AI Automation vs Human Judgment
AI may identify risk, but lecturers or coordinators may have contextual knowledge unavailable to the model.

**Resolution principle:** AI provides decision support, not automatic final academic decisions.

### Operational Simplicity vs Data Completeness
Requiring too much student input may improve data quality but reduce usability.

**Resolution principle:** collect only information necessary for OJT management and risk assessment.

---

## 5. Stakeholder Priority

For the MVP:

1. OJT Coordinator
2. Lecturer / Academic Advisor
3. Student
4. Administrator

University Management reporting will be included at a basic level.

Company Supervisor integration is out of scope for the MVP unless later prioritized.
