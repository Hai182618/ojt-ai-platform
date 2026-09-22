# TO-BE OJT Management Process

## 1. Objective

Create a centralized process where operational data, progress monitoring, risk assessment, and intervention are connected.

---

## 2. TO-BE Flow

```mermaid
flowchart TD
    A[Student OJT eligibility available] --> B[Student creates OJT plan]
    B --> C[System validates required information]
    C --> D{Valid?}
    D -- No --> E[Show validation errors]
    E --> B
    D -- Yes --> F[Submit OJT plan]
    F --> G[Lecturer / Coordinator review]
    G --> H{Approved?}
    H -- No --> I[Record rejection reason]
    I --> B
    H -- Yes --> J[Activate OJT tracking]
    J --> K[Track milestones and progress]
    K --> L[Generate / refresh risk assessment]
    L --> M{Risk elevated?}
    M -- No --> K
    M -- Yes --> N[Show risk factors and recommendations]
    N --> O[Lecturer / Coordinator reviews context]
    O --> P{Intervention needed?}
    P -- No --> K
    P -- Yes --> Q[Create intervention]
    Q --> R[Track intervention outcome]
    R --> K
    K --> S{OJT completed?}
    S -- No --> K
    S -- Yes --> T[Record completion]
```

---

## 3. Expected Improvements

- Centralized student and OJT information.
- Explicit workflow status.
- Earlier visibility of risk.
- Risk-based prioritization.
- Traceable intervention actions.
- Historical prediction records.
- Easier operational reporting.

These are intended improvements and must later be measured rather than assumed.
