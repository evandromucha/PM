flowchart TD
    %% Nível Estratégico: Identidade Organizacional
    subgraph Estrategia ["IDENTIDADE E ESTRATÉGIA"]
        VAL["<b>Valores Éticos</b><br/>(Responsabilidade, Respeito, Equidade, Honestidade)"]
        VIS["<b>Visão</b><br/>(Onde a empresa quer chegar)"]
        MIS["<b>Missão</b><br/>(Propósito predeterminado)"]
        OKR["<b>OKRs</b><br/>(Objetivos e Resultados-Chave)"]
        
        VAL --> VIS --> MIS --> OKR
    end

    %% Influências e Governança
    subgraph Influencias ["INFLUÊNCIAS E GOVERNANÇA"]
        direction LR
        FAE["<b>FAE</b><br/>(Fatores Ambientais: Mercado, Cultura)"]
        APO["<b>APO</b><br/>(Ativos de Processos: Templates, Lições)"]
        GOV{{"<b>Governança</b><br/>(Regras e Tomada de Decisão)"}}
    end

    %% GOP: Sistema de Entrega de Valor
    subgraph GOP ["GOP: SISTEMA DE ENTREGA DE VALOR"]
        PORT["<b>Gerenciamento de Portfólios</b><br/>(Alinhamento de Investimentos)"]
        PROG["<b>Gerenciamento de Programas</b><br/>(Obtenção de Benefícios)"]
        PROJ["<b>Gerenciamento de Projetos</b><br/>(Criação de Resultados Únicos)"]
        OPER["<b>Operações</b><br/>(Geração Recorrente de Valor)"]
        
        PORT --> PROG
        PROG --> PROJ
        PORT --> OPER
    end

    %% Fluxo de Entrega
    subgraph Fluxo ["FLUXO DE EXECUÇÃO E ENTREGA"]
        START["<b>Iniciação</b><br/>(Termo de Abertura e Visão)"]
        ROAD["<b>Roadmap</b><br/>(Direção do Produto)"]
        LIFE{"<b>Ciclo de Vida</b>"}
        PRED["<b>Preditivo</b><br/>(Fase a Fase)"]
        ADAP["<b>Adaptativo</b><br/>(Incremental/Ágil)"]
        ENTREGA["<b>Entrega e Transição</b><br/>(Passagem para o Cliente)"]
        BENE["<b>Realização de Benefícios</b><br/>(Sustentabilidade do Valor)"]
        
        START --> ROAD --> LIFE
        LIFE --> PRED
        LIFE --> ADAP
        PRED --> ENTREGA
        ADAP --> ENTREGA
        ENTREGA --> BENE
    end

    %% Conexões entre camadas
    OKR --> PORT
    PROJ --> START
    FAE -.-> PROJ
    APO -.-> PROJ
    GOV -.-> GOP

    %% Estilização para o GitHub
    style Estrategia fill:#f9f9f9,stroke:#333,stroke-width:2px
    style Influencias fill:#fff4dd,stroke:#d4a017,stroke-width:2px
    style GOP fill:#e1f5fe,stroke:#01579b,stroke-width:2px
    style Fluxo fill:#e8f5e9,stroke:#2e7d32,stroke-width:2px
