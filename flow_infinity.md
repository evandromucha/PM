flowchart TB
  %% Enterprise-to-Value Delivery flow with governance, compliance, monitoring, and stakeholders

  %% --- Enterprise context / direction ---
  subgraph E[Enterprise Context & Direction]
    VVM[Values • Vision • Mission]
    STRAT[Organizational Strategy & Objectives]
    POL[Policies • Ethical/Social Responsibilities • Risk Appetite]
    VVM --> STRAT
    VVM --> POL
    POL --> STRAT
  end

  %% --- Governance overlay (organizational + project) ---
  subgraph GOV[Governance (Direction & Control)]
    OG[Organizational Governance
(Board/Exec Committee)]
    PG[Project/Program/Portfolio Governance
(Boards, decision models, RACI, stage gates)]
    OG --> PG
  end

  %% Governance influences strategy and execution
  OG -.sets principles & oversight.-> STRAT
  PG -.authorizes & controls.-> EXEC

  %% --- System for Value Delivery ---
  subgraph SVD[System for Value Delivery]
    PORT[Portfolio]
    PROG[Programs]
    OPS[Operations]
    PROD[Products]
    PROJ[Projects]
    STRAT --> PORT
    PORT --> PROG
    PORT --> PROJ
    PROG --> PROJ
    PROJ --> PROD
    PROD --> OPS
  end

  %% --- Project execution / delivery ---
  subgraph EXEC[Project Delivery (Lifecycle)]
    INIT[Initiate / Charter]
    PLAN[Plan]
    DO[Execute]
    MON[Monitor & Control]
    CLOSE[Close / Transition]
    INIT --> PLAN --> DO --> MON --> CLOSE
  end

  %% Value realization / outcomes
  CLOSE --> OUT[Outputs & Outcomes]
  OUT --> VALUE[Value Delivered (Benefits/Value)]
  VALUE --> STRAT

  %% --- Stakeholders & external/internal influences ---
  subgraph STK[Stakeholders & Needs]
    CUST[Customers / Users]
    SPON[Sponsor]
    TEAM[Project Team]
    OPSM[Operations / Service Owners]
    SUP[Suppliers / Partners]
    COMM[Community / Society]
  end

  %% Stakeholder relationships to project and value
  CUST -->|Needs & acceptance criteria| PLAN
  SPON -->|Funding, priorities, decisions| INIT
  TEAM -->|Delivery| DO
  OPSM -->|Operational readiness & transition| CLOSE
  SUP -->|Contracts, deliverables| DO
  COMM -->|Expectations & impact| STRAT

  %% --- Regulators, compliance, and assurance ---
  subgraph COMP[Regulators • Compliance • Assurance]
    REG[Regulators / Laws]
    STD[Industry Standards]
    AUD[Audit / Assurance]
    SEC[Security / Privacy / Safety]
  end

  REG -->|Requirements| PLAN
  STD -->|Constraints & practices| PLAN
  SEC -->|Controls| DO
  AUD -->|Independent review| MON

  %% --- Enterprise Environmental Factors (influences/constraints) ---
  subgraph EEF[Influences (Enterprise Environmental Factors)]
    CULT[Culture • Structure • Leadership]
    MARKET[Market / Competition]
    TECH[Technology Landscape]
    ECO[Economic / Geopolitical]
  end

  CULT -.influences.-> INIT
  MARKET -.influences.-> STRAT
  TECH -.constraints/opportunities.-> PLAN
  ECO -.risks/constraints.-> MON

  %% --- Monitoring, reporting, and feedback loops ---
  MON -->|Performance data, risk/issues| PG
  PG -->|Decisions, change authorization| PLAN
  MON -->|Compliance evidence| COMP
  PG -->|Escalations| OG
