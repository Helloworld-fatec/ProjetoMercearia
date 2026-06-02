# Product Backlog — Controle de Estoque + Sistema de Caixa + Chatbot WhatsApp

## 1. Contexto e Objetivos

Este backlog cobre o desenvolvimento de um sistema integrado de controle de estoque, gestão de caixa (PDV) e automação de atendimento via WhatsApp para uma loja.

O objetivo central é eliminar o atendimento repetitivo realizado pelo vendedor, centralizar o controle de estoque e caixa e automatizar consultas de produtos e informações da loja.

### Problema principal

* Vendedor gasta tempo respondendo as mesmas dúvidas no WhatsApp.
* Estoque controlado em planilhas sem atualização automática.
* Caixa controlado manualmente, dificultando a visão financeira da operação.

### Solução proposta

Sistema integrado de estoque e caixa com chatbot WhatsApp capaz de consultar produtos disponíveis, responder dúvidas frequentes e encaminhar atendimentos complexos para um vendedor.

---

# 2. Resumo do Backlog

| Épico                      | User Stories | Total Pontos | Sprints   | Prioridade |
| -------------------------- | ------------ | ------------ | --------- | ---------- |
| EP-01 Gestão de Estoque    | 4 stories    | 19 pts       | S1-S2     | Alta       |
| EP-02 Controle de Caixa    | 4 stories    | 16 pts       | S2-S3     | Alta       |
| EP-03 Cadastro de Clientes | 3 stories    | 10 pts       | S2-S3     | Média      |
| EP-04 Chatbot WhatsApp     | 5 stories    | 41 pts       | S3-S4     | Alta       |
| TOTAL                      | 16 stories   | 86 pts       | 4 Sprints | —          |

---

# 3. Backlog Detalhado

## EP-01 — Gestão de Estoque

| ID    | User Story                                                                                | Prioridade | Esforço |
| ----- | ----------------------------------------------------------------------------------------- | ---------- | ------- |
| US-01 | Como admin, quero importar produtos do Excel para não precisar cadastrar tudo manualmente | Alta       | 8 pts   |
| US-02 | Como admin, quero consultar os produtos cadastrados com quantidade disponível             | Alta       | 5 pts   |
| US-03 | Como admin, quero receber alerta quando um produto estiver acabando                       | Alta       | 3 pts   |
| US-04 | Como admin, quero ajustar estoque manualmente em casos de perda ou devolução              | Média      | 3 pts   |

---

## EP-02 — Controle de Caixa

| ID    | User Story                                                                                       | Prioridade | Esforço |
| ----- | ------------------------------------------------------------------------------------------------ | ---------- | ------- |
| US-05 | Como operador, quero registrar vendas no sistema de caixa para atualizar estoque automaticamente | Alta       | 5 pts   |
| US-06 | Como admin, quero visualizar faturamento diário por forma de pagamento                           | Alta       | 5 pts   |
| US-07 | Como admin, quero exportar relatórios de vendas por período                                      | Média      | 3 pts   |
| US-08 | Como admin, quero registrar despesas e saídas de caixa para controlar o saldo real               | Média      | 3 pts   |

---

## EP-03 — Cadastro de Clientes

| ID    | User Story                                                                   | Prioridade | Esforço |
| ----- | ---------------------------------------------------------------------------- | ---------- | ------- |
| US-09 | Como operador, quero cadastrar clientes para associar compras e atendimentos | Alta       | 5 pts   |
| US-10 | Como admin, quero visualizar ranking de clientes mais frequentes             | Média      | 3 pts   |
| US-11 | Como admin, quero registrar observações sobre clientes                       | Baixa      | 2 pts   |

---

## EP-04 — Chatbot WhatsApp

| ID    | User Story                                                                                 | Prioridade | Esforço |
| ----- | ------------------------------------------------------------------------------------------ | ---------- | ------- |
| US-12 | Como cliente, quero consultar produtos disponíveis pelo WhatsApp                           | Alta       | 13 pts  |
| US-13 | Como cliente, quero tirar dúvidas frequentes sem depender do vendedor                      | Alta       | 5 pts   |
| US-14 | Como cliente, quero consultar disponibilidade de um produto pelo WhatsApp                  | Alta       | 8 pts   |
| US-15 | Como vendedor, quero ser acionado apenas quando o bot não conseguir resolver o atendimento | Alta       | 5 pts   |
| US-16 | Como admin, quero configurar respostas automáticas sem programação                         | Média      | 10 pts  |

---

# 4. Planejamento de Sprints

| Sprint   | Foco                              | User Stories                      | Pontos |
| -------- | --------------------------------- | --------------------------------- | ------ |
| Sprint 1 | Base do Estoque                   | US-01, US-02                      | 13 pts |
| Sprint 2 | Estoque + Caixa                   | US-03, US-04, US-05, US-06, US-09 | 21 pts |
| Sprint 3 | Caixa + Clientes + Chatbot Básico | US-07, US-08, US-10, US-12, US-13 | 29 pts |
| Sprint 4 | Chatbot Completo                  | US-11, US-14, US-15, US-16        | 23 pts |

---

# Sprint Planning — Sprint 1

## Informações Gerais

**Projeto:** Controle de Estoque + Sistema de Caixa + Chatbot WhatsApp

**Sprint:** Sprint 1

**Duração:** 2 semanas

## Objetivo da Sprint

Construir a base do módulo de estoque permitindo o cadastro em massa de produtos e a consulta dos itens disponíveis.

### Funcionalidades Prioritárias

* Importação de produtos via Excel
* Consulta de produtos cadastrados
* Visualização de estoque disponível

---

## User Stories Selecionadas

| ID    | User Story                                            | Prioridade | Esforço |
| ----- | ----------------------------------------------------- | ---------- | ------- |
| US-01 | Importação de produtos via Excel                      | Alta       | 8 pts   |
| US-02 | Consulta de produtos cadastrados e estoque disponível | Alta       | 5 pts   |

**Total da Sprint:** 13 Story Points

---

## Planejamento das Tasks

### Nicolas

| Task ID  | Descrição                                               |
| -------- | ------------------------------------------------------- |
| T1       | Implementar backend da importação de produtos via Excel |
| T2       | Desenvolver validações e mapeamento das colunas         |
| T3 (TDD) | Criar testes unitários da importação                    |

### Bruna

| Task ID  | Descrição                                         |
| -------- | ------------------------------------------------- |
| T4       | Criar tela de listagem de produtos                |
| T5       | Implementar visualização de quantidade em estoque |
| T6 (TDD) | Criar testes dos componentes da listagem          |

### Bruno

| Task ID  | Descrição                                         |
| -------- | ------------------------------------------------- |
| T7       | Desenvolver API de consulta de produtos           |
| T8       | Implementar filtros de busca por nome e categoria |
| T9 (TDD) | Criar testes unitários da consulta                |

### Suelen

| Task ID   | Descrição                                     |
| --------- | --------------------------------------------- |
| T10       | Integrar frontend com API de produtos         |
| T11       | Implementar paginação e atualização dos dados |
| T12 (TDD) | Criar testes de integração                    |

---

## Critérios de Sucesso

* Produtos importados corretamente via Excel
* Consulta de produtos funcionando
* Visualização do estoque disponível
* Filtros de busca funcionando
* Testes unitários aprovados
* Código integrado sem erros críticos

---

# Sprint Backlog — Sprint 1

## Objetivo da Sprint

Entregar a base funcional do módulo de estoque.

### User Stories

* US-01 — Importação de produtos via Excel
* US-02 — Consulta de produtos cadastrados

---

## Distribuição das Tasks

| Dev     | Task ID | Task                                           |
| ------- | ------- | ---------------------------------------------- |
| Nicolas | T1      | Implementar backend da importação de Excel     |
| Nicolas | T2      | Desenvolver mapeamento de colunas e validações |
| Nicolas | T3      | Criar testes unitários da importação           |
| Bruna   | T4      | Criar interface de listagem de produtos        |
| Bruna   | T5      | Implementar exibição do estoque disponível     |
| Bruna   | T6      | Criar testes da interface                      |
| Bruno   | T7      | Desenvolver API de consulta de produtos        |
| Bruno   | T8      | Implementar filtros de pesquisa                |
| Bruno   | T9      | Criar testes unitários da consulta             |
| Suelen  | T10     | Integrar frontend e backend                    |
| Suelen  | T11     | Implementar paginação                          |
| Suelen  | T12     | Criar testes de integração                     |

---

## Entrega Esperada

Ao final da Sprint 1 o sistema deverá possuir:

✅ Importação de produtos via Excel funcionando

✅ Consulta de produtos cadastrados

✅ Visualização do estoque disponível

✅ Filtros de busca

✅ Testes implementados seguindo TDD
