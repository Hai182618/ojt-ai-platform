# Project Scope

## 1. Scope Objective

Define the boundaries of the first production-capable version of the AI-Powered OJT Management & Risk Prediction System.

---

## 2. In Scope

### 2.1 Authentication and Authorization
- User login
- Secure authentication
- Role-based access control
- Student role
- Lecturer role
- OJT Coordinator role
- Administrator role

### 2.2 Student Management
- Student profile
- Academic information relevant to OJT
- OJT eligibility information
- Current OJT status
- Assigned lecturer/advisor

### 2.3 OJT Planning
- Create OJT plan
- Record company information
- Record OJT period
- Record OJT position/role
- Submit plan
- Review plan
- Approve/reject plan
- Track plan status

### 2.4 OJT Progress Tracking
- Create and manage milestones
- Record milestone completion
- Record progress updates
- Track deadlines
- View progress history
- Identify overdue milestones

### 2.5 Risk Prediction
- Generate OJT delay risk score
- Classify risk level
- Store prediction history
- Display prediction timestamp
- Display relevant risk factors

### 2.6 Risk Explanation
- Explain major factors contributing to risk
- Show understandable risk reasons to authorized users
- Avoid presenting the AI result as an unquestionable final decision

### 2.7 Recommendation
- Generate recommended intervention actions
- Associate recommendations with detected risk factors
- Allow authorized users to choose an intervention

### 2.8 Intervention Management
- Create intervention record
- Assign intervention owner
- Set intervention status
- Add notes
- Track intervention outcome
- Maintain intervention history

### 2.9 Dashboards
- Student dashboard
- Lecturer dashboard
- Coordinator dashboard
- Administrator dashboard
- High-risk student view
- OJT progress overview

### 2.10 Reporting
- OJT status summary
- Risk distribution
- Milestone completion summary
- Intervention summary
- Basic export where appropriate

### 2.11 Auditability
- Record selected important user actions
- Maintain timestamps for critical changes
- Preserve risk prediction history

---

## 3. Out of Scope for MVP

The following are intentionally excluded from the first release:

- Payroll
- Company HR management
- Full university Student Information System replacement
- Full Learning Management System
- Attendance hardware integration
- Biometric authentication
- Automatic academic grading
- Automatic disciplinary decisions
- Automatic rejection or approval based only on AI
- Mobile native application
- Direct company supervisor portal
- Real-time chat
- Video conferencing
- Blockchain
- Payment processing
- Full enterprise data warehouse
- Multi-university SaaS tenancy

These may be considered future enhancements.

---

## 4. AI Scope Boundary

The AI component is a **decision-support system**.

It may:
- estimate delay risk;
- identify contributing factors;
- suggest possible actions.

It must not:
- make final academic decisions automatically;
- impose penalties;
- approve or reject OJT by itself;
- replace lecturer/coordinator judgment.

---

## 5. MVP Completion Definition

The MVP is considered functionally complete when:

1. Users can log in under supported roles.
2. Student OJT information can be created and managed.
3. OJT plans can be submitted and reviewed.
4. Progress and milestones can be tracked.
5. The system can generate a risk prediction.
6. Authorized users can understand major risk reasons.
7. Lecturers/coordinators can create and track interventions.
8. Dashboards expose relevant OJT and risk information.
9. Core flows are covered by documented UAT scenarios.
10. The system can be demonstrated through a deployed environment.
