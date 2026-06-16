# 📦 Product Backlog — Controle de Estoque + Sistema de Caixa + Chatbot WhatsApp

## 📋 Contexto e Objetivos

Sistema integrado de controle de estoque, gestão de caixa (PDV) e automação de atendimento via WhatsApp para uma loja.

O objetivo central é **eliminar o atendimento repetitivo** realizado pelo vendedor, centralizar o controle de estoque e caixa e automatizar consultas de produtos e informações da loja.

**Problemas que resolve:**
- Vendedor gasta tempo respondendo as mesmas dúvidas no WhatsApp
- Estoque controlado em planilhas sem atualização automática
- Caixa controlado manualmente, dificultando a visão financeira da operação

---

## 👥 Equipe

| Membro | Função | Responsabilidades |
|--------|--------|-------------------|
| Pedro | Product-Owner | Maximixar os valores e o trabalho em equipe durante o desenvolvimento |
| Ryan | Scrum Master | Garantir o flow do projeto com a metodologia Scrum com o uso do Git e do Trello |
| Nicolas | Dev Backend | Importação Excel, validações, testes unitários |
| Bruna | Dev Frontend | Interfaces, componentes UI, testes de interface |
| Bruno | Dev Backend / API | APIs, filtros de busca, testes unitários |
| Suelen | Dev Full Stack / QA | Integração frontend-backend, paginação, testes de integração |

---

## 📊 Resumo do Backlog

| Épico | User Stories | Total Pontos | Sprints | Prioridade |
|-------|-------------|-------------|---------|-----------|
| EP-01 Gestão de Estoque | 4 stories | 19 pts | S1-S2 | 🔴 Alta |
| EP-02 Controle de Caixa | 4 stories | 16 pts | S2-S3 | 🔴 Alta |
| EP-03 Cadastro de Clientes | 3 stories | 10 pts | S2-S3 | 🟡 Média |
| EP-04 Chatbot WhatsApp | 5 stories | 41 pts | S3-S4 | 🔴 Alta |
| **TOTAL** | **16 stories** | **86 pts** | **4 Sprints** | — |

---

## 📝 Backlog Detalhado

### EP-01 — Gestão de Estoque

| ID | User Story | Prioridade | Esforço |
|----|-----------|-----------|---------|
| US-01 | Como admin, quero importar produtos do Excel para não precisar cadastrar tudo manualmente | 🔴 Alta | 8 pts |
| US-02 | Como admin, quero consultar os produtos cadastrados com quantidade disponível | 🔴 Alta | 5 pts |
| US-03 | Como admin, quero receber alerta quando um produto estiver acabando | 🔴 Alta | 3 pts |
| US-04 | Como admin, quero ajustar estoque manualmente em casos de perda ou devolução | 🟡 Média | 3 pts |

### EP-02 — Controle de Caixa

| ID | User Story | Prioridade | Esforço |
|----|-----------|-----------|---------|
| US-05 | Como operador, quero registrar vendas no sistema de caixa para atualizar estoque automaticamente | 🔴 Alta | 5 pts |
| US-06 | Como admin, quero visualizar faturamento diário por forma de pagamento | 🔴 Alta | 5 pts |
| US-07 | Como admin, quero exportar relatórios de vendas por período | 🟡 Média | 3 pts |
| US-08 | Como admin, quero registrar despesas e saídas de caixa para controlar o saldo real | 🟡 Média | 3 pts |

### EP-03 — Cadastro de Clientes

| ID | User Story | Prioridade | Esforço |
|----|-----------|-----------|---------|
| US-09 | Como operador, quero cadastrar clientes para associar compras e atendimentos | 🔴 Alta | 5 pts |
| US-10 | Como admin, quero visualizar ranking de clientes mais frequentes | 🟡 Média | 3 pts |
| US-11 | Como admin, quero registrar observações sobre clientes | 🟢 Baixa | 2 pts |

### EP-04 — Chatbot WhatsApp

| ID | User Story | Prioridade | Esforço |
|----|-----------|-----------|---------|
| US-12 | Como cliente, quero consultar produtos disponíveis pelo WhatsApp | 🔴 Alta | 13 pts |
| US-13 | Como cliente, quero tirar dúvidas frequentes sem depender do vendedor | 🔴 Alta | 5 pts |
| US-14 | Como cliente, quero consultar disponibilidade de um produto pelo WhatsApp | 🔴 Alta | 8 pts |
| US-15 | Como vendedor, quero ser acionado apenas quando o bot não conseguir resolver o atendimento | 🔴 Alta | 5 pts |
| US-16 | Como admin, quero configurar respostas automáticas sem programação | 🟡 Média | 10 pts |

---

## 🗓️ Planejamento de Sprints

| Sprint | Foco | User Stories | Pontos | Documento |
|--------|------|-------------|--------|-----------|
| Sprint 1 | Base do Estoque | US-01, US-02 | 13 pts | [📄 Ver Sprint 1](./docs/sprint-1/README.md) |
| Sprint 2 | Estoque + Caixa | US-03, US-04, US-05, US-06, US-09 | 21 pts | [📄 Ver Sprint 2](./docs/sprint-2/README.md) |
| Sprint 3 | Caixa + Clientes + Chatbot Básico | US-07, US-08, US-10, US-12, US-13 | 29 pts | [📄 Ver Sprint 3](./docs/sprint-3/README.md) |
| Sprint 4 | Chatbot Completo | US-11, US-14, US-15, US-16 | 23 pts | [📄 Ver Sprint 4](./docs/sprint-4/README.md) |
