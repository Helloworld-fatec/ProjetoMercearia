# Sprint 2 — Estoque + Caixa

**Período:** 2 semanas

**Foco:** Controle de estoque, ajustes manuais, alertas de estoque mínimo, cadastro de clientes, registro de vendas e faturamento diário.

---

## Objetivo da Sprint

Expandir o módulo de estoque implementado na Sprint 1 e iniciar o módulo de caixa, permitindo o controle de estoque mínimo, ajustes manuais de produtos, cadastro de clientes, registro de vendas e acompanhamento do faturamento diário.

A Sprint 2 estabelece a integração entre estoque e caixa, garantindo que as movimentações de venda atualizem automaticamente os saldos dos produtos e permitam o acompanhamento financeiro básico da operação.

---

## Definition of Done

Uma task é considerada **Concluída** quando:

* Código commitado no repositório na branch `feat/nome-da-task`
* Pull Request aprovado por pelo menos um integrante
* Testes automatizados implementados e aprovados
* Integração com backend e frontend validada
* Nenhum erro crítico de compilação, tipagem ou execução
* Cobertura mínima de testes mantida
* Pipeline CI executando sem falhas
* Documentação atualizada quando necessário

---

## Sprint Backlog

| ID    | Tarefa                                                           | Responsável | Horas | Status    |
| ----- | ---------------------------------------------------------------- | ----------- | ----- | --------- |
| S2-01 | Implementar serviço de alerta de estoque mínimo                  | Nicolas     | 5h    | Concluído |
| S2-02 | Criar lógica de ajuste manual de estoque (perda/devolução)       | Nicolas     | 5h    | Concluído |
| S2-03 | Criar testes unitários dos alertas e ajustes (TDD)               | Nicolas     | 3h    | Concluído |
| S2-04 | Criar tela de configuração de estoque mínimo                     | Bruna       | 4h    | Concluído |
| S2-05 | Criar tela de ajuste manual de estoque                           | Bruna       | 4h    | Concluído |
| S2-06 | Criar tela de cadastro de clientes                               | Bruna       | 4h    | Concluído |
| S2-07 | Desenvolver API de registro de vendas no caixa                   | Bruno       | 5h    | Concluído |
| S2-08 | Implementar atualização automática de estoque ao vender          | Bruno       | 4h    | Concluído |
| S2-09 | Desenvolver API de faturamento diário por pagamento              | Bruno       | 4h    | Concluído |
| S2-10 | Integrar tela de caixa com API de vendas                         | Suelen      | 4h    | Concluído |
| S2-11 | Integrar tela de faturamento com API de relatórios               | Suelen      | 4h    | Concluído |
| S2-12 | Criar testes de integração do caixa e cadastro de clientes (TDD) | Suelen      | 4h    | Concluído |

---

## Detalhamento das Tasks

### Nicolas — Backend de Estoque

| ID    | Task                                               | História(s) Relacionada(s) | Descrição                                                                                        |
| ----- | -------------------------------------------------- | -------------------------- | ------------------------------------------------------------------------------------------------ |
| S2-01 | Implementar serviço de alerta de estoque mínimo    | US-03                      | Desenvolver lógica responsável por identificar produtos abaixo da quantidade mínima configurada. |
| S2-02 | Criar lógica de ajuste manual de estoque           | US-04                      | Permitir registro de perdas, devoluções e correções de inventário com rastreabilidade.           |
| S2-03 | Criar testes unitários dos alertas e ajustes (TDD) | US-03, US-04               | Validar cenários de estoque mínimo, ajustes positivos e negativos.                               |

---

### Bruna — Frontend de Estoque e Clientes

| ID    | Task                                         | História(s) Relacionada(s) | Descrição                                                                 |
| ----- | -------------------------------------------- | -------------------------- | ------------------------------------------------------------------------- |
| S2-04 | Criar tela de configuração de estoque mínimo | US-03                      | Desenvolver interface para definição das quantidades mínimas por produto. |
| S2-05 | Criar tela de ajuste manual de estoque       | US-04                      | Desenvolver formulário para registro de perdas, devoluções e ajustes.     |
| S2-06 | Criar tela de cadastro de clientes           | US-09                      | Desenvolver tela de cadastro e manutenção dos clientes da empresa.        |

---

### Bruno — APIs de Caixa

