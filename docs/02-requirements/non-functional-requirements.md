# Non-Functional Requirements

## 1. Purpose

This document defines quality attributes and technical constraints for the system.

---

# 2. Security

## NFR-SEC-001
Passwords shall never be stored in plaintext.

## NFR-SEC-002
Sensitive authentication secrets shall not be committed to source control.

## NFR-SEC-003
Protected API endpoints shall require valid authentication.

## NFR-SEC-004
Authorization shall be enforced by the backend and shall not rely only on frontend visibility.

## NFR-SEC-005
The system shall apply least-privilege access principles.

## NFR-SEC-006
Public demo data shall not contain real sensitive student information.

---

# 3. Performance

## NFR-PERF-001
Common interactive API requests should normally respond within 2 seconds under portfolio/demo load, excluding long-running AI training operations.

## NFR-PERF-002
Dashboard queries shall use pagination, aggregation, or other suitable mechanisms when result size grows.

## NFR-PERF-003
AI inference should be separated from model training so prediction requests do not trigger retraining.

---

# 4. Availability and Reliability

## NFR-REL-001
The deployed demo should recover gracefully from normal application errors without exposing stack traces to end users.

## NFR-REL-002
Database operations that modify multiple related records shall use transaction boundaries where consistency requires them.

## NFR-REL-003
Critical historical records such as risk predictions and audit records shall not be silently overwritten.

---

# 5. Maintainability

## NFR-MNT-001
Frontend, backend, database, AI, documentation, and deployment concerns shall remain modular.

## NFR-MNT-002
Source code shall use consistent naming and folder conventions.

## NFR-MNT-003
Environment-specific settings shall be externalized through configuration or environment variables.

## NFR-MNT-004
Major architectural decisions shall be documented.

---

# 6. Usability

## NFR-USA-001
Primary workflows shall expose clear status information to users.

## NFR-USA-002
Validation errors shall identify the field or action requiring correction.

## NFR-USA-003
Risk information shall use understandable labels in addition to numeric scores.

## NFR-USA-004
AI explanations shall avoid presenting a probability score as certainty.

---

# 7. Compatibility

## NFR-COMP-001
The web application shall support current major Chromium-based desktop browsers.

## NFR-COMP-002
The UI shall be responsive enough to remain usable on common laptop and tablet widths.

---

# 8. Observability

## NFR-OBS-001
Backend errors shall be logged with sufficient technical context for debugging.

## NFR-OBS-002
Logs shall avoid exposing passwords, tokens, or other secrets.

## NFR-OBS-003
AI predictions shall retain model version and timestamp information.

---

# 9. Data Integrity

## NFR-DATA-001
Primary business entities shall use stable unique identifiers.

## NFR-DATA-002
Required database relationships shall use integrity constraints where appropriate.

## NFR-DATA-003
Deletion behavior for referenced records shall be explicitly defined rather than assumed.

## NFR-DATA-004
Timestamps shall use a consistent storage strategy.

---

# 10. Testability

## NFR-TEST-001
Core business rules shall be testable independently from the UI where practical.

## NFR-TEST-002
API contracts shall be documented sufficiently for integration testing.

## NFR-TEST-003
Each critical business workflow shall have at least one positive and one negative test scenario before MVP completion.
