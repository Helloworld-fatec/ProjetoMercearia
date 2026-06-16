# Sprint 3 — Caixa + Clientes + Chatbot Básico

**Período:** 2 semanas

**Foco:** Relatórios gerenciais, controle financeiro do caixa, ranking de clientes e integração inicial com WhatsApp.

---

## Objetivo da Sprint

Consolidar o módulo de caixa por meio da geração de relatórios e controle de despesas operacionais, ampliar o módulo de clientes com indicadores de recorrência e iniciar a implementação do chatbot integrado ao WhatsApp.

A Sprint 3 tem como objetivo fornecer informações gerenciais para tomada de decisão e disponibilizar o primeiro fluxo automatizado de atendimento aos clientes.

---

## Definition of Done

Uma task é considerada **Concluída** quando:

* Código commitado na branch `feat/nome-da-task`
* Pull Request aprovado por pelo menos um integrante
* Testes automatizados implementados e aprovados
* Integração frontend -> backend funcionando corretamente
* Nenhum erro crítico de compilação ou execução
* Pipeline CI executado com sucesso
* Cobertura mínima de testes mantida
* Documentação atualizada quando necessário

---

## Sprint Backlog

| ID    | Tarefa                                                            | Responsável | Horas | Status    |
| ----- | ----------------------------------------------------------------- | ----------- | ----- | --------- |
| S3-01 | Implementar serviço de exportação de relatórios por período       | Nicolas     | 5h    | Concluído |
| S3-02 | Implementar serviço de registro de despesas e saídas de caixa     | Nicolas     | 4h    | Concluído |
| S3-03 | Criar testes unitários dos serviços de relatório e despesas (TDD) | Nicolas     | 3h    | Concluído |
| S3-04 | Criar tela de exportação de relatórios de vendas                  | Bruna       | 4h    | Concluído |
| S3-05 | Criar tela de registro de despesas e saídas de caixa              | Bruna       | 4h    | Concluído |
| S3-06 | Criar tela de ranking de clientes frequentes                      | Bruna       | 4h    | Concluído |
| S3-07 | Desenvolver API de exportação de relatórios (PDF/Excel)           | Bruno       | 5h    | Concluído |
| S3-08 | Desenvolver API e integração com WhatsApp (chatbot básico)        | Bruno       | 6h    | Concluído |
| S3-09 | Implementar respostas automáticas para dúvidas frequentes         | Bruno       | 4h    | Concluído |
| S3-10 | Integrar telas de relatórios e despesas com APIs                  | Suelen      | 4h    | Concluído |
| S3-11 | Integrar tela de ranking com API de clientes                      | Suelen      | 3h    | Concluído |
| S3-12 | Criar testes de integração do chatbot e relatórios (TDD)          | Suelen      | 4h    | Concluído |

---

## Detalhamento das Tasks

### Nicolas — Backend Financeiro

| ID    | Task                                                              | História(s) Relacionada(s) | Descrição                                                                                        |
| ----- | ----------------------------------------------------------------- | -------------------------- | ------------------------------------------------------------------------------------------------ |
| S3-01 | Implementar serviço de exportação de relatórios por período       | US-07                      | Desenvolver serviço responsável por gerar relatórios de vendas filtrados por intervalo de datas. |
| S3-02 | Implementar serviço de registro de despesas e saídas de caixa     | US-08                      | Criar regras de negócio para registrar movimentações financeiras negativas.                      |
| S3-03 | Criar testes unitários dos serviços de relatório e despesas (TDD) | US-07, US-08               | Validar geração correta dos relatórios e registro das despesas.                                  |

---

### Bruna — Frontend Financeiro e Clientes

| ID    | Task                                                 | História(s) Relacionada(s) | Descrição                                                          |
| ----- | ---------------------------------------------------- | -------------------------- | ------------------------------------------------------------------ |
| S3-04 | Criar tela de exportação de relatórios de vendas     | US-07                      | Desenvolver interface para geração e download dos relatórios.      |
| S3-05 | Criar tela de registro de despesas e saídas de caixa | US-08                      | Desenvolver formulário para cadastro de despesas operacionais.     |
| S3-06 | Criar tela de ranking de clientes frequentes         | US-10                      | Criar dashboard apresentando clientes com maior volume de compras. |

---

### Bruno — APIs e Integração WhatsApp

| ID    | Task                                                      | História(s) Relacionada(s) | Descrição                                                       |
| ----- | --------------------------------------------------------- | -------------------------- | --------------------------------------------------------------- |
| S3-07 | Desenvolver API de exportação de relatórios (PDF/Excel)   | US-07                      | Disponibilizar endpoint para geração e download de relatórios.  |
| S3-08 | Desenvolver API e integração com WhatsApp                 | US-12                      | Implementar integração inicial com WhatsApp Business.           |
| S3-09 | Implementar respostas automáticas para dúvidas frequentes | US-13                      | Criar mecanismo de FAQ automatizado para perguntas recorrentes. |

---

### Suelen — Integração e Qualidade

| ID    | Task                                                     | História(s) Relacionada(s) | Descrição                                                                 |
| ----- | -------------------------------------------------------- | -------------------------- | ------------------------------------------------------------------------- |
| S3-10 | Integrar telas de relatórios e despesas com APIs         | US-07, US-08               | Conectar as interfaces aos serviços disponibilizados pelo backend.        |
| S3-11 | Integrar tela de ranking com API de clientes             | US-10                      | Consumir os dados estatísticos dos clientes e exibi-los na interface.     |
| S3-12 | Criar testes de integração do chatbot e relatórios (TDD) | US-07, US-12, US-13        | Validar os fluxos completos entre frontend, backend e integração externa. |

---

## Relação com Product Backlog

| História | Descrição                                     | Tasks Relacionadas                |
| -------- | --------------------------------------------- | --------------------------------- |
| US-07    | Exportação de relatórios por período          | S3-01, S3-03, S3-04, S3-07, S3-10 |
| US-08    | Registro de despesas e saídas de caixa        | S3-02, S3-03, S3-05, S3-10        |
| US-10    | Ranking de clientes frequentes                | S3-06, S3-11                      |
| US-12    | Integração com WhatsApp                       | S3-08, S3-12                      |
| US-13    | Respostas automáticas para dúvidas frequentes | S3-09, S3-12                      |

---

## Estrutura Técnica Entregue

### Backend

* Serviço de exportação de relatórios
* Controle de despesas e saídas
* API de geração de PDF
* API de geração de Excel
* Integração inicial com WhatsApp
* Motor de respostas automáticas

### Frontend

* Tela de exportação de relatórios
* Tela de despesas operacionais
* Dashboard de ranking de clientes
* Integração com APIs financeiras

### Qualidade

* Testes unitários dos serviços financeiros
* Testes de integração dos relatórios
* Testes de integração do chatbot
* Cobertura de fluxos críticos

### CI/CD

* Stage Checkout
* Stage Build Front
* Stage Build Back
* Stage Test
* Stage Quality Gate
* Stage Deploy Homolog

---

## Distribuição por Membro

| Membro    | Papel            | Tasks        | Horas   |
| --------- | ---------------- | ------------ | ------- |
| Nicolas   | Backend          | 3            | 12h     |
| Bruna     | Frontend         | 3            | 12h     |
| Bruno     | API / Integração | 3            | 15h     |
| Suelen    | Full Stack / QA  | 3            | 11h     |
| **Total** |                  | **12 tasks** | **50h** |

---

## Entregáveis

* Exportação de relatórios em PDF
* Exportação de relatórios em Excel
* Controle de despesas e saídas de caixa
* Ranking de clientes frequentes
* Integração com WhatsApp Business
* Respostas automáticas para FAQ
* Testes automatizados
* Pipeline CI atualizado

---

## Observações Gerais

* Os relatórios devem permitir filtragem por período.
* Todas as despesas devem possuir categoria e descrição.
* A integração com WhatsApp deve seguir o fluxo oficial da API utilizada.
* Aplicar TDD nas tasks previstas.
* Garantir rastreabilidade das movimentações financeiras.
* Preparar a arquitetura para evolução do chatbot na Sprint 4.

---

## Revisão da Sprint

Durante a Sprint Review será realizada a demonstração das funcionalidades financeiras e da primeira versão do chatbot.

### Itens a demonstrar

* Geração de relatórios PDF
* Geração de relatórios Excel
* Registro de despesas
* Ranking de clientes
* Atendimento automatizado via WhatsApp
* Respostas automáticas para FAQ
* Integração frontend -> backend
* Execução dos testes automatizados
* Execução do pipeline CI

### Feedbacks Recebidos

> Resumo da Sprint Review e observações dos stakeholders.

---

## Retrospectiva

### O que funcionou bem?

*

### O que pode melhorar?

*

### Ações para a próxima sprint

* Implementar handoff chatbot -> vendedor.
* Criar painel administrativo do chatbot.
* Adicionar observações de clientes.
* Desenvolver consulta automática de disponibilidade de produtos.
* Preparar deploy final para produção.
* Reforçar cobertura de testes dos fluxos conversacionais.

---
