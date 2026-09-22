# System Context

```mermaid
flowchart LR
    STU[Student]
    LEC[Lecturer / Advisor]
    COORD[OJT Coordinator]
    ADM[Administrator]
    MGMT[University Management]

    SYS[AI-Powered OJT Management System]

    STU -->|Profile, OJT plan, progress updates| SYS
    SYS -->|Status, milestones, alerts, recommendations| STU

    LEC -->|Review, monitoring, intervention| SYS
    SYS -->|Assigned students, risk, history| LEC

    COORD -->|Configuration, monitoring, intervention| SYS
    SYS -->|Program dashboard, reports, risk overview| COORD

    ADM -->|Accounts, roles, configuration| SYS
    SYS -->|Administration information| ADM

    MGMT -->|Reporting request| SYS
    SYS -->|Aggregated reporting| MGMT
```

## Context Boundary

The system does not initially replace:
- the university's full Student Information System;
- an LMS;
- company HR systems;
- payroll systems.

External integration can be added later through defined APIs or import processes.
