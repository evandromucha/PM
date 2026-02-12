flowchart TB
  %% PMBOK® Guide – Seventh Edition aligned view
  %% Organizational System for Value Delivery + Performance Domains
  %% Showing where Predictive / Agile (Adaptive) / Hybrid commonly fit

  subgraph ORG["Organization & Context (System for Value Delivery)"]
    VVM["Values • Vision • Mission"]
    STRAT["Strategy & Objectives"]
    VVM --> STRAT

    EEF["Enterprise Environment<br/>(culture, structure, market, tech, etc.)"]
    COMP["Compliance Environment<br/>(laws, regulators, standards)"]

    EEF -. influences .-> STRAT
    COMP -. constrains .-> STRAT

    PORT["Portfolio"]
    PROG["Program(s)"]
    OPS["Operations & Product Mgmt"]

    STRAT --> PORT
    PORT --> PROG
    STRAT --> OPS
  end

  %% Governance Performance Domain
  subgraph GOVPD["Governance Performance Domain"]
    OG["Organizational Governance<br/>(board / executives)"]
    PG["Project Governance<br/>(decision rights, reporting,<br/>change control, escalation)"]

    OG --> PG

    G_TAIL["Tailoring Signal:<br/>
    Predictive → formal controls<br/>
    Agile → lighter governance via events & artifacts<br/>
    Hybrid → mixed controls based on risk"]
  end

  OG -. oversight .-> STRAT
  PG -. authorizes / steers .-> PROJ
  G_TAIL --- PG

  %% Project Level (Performance Domains)
  subgraph PROJ["Project (PMBOK7 Performance Domains)"]
    direction["Stakeholders PD<br/>identify, analyze, engage"]
    team["Team PD<br/>culture, leadership, collaboration"]
    plan["Planning PD<br/>plans, estimates, baselines / rolling wave"]
    work["Work PD<br/>produce deliverables, manage flow"]
    delivery["Delivery PD<br/>incremental or complete delivery"]
    measure["Measurement PD<br/>metrics, forecasts, transparency"]
    uncertainty["Uncertainty PD<br/>risk, ambiguity, complexity"]

    direction --> team --> plan --> work --> delivery --> measure --> uncertainty
    measure --> plan
    uncertainty --> plan
  end

  %% Connections
  PROG --> PROJ

  delivery --> VALUE["Value / Benefits Realization"]
  VALUE --> OPS
  VALUE --> STRAT

  STK["Key Stakeholders<br/>
  customers, sponsor, PMO,<br/>
  suppliers, functions, community"] --> direction

  COMP --> PG
  COMP --> plan
  COMP --> measure

  %% Development Approaches
  subgraph APPR["Development Approaches (Tailored)"]
    PRED["Predictive<br/>
    • scope & schedule baselined<br/>
    • stage gates<br/>
    • formal change control"]

    AGILE["Agile / Adaptive<br/>
    • iterative delivery<br/>
    • timeboxed planning<br/>
    • self-managed teams"]

    HYB["Hybrid<br/>
    • predictive governance<br/>
    • agile execution<br/>
    • mixed cadence"]
  end

  %% Mapping approach tendencies
  PRED -. stronger fit .-> plan
  PRED -. stronger fit .-> PG
  PRED -. stronger fit .-> measure

  AGILE -. stronger fit .-> work
  AGILE -. stronger fit .-> delivery
  AGILE -. stronger fit .-> team

  HYB -. common fit .-> plan
  HYB -. common fit .-> delivery
  HYB -. common fit .-> PG
