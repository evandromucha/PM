```mermaid
flowchart TD

%% IDENTIDADE E ESTRATÉGIA
subgraph Estrategia [IDENTIDADE E ESTRATÉGIA]
    VAL[Valores Éticos/nResponsabilidade, Respeito, Equidade, Honestidade]
    VIS[Visão \nOnde a empresa quer chegar]
    MIS[Missão \nPropósito organizacional]
    OKR[OKRs\n Objetivos e Resultados-Chave]

    VAL --> VIS --> MIS --> OKR
end

%% INFLUÊNCIAS E GOVERNANÇA
subgraph Influencias [INFLUÊNCIAS E GOVERNANÇA]
    direction LR
    FAE[FAEs\nMercado, Cultura, Ambiente]
    APO[APOs\nTemplates, Políticas, Lições]
    GOV{Governança\nRegras e Tomada de Decisão}
end

%% SISTEMA DE ENTREGA DE VALOR
subgraph GOP [SISTEMA DE ENTREGA DE VALOR]
    PORT[Gerenciamento de Portfólios\nAlinhamento Estratégico]
    PROG[Gerenciamento de Programas\nObtenção de Benefícios]
    PROJ[Gerenciamento de Projetos\nResultados Únicos]
    OPER[Operações\nValor Recorrente]

    PORT --> PROG
    PROG --> PROJ
    PORT --> OPER
end

%% FLUXO DE EXECUÇÃO
subgraph Fluxo [FLUXO DE EXECUÇÃO E ENTREGA]
    START[Iniciação\nTermo de Abertura]
    ROAD[Roadmap\nDireção do Produto]
    LIFE{Ciclo de Vida}
    PRED[Preditivo\nFase a Fase]
    ADAP[Adaptativo\nIncremental / Ágil]
    ENTREGA[Entrega e Transição]
    BENE[Realização de Benefícios]

    START --> ROAD --> LIFE
    LIFE --> PRED
    LIFE --> ADAP
    PRED --> ENTREGA
    ADAP --> ENTREGA
    ENTREGA --> BENE
end

%% CONEXÕES ENTRE CAMADAS
OKR --> PORT
PROJ --> START
FAE -.-> PROJ
APO -.-> PROJ
GOV -.-> GOP
```