| ID    | Task                                                    | História(s) Relacionada(s) | Descrição                                                                                |
| ----- | ------------------------------------------------------- | -------------------------- | ---------------------------------------------------------------------------------------- |
| S2-07 | Desenvolver API de registro de vendas no caixa          | US-05                      | Criar endpoint responsável por registrar vendas realizadas no sistema.                   |
| S2-08 | Implementar atualização automática de estoque ao vender | US-05                      | Garantir que toda venda reduza automaticamente o estoque dos produtos vendidos.          |
| S2-09 | Desenvolver API de faturamento diário por pagamento     | US-06                      | Disponibilizar informações consolidadas de faturamento agrupadas por forma de pagamento. |

---

### Suelen — Integração e Qualidade

| ID    | Task                                                             | História(s) Relacionada(s) | Descrição                                                                |
| ----- | ---------------------------------------------------------------- | -------------------------- | ------------------------------------------------------------------------ |
| S2-10 | Integrar tela de caixa com API de vendas                         | US-05                      | Conectar a interface de vendas aos endpoints de caixa.                   |
| S2-11 | Integrar tela de faturamento com API de relatórios               | US-06                      | Consumir os dados de faturamento e exibi-los na interface.               |
| S2-12 | Criar testes de integração do caixa e cadastro de clientes (TDD) | US-05, US-06, US-09        | Validar o fluxo completo entre cadastro, venda e atualização do estoque. |

---

## Relação com Product Backlog

| História | Descrição                                 | Tasks Relacionadas         |
| -------- | ----------------------------------------- | -------------------------- |
| US-03    | Controle de estoque mínimo                | S2-01, S2-03, S2-04        |
| US-04    | Ajuste manual de estoque                  | S2-02, S2-03, S2-05        |
| US-05    | Registro de vendas no caixa               | S2-07, S2-08, S2-10, S2-12 |
| US-06    | Faturamento diário por forma de pagamento | S2-09, S2-11, S2-12        |
| US-09    | Cadastro de clientes                      | S2-06, S2-12               |

---

## Estrutura Técnica Entregue

### Backend

* Serviço de alerta de estoque mínimo
* Controle de ajustes manuais
* Registro de perdas e devoluções
* API de vendas
* Atualização automática de estoque
* API de faturamento diário

### Frontend

* Tela de estoque mínimo
* Tela de ajuste de estoque
* Tela de cadastro de clientes
* Integração do módulo de caixa
* Integração dos relatórios financeiros

### Qualidade

* Testes unitários de estoque
* Testes unitários de ajustes
* Testes de integração de vendas
* Testes de integração de clientes

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
| Nicolas   | Backend          | 3            | 13h     |
| Bruna     | Frontend         | 3            | 12h     |
| Bruno     | API / Integração | 3            | 13h     |
| Suelen    | Full Stack / QA  | 3            | 12h     |
| **Total** |                  | **12 tasks** | **50h** |

---

## Entregáveis

* Controle de estoque mínimo
* Alertas de estoque baixo
* Ajustes manuais de estoque
* Registro de perdas e devoluções
* Cadastro de clientes
* API de vendas
* Atualização automática de estoque
* API de faturamento diário
* Integração das telas de caixa
* Integração dos relatórios financeiros
* Testes automatizados da sprint
* Pipeline CI atualizado

---

## Observações Gerais

* Toda venda deve atualizar o estoque automaticamente.
* Movimentações de estoque devem possuir histórico e rastreabilidade.
* Ajustes manuais devem registrar motivo da alteração.
* As APIs devem seguir o padrão REST definido pelo projeto.
* Aplicar TDD nas tasks previstas para testes.
* Validar regras de negócio antes da aprovação dos Pull Requests.
* Garantir compatibilidade com os módulos da Sprint 1.

---

## Revisão da Sprint

Durante a Sprint Review será realizada a demonstração da integração entre estoque e caixa.

### Itens a demonstrar

* Configuração de estoque mínimo
* Identificação de produtos abaixo do limite
* Ajuste manual de estoque
* Cadastro de clientes
* Registro de vendas
* Atualização automática do estoque
* Relatório de faturamento diário
* Integração frontend -> backend
* Execução dos testes automatizados
* Execução do pipeline CI

### Feedbacks Recebidos

* A preencher durante a Sprint Review.

---

## Retrospectiva

### O que funcionou bem?

*

### O que pode melhorar?

*

### Ações para a próxima sprint

* Iniciar módulo de relatórios.
* Implementar exportação de dados.
* Criar controle de despesas e saídas de caixa.
* Desenvolver ranking de clientes.
* Iniciar integração com WhatsApp.
* Evoluir cobertura dos testes automatizados.

---
