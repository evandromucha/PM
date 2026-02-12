flowchart TD

    %% Nível Estratégico: O Topo da Pirâmide
    subgraph Estrategia [IDENTIDADE E ESTRATÉGIA ORGANIZACIONAL]
        VAL[<b>Valores Éticos</b><br/>Responsabilidade, Respeito, Equidade e Honestidade] 
        VIS[<b>Visão</b><br/>Destino futuro e metas mais desejáveis]
        MIS[<b>Missão</b><br/>Propósito predeterminado da organização]
        OBJ[<b>Estratégia e Objetivos</b><br/>Áreas de desempenho e caminhos definidos]
        OKR[<b>OKRs (Objectives & Key Results)</b><br/>Estrutura de metas para alinhamento tático-estratégico]

        VAL --> VIS --> MIS --> OBJ --> OKR
    end

    %% Influências e Governança: A Moldura do Sistema
    subgraph Influencias [INFLUÊNCIAS E GOVERNANÇA]
        GOV{<b>Governança do Projeto</b><br/>Framework de supervisão, regras do jogo e tomada de decisão}
        FAE[<b>FAEs (Fatores Ambientais)</b><br/>Internos: Cultura, Software<br/>Externos: Mercado, Leis, PESTLE]
        APO[<b>APOs (Ativos de Processos)</b><br/>Processos, Políticas, Templates e Lições Aprendidas]
    end

    %% GOP: Sistema de Entrega de Valor
    subgraph GOP [GOP: SISTEMA DE ENTREGA DE VALOR]
        PORT[<b>Gerenciamento de Portfólios</b><br/>Seleção de investimentos alinhada à estratégia]
        PROG[<b>Gerenciamento de Programas</b><br/>Coordenação de projetos para obtenção de benefícios]
        PROJ[<b>Gerenciamento de Projetos</b><br/>Esforço temporário para criar um resultado único]
        OPER[<b>Operações Contínuas</b><br/>Geração recorrente de valor para o negócio]
    end

    %% Fluxo de Entrega: Da Iniciação aos Benefícios
    subgraph Fluxo_Entrega [FLUXO DE EXECUÇÃO E ENTREGA]
        START[<b>Iniciação</b><br/>Termo de Abertura e Visão do Projeto]
        PLAN[<b>Planejamento / Roadmap</b><br/>Direção global e visão do produto]
        LIFE{<b>Ciclo de Vida</b>}
        PRED[<b>Abordagem Preditiva</b><br/>Fases lineares e Revisões de Fase/Gates]
        ADAP[<b>Abordagem Adaptativa (Ágil)</b><br/>Backlogs e Iterações/Sprints de valor incremental]
        TRANS[<b>Entrega e Transição</b><br/>Transferência do produto para o cliente ou operações]
        VALOR[<b>Realização de Benefícios</b><br/>Sustentabilidade e concretização do valor esperado]
    end

    %% Conexões entre as Camadas
    OKR --> PORT
    PORT --> PROG
    PROG --> PROJ
    PORT --> OPER

    PROJ --> START
    START --> PLAN
    PLAN --> LIFE
    LIFE --> PRED
    LIFE --> ADAP
    PRED --> TRANS
    ADAP --> TRANS
    TRANS --> VALOR

    %% Influências Laterais
    GOV -.-> GOP
    FAE -.-> PROJ
    APO -.-> PROJ

    %% Estilização
    style Estrategia fill:#f9f,stroke:#333,stroke-width:2px
    style Influencias fill:#fff4dd,stroke:#d4a017,stroke-width:2px
    style GOP fill:#e1f5fe,stroke:#01579b,stroke-width:2px
    style Fluxo_Entrega fill:#e8f5e9,stroke:#2e7d32,stroke-width:2px
