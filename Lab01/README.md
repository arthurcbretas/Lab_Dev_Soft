# Sistema de Matrículas - PUC Minas

Repositório destinado ao desenvolvimento do **Laboratório 01** da disciplina de Laboratório de Desenvolvimento de Software (4º Período). O projeto consiste em um sistema para automatizar o processo de matrículas de uma universidade.

---

## Sprint 01: Modelo de Análise

### Personas e Atores
* **Secretaria:** Responsável por gerar o currículo acadêmico e manter dados de disciplinas, professores e alunos.
* **Aluno:** Pode se matricular em disciplinas (obrigatórias e optativas) e cancelar matrículas.
* **Professor:** Consulta a lista de alunos matriculados em suas turmas.
* **Sistema de Cobrança:** Ator externo notificado após a confirmação da matrícula.

### Histórias de Usuário

#### HU01 - Manutenção de Currículo e Dados
**Como** membro da Secretaria,  
**quero** gerenciar as informações de cursos, disciplinas, professores e alunos,  
**para** que o sistema reflita a oferta acadêmica correta do semestre.
* **Critérios de Aceitação:**
    * Cada curso deve registrar nome e número de créditos.
    * O sistema deve permitir a vinculação de professores às disciplinas.

#### HU02 - Realização de Matrícula
**Como** Aluno,  
**quero** selecionar minhas disciplinas para o próximo semestre,  
**para** garantir minha vaga e progressão no curso.
* **Critérios de Aceitação:**
    * Limite de até 4 disciplinas obrigatórias (1ª opção).
    * Limite de até 2 disciplinas optativas (alternativas).
    * O sistema deve bloquear matrículas se a turma atingir 60 alunos.

#### HU03 - Cancelamento de Matrícula
**Como** Aluno,  
**quero** ter a opção de cancelar uma matrícula dentro do período permitido,  
**para** ajustar minha grade horária conforme minha necessidade[cite: 12].
* **Critérios de Aceitação:**
    * A ação só pode ser realizada durante os períodos de matrícula definidos.

#### HU04 - Autenticação de Segurança
**Como** Usuário do Sistema,  
**quero** realizar login através de usuário e senha,  
**para** proteger minhas informações e restringir o acesso a funções específicas.
* **Critérios de Aceitação:**
    * O sistema deve validar as credenciais antes de liberar o acesso.

#### HU05 - Fechamento de Turmas (Processo Automático)
**Como** Sistema,  
**quero** validar o quórum mínimo de cada disciplina ao fim do período de matrícula,  
**para** decidir se a turma será aberta ou cancelada.
* **Critérios de Aceitação:**
    * Disciplinas com menos de 3 inscritos devem ser canceladas.
    * O Sistema de Cobrança deve ser notificado após a confirmação da inscrição.

#### HU06 - Consulta de Alunos por Turma
**Como** Professor,  
**quero** visualizar a lista de alunos inscritos em minhas turmas,  
**para** gerenciar o diário de classe e atividades acadêmicas.
* **Critérios de Aceitação:**
    * A lista deve estar disponível para todas as disciplinas vinculadas ao professor.

---

## Especificações Técnicas

* **Linguagem:** Java.
* **Interface:** Linha de Comando (CLI).
* **Persistência:** Arquivos de texto ou binários.
* **Modelo de Desenvolvimento:** Ágil (Sprints).

---

## Próximos Passos
- [ ] **Sprint 02:** Diagrama de Classes e Esqueleto do Código (Stubs).
- [ ] **Sprint 03:** Implementação completa, interface e persistência.