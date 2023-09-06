```mermaid
    flowchart TD             
    subgraph "`**Platform Registration**`"
    A(Candidate) --> B[Register on Platform]
    B --> C(User registers witht their email)
    C --> D(User accepts terms and conditions)
    D-.->E(User Receives a Welcome Email)
    style E fill:#ff9800,stroke:#333,stroke-width:2px
    E --> F(User completes their profile)
    F --> G[/User sees the Dashboard/]
    G --> H[/Are there open jobs?/]
    H --> |yes| I(Express Interest)
    H --> |No| G
    I --> K[/EOI Valid?/]
    K --> |No or Position Closed| L(Decline)
    G --> M(Upskilling Opportunities)
    end
    subgraph "`**Internal Shortlist**`"
    K --> |Yes| S
    S(Internal Shortlist) --> T(Search)
    S --> U(Database Search)
    S --> V(Excel Sheets, Google Drive, etc.)
    U --> W(Import Profile)
    T --> W 
    V --> W
    W --> X(Create a Job Match)
    X --> Y(Internal Shortlist)
    Y --> Z(Intake)
    Z --> A1("`Job match is set to **Internal Shortlist**`")
    Z --> B1("`Status is set to **Intake**`")
    A1-.->C1(User Receives an Intake Scheduling Email)
    style C1 fill:#ff9800,stroke:#333,stroke-width:2px
    B1-.->C1
    C1 --> D1(User Schedules the Intake)
    D1 --> E1(Intake is completed)
    E1 --> EE1(Set the intake date on candidate profile)
    EE1 --> F1(Eligibility Check)
    F1 --> G1(Confirmation of Interest)
    G1 --> H1(Set the Confirmation of Interest tag)
    H1-.->I1(User receives an Email)
    style I1 fill:#ff9800,stroke:#333,stroke-width:2px
    I1 --> J1(CV Development)
    J1-.->K1(Candidates receive an email requesting to update their CV and email it back)
    style K1 fill:#ff9800,stroke:#333,stroke-width:2px
    K1 --> L1(Tag is set to: Ready for Employer)
    end
    subgraph "`**Shortlist**`"
    L1 --> M1(Manual Email to Employer with shortlist)
    M1 --> N1(Employer responds)
    N1 --> O1(Interview one or more candidates)
    N1 --> P1(Another round of candidates)
    N1 --> Q1(Declines to proceed)
    end
    subgraph "`**Interview Offer**`"
    O1-.->R1(Schedule a volunteer interview. 
    Tag=Schedule volunteer interview)
    P1-.->R1
    end
    subgraph "`**Interview**`"
    R1 --> S1(Job Offer)
    R1 --> T1(Unsuccessful)
    end
    subgraph "`**Job Offer**`"
    S1 --> U1(Employer Invoice)
    S1 --> V1(Set tag=Job Offer Signed)
    end
    subgraph "`**Legal Flow**`"
    U1 & V1 --> W1(Recruitment Informs Legal about a Job Offer)
    W1 --> X1(Matter or database card is created: OINP… EMPP Stream A… EMPP Stream B… NLPNP)
    X1-.->Y1(Folders are created)
    style Y1 fill:#8bc34a,stroke:#333,stroke-width:2px
    X1 --> Z1(Legal Makes a Decision)
    Z1 --> A2(Candidate is invited to Slack)
    Z1 --> B2(Depending on Matter, Legal submit the forms)
    B2 --> C2(Status is changed to submitted)
    C2 --> D2(Candidate is approved for PR)
    end
    subgraph "`**Settlement Flow**`"
    D2 --> E2(Settlement team complete user details)
    E2 --> F2(Tasks are generated to be followed by Settlement team)
    end
```