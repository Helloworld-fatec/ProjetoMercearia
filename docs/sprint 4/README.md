# Sprint 4 — Chatbot Completo e Entrega Final

**Período:** 2 semanas

**Foco:** Evolução do chatbot WhatsApp, handoff para vendedores, gerenciamento de respostas automáticas, observações de clientes, homologação final e deploy em produção.

---

## Objetivo da Sprint

Concluir o desenvolvimento do sistema através da implementação completa do módulo de chatbot WhatsApp, permitindo atendimento híbrido entre automação e vendedores, gerenciamento de respostas automáticas sem necessidade de código, consulta de disponibilidade de produtos e registro de observações dos clientes.

A Sprint 4 encerra o ciclo de desenvolvimento do projeto, contemplando testes finais, homologação, documentação e preparação para publicação em produção.

---

## Definition of Done

Uma task é considerada **Concluída** quando:

* Código commitado na branch `feat/nome-da-task`
* Pull Request aprovado por pelo menos um integrante
* Testes automatizados executados com sucesso
* Cobertura mínima de testes atingida
* Pipeline CI/CD executado sem falhas
* Funcionalidade validada em homologação
* Documentação atualizada
* Sem bugs críticos ou bloqueantes
* Deploy validado em ambiente de produção

---

## Sprint Backlog

| ID    | Tarefa                                                          | Responsável | Horas | Status    |
| ----- | --------------------------------------------------------------- | ----------- | ----- | --------- |
| S4-01 | Implementar endpoint de observações de clientes                 | Nicolas     | 4h    | Concluído |
| S4-02 | Implementar endpoint de consulta de disponibilidade de produtos | Nicolas     | 4h    | Concluído |
| S4-03 | Implementar CRUD de respostas automáticas sem código            | Nicolas     | 5h    | Concluído |
| S4-04 | Criar painel de configuração de respostas automáticas           | Bruna       | 5h    | Concluído |
| S4-05 | Criar campo de observações do cliente                           | Bruna       | 3h    | Concluído |
| S4-06 | Criar testes dos fluxos administrativos do chatbot (TDD)        | Bruna       | 3h    | Concluído |
| S4-07 | Implementar lógica de handoff chatbot -> vendedor               | Bruno       | 5h    | Concluído |
| S4-08 | Implementar gerenciamento avançado das conversas                | Bruno       | 5h    | Concluído |
| S4-09 | Criar testes de integração dos fluxos conversacionais (TDD)     | Bruno       | 3h    | Concluído |
| S4-10 | Criar painel de acompanhamento das conversas                    | Suelen      | 4h    | Concluído |
| S4-11 | Executar homologação geral do sistema                           | Suelen      | 4h    | Concluído |
| S4-12 | Criar testes finais de regressão e validação (TDD)              | Suelen      | 4h    | Concluído |

---

## Detalhamento das Tasks

### Nicolas — Backend Chatbot e Clientes

| ID    | Task                                                            | História(s) Relacionada(s) | Descrição                                                                                          |
| ----- | --------------------------------------------------------------- | -------------------------- | -------------------------------------------------------------------------------------------------- |
| S4-01 | Implementar endpoint de observações de clientes                 | US-11                      | Criar funcionalidade para registrar e consultar observações relacionadas aos clientes.             |
| S4-02 | Implementar endpoint de consulta de disponibilidade de produtos | US-14                      | Disponibilizar endpoint para que o chatbot consulte estoque em tempo real.                         |
| S4-03 | Implementar CRUD de respostas automáticas sem código            | US-16                      | Permitir criação, edição, exclusão e consulta de respostas automáticas pelo painel administrativo. |

---

### Bruna — Frontend Administrativo

| ID    | Task                                                     | História(s) Relacionada(s) | Descrição                                                                       |
| ----- | -------------------------------------------------------- | -------------------------- | ------------------------------------------------------------------------------- |
| S4-04 | Criar painel de configuração de respostas automáticas    | US-16                      | Desenvolver interface para gerenciamento das respostas utilizadas pelo chatbot. |
| S4-05 | Criar campo de observações do cliente                    | US-11                      | Adicionar funcionalidade de observações dentro do cadastro de clientes.         |
| S4-06 | Criar testes dos fluxos administrativos do chatbot (TDD) | US-11, US-16               | Validar os fluxos de gerenciamento administrativo da solução.                   |

---

### Bruno — Integração WhatsApp

| ID    | Task                                                        | História(s) Relacionada(s) | Descrição                                                                   |
| ----- | ----------------------------------------------------------- | -------------------------- | --------------------------------------------------------------------------- |
| S4-07 | Implementar lógica de handoff chatbot -> vendedor           | US-15                      | Permitir transferência do atendimento automatizado para um vendedor humano. |
| S4-08 | Implementar gerenciamento avançado das conversas            | US-14, US-15               | Controlar estados de conversa, sessões e histórico de atendimento.          |
| S4-09 | Criar testes de integração dos fluxos conversacionais (TDD) | US-14, US-15, US-16        | Validar todos os fluxos do chatbot integrados ao WhatsApp.                  |

---

### Suelen — QA e Homologação

| ID    | Task                                               | História(s) Relacionada(s) | Descrição                                                                        |
| ----- | -------------------------------------------------- | -------------------------- | -------------------------------------------------------------------------------- |
| S4-10 | Criar painel de acompanhamento das conversas       | US-15                      | Desenvolver interface para monitoramento dos atendimentos realizados.            |
| S4-11 | Executar homologação geral do sistema              | Todas                      | Realizar validação completa de todos os módulos implementados durante o projeto. |
| S4-12 | Criar testes finais de regressão e validação (TDD) | Todas                      | Garantir que novas funcionalidades não impactaram recursos já entregues.         |

---

## Relação com Product Backlog

| História | Descrição                               | Tasks Relacionadas         |
| -------- | --------------------------------------- | -------------------------- |
| US-11    | Observações de clientes                 | S4-01, S4-05, S4-06        |
| US-14    | Consulta de disponibilidade de produtos | S4-02, S4-08, S4-09        |
| US-15    | Handoff chatbot -> vendedor             | S4-07, S4-08, S4-09, S4-10 |
| US-16    | Configuração de respostas automáticas   | S4-03, S4-04, S4-06, S4-09 |

---

## Estrutura Técnica Entregue

### Backend

* Endpoint de observações de clientes
* Endpoint de consulta de estoque para chatbot
* CRUD de respostas automáticas
* Gerenciamento de sessões de conversa
* Integração avançada com WhatsApp

### Frontend

* Painel administrativo do chatbot
* Tela de observações de clientes
* Painel de acompanhamento das conversas
* Configuração de respostas automáticas

### Qualidade

* Testes de regressão
* Testes de integração do chatbot
* Testes administrativos
* Homologação completa do sistema

### CI/CD

* Stage Checkout
* Stage Build Front
* Stage Build Back
* Stage Test
* Stage Quality Gate
* Stage Deploy Homolog
* Stage Deploy Production

---

## Distribuição por Membro

| Membro    | Papel            | Tasks        | Horas   |
| --------- | ---------------- | ------------ | ------- |
| Nicolas   | Backend          | 3            | 13h     |
| Bruna     | Frontend         | 3            | 11h     |
| Bruno     | API / Integração | 3            | 13h     |
| Suelen    | Full Stack / QA  | 3            | 12h     |
| **Total** |                  | **12 tasks** | **49h** |

---

## Entregáveis

* Chatbot WhatsApp completo
* Consulta de disponibilidade de produtos
* Handoff para vendedor
* Observações de clientes
* CRUD de respostas automáticas
* Painel administrativo do chatbot
* Painel de acompanhamento de conversas
* Testes de regressão
* Homologação final
* Deploy em produção

---

## Observações Gerais

* Todas as funcionalidades do chatbot devem ser configuráveis sem alteração de código.
* O handoff deve manter histórico completo da conversa.
* Consultas de estoque devem utilizar dados atualizados em tempo real.
* O deploy em produção só poderá ocorrer após aprovação da homologação.
* Garantir rastreabilidade de mensagens e interações.
* Todos os módulos das sprints anteriores devem permanecer operacionais após a entrega final.

---

## Revisão da Sprint

Durante a Sprint Review será apresentada a versão final do sistema, incluindo todos os módulos desenvolvidos ao longo do projeto.

### Itens a demonstrar

* Importação de produtos
* Controle de estoque
* Registro de vendas
* Controle financeiro
* Cadastro de clientes
* Relatórios gerenciais
* Ranking de clientes
* Integração WhatsApp
* Atendimento automatizado
* Handoff para vendedor
* Configuração de respostas automáticas
* Consulta de disponibilidade de produtos
* Pipeline CI/CD completo
* Deploy em produção

### Feedbacks Recebidos

> Resumo da Sprint Review, aprovação final do produto e observações dos stakeholders.

---

## Retrospectiva

### O que funcionou bem?

*

### O que pode melhorar?

*

### Ações Futuras

* Evoluir chatbot com inteligência artificial generativa.
* Criar aplicativo mobile para vendedores.
* Implementar dashboards analíticos avançados.
* Adicionar notificações em tempo real.
* Desenvolver integração com ERP.
* Criar indicadores avançados de atendimento e conversão.

---

# Encerramento do Projeto

## Resumo Geral

| Épico                        | User Stories | Story Points |
| ---------------------------- | ------------ | ------------ |
| EP-01 — Gestão de Estoque    | 4            | 19           |
| EP-02 — Controle de Caixa    | 4            | 16           |
| EP-03 — Cadastro de Clientes | 3            | 10           |
| EP-04 — Chatbot WhatsApp     | 5            | 41           |
| **Total**                    | **16**       | **86**       |

---

## Distribuição Final

| Integrante | Papel            | Tasks        |
| ---------- | ---------------- | ------------ |
| Nicolas    | Backend          | 12           |
| Bruna      | Frontend         | 12           |
| Bruno      | API / Integração | 12           |
| Suelen     | Full Stack / QA  | 12           |
| **Total**  |                  | **48 Tasks** |

---

## Entrega Final

* Sistema de Controle de Estoque
* Sistema de Caixa
* Cadastro de Clientes
* Relatórios Gerenciais
* Chatbot WhatsApp Integrado
* Pipeline CI/CD Completo
* Ambiente de Homologação
* Ambiente de Produção
* Testes Automatizados
* Documentação Técnica
* Documentação do Usuário

---
