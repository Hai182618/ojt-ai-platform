# Assumptions and Constraints

## 1. Assumptions

### AS-01
Each student has a unique identifier.

### AS-02
Each system user has exactly one primary role in the MVP.

### AS-03
OJT periods and milestones are defined by the university or department.

### AS-04
Student academic and OJT data required for risk assessment can be entered or imported into the system.

### AS-05
Lecturers and coordinators have authority to review student progress and record interventions.

### AS-06
The AI model receives only features that are available at prediction time.

### AS-07
Risk predictions are advisory and require human interpretation.

### AS-08
Users have Internet access and use a modern web browser.

### AS-09
The MVP serves one university/organizational context.

---

## 2. Constraints

### CO-01 — Portfolio Project Constraint
The system is developed as a portfolio-grade project, so real university production data may not be available.

### CO-02 — Data Constraint
Synthetic or anonymized data may be required for development and demonstration.

### CO-03 — AI Validation Constraint
Model performance demonstrated on synthetic or limited data must not be presented as validated production performance.

### CO-04 — Privacy Constraint
Sensitive student information must not be exposed publicly in the demo environment.

### CO-05 — Security Constraint
Secrets, database credentials, tokens, and API keys must not be committed to GitHub.

### CO-06 — Deployment Constraint
The initial deployment should use services suitable for a portfolio/demo environment.

### CO-07 — Integration Constraint
External university systems are not required for the MVP.

### CO-08 — Time Constraint
Features should be prioritized to produce an end-to-end working system before optional enhancements.

---

## 3. Design Principles Derived from Constraints

- Prefer modular architecture.
- Keep frontend, backend, database, AI, and documentation clearly separated.
- Use environment variables for secrets.
- Keep AI decisions explainable.
- Preserve human override.
- Maintain traceability from requirement to implementation and test.
- Use demo-safe data.
