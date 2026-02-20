# Diagrama de Casos de Uso - Sistema de Matrículas

```mermaid
graph LR
    subgraph Atores
        direction TB
        Secretaria((Secretaria))
        Professor((Professor))
        Aluno((Aluno))
    end

    SC[("Sistema de Cobrança")]

    subgraph "Sistema de Matrículas"
        UC1(UC1: Realizar Login)
        UC2(UC2: Manter Disciplinas/Cursos)
        UC3(UC3: Efetuar Matrícula)
        UC4(UC4: Cancelar Matrícula)
        UC5(UC5: Consultar Lista de Alunos)
        UC6(UC6: Notificar Cobrança)
    end

    %% Conexões
    Secretaria --> UC2
    Professor --> UC5
    Aluno --> UC4
    Aluno --> UC3

    %% Inclusão de Login
    UC2 -.-> UC1
    UC3 -.-> UC1
    UC4 -.-> UC1
    UC5 -.-> UC1
    
    %% Fluxo de Cobrança
    UC3 ==> UC6
    UC6 --- SC

    %% Estilização
    style UC1 fill:#f9f,stroke:#333,stroke-width:2px
    style Atores fill:none,stroke:none
```
