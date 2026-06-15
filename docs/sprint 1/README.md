# Sprint 1 — Base do Estoque

**Período:** 2 semanas

**Foco:** Importação de produtos via Excel, consulta de produtos, listagem de estoque e integração inicial entre frontend e backend.

---

## Objetivo da Sprint

Construir a primeira versão funcional do módulo de estoque, permitindo a importação de produtos por planilha Excel, consulta de produtos através de API, visualização do estoque disponível e integração completa entre frontend e backend.

Esta sprint estabelece toda a fundação necessária para os módulos de estoque, caixa e chatbot que serão desenvolvidos nas próximas entregas.

---

## Definition of Done

Uma task é considerada **Concluída** quando:

* Código commitado no repositório na branch `feat/nome-da-task`
* Pull Request aberto e aprovado por pelo menos um integrante
* Testes implementados e executados com sucesso
* Funcionalidade validada localmente
* Nenhum erro crítico de compilação ou tipagem
* Documentação atualizada quando necessário
* Cobertura de testes mantida conforme critérios do projeto
* Pipeline CI executando sem falhas

---

## Sprint Backlog

| ID    | Tarefa                                                  | Responsável | Horas | Status    |
| ----- | ------------------------------------------------------- | ----------- | ----- | --------- |
| S1-01 | Implementar backend da importação de produtos via Excel | Nicolas     | 6h    | Concluído |
| S1-02 | Desenvolver validações e mapeamento das colunas         | Nicolas     | 4h    | Concluído |
| S1-03 | Criar testes unitários da importação (TDD)              | Nicolas     | 3h    | Concluído |
| S1-04 | Criar tela de listagem de produtos                      | Bruna       | 5h    | Concluído |
| S1-05 | Implementar visualização de quantidade em estoque       | Bruna       | 3h    | Concluído |
| S1-06 | Criar testes dos componentes da listagem (TDD)          | Bruna       | 3h    | Concluído |
| S1-07 | Desenvolver API de consulta de produtos                 | Bruno       | 5h    | Concluído |
| S1-08 | Implementar filtros de busca por nome e categoria       | Bruno       | 3h    | Concluído |
| S1-09 | Criar testes unitários da consulta (TDD)                | Bruno       | 3h    | Concluído |
| S1-10 | Integrar frontend com API de produtos                   | Suelen      | 4h    | Concluído |
| S1-11 | Implementar paginação e atualização dos dados           | Suelen      | 3h    | Concluído |
| S1-12 | Criar testes de integração frontend -> backend (TDD)    | Suelen      | 4h    | Concluído |

---

## Detalhamento das Tasks

### Nicolas — Backend de Estoque

| ID    | Task                                                    | História(s) Relacionada(s) | Descrição                                                                                                            |
| ----- | ------------------------------------------------------- | -------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| S1-01 | Implementar backend da importação de produtos via Excel | US-01                      | Desenvolver endpoint responsável por receber arquivos Excel e processar o cadastro inicial dos produtos.             |
| S1-02 | Desenvolver validações e mapeamento das colunas         | US-01                      | Validar estrutura da planilha, campos obrigatórios e realizar o mapeamento correto das colunas para a base de dados. |
| S1-03 | Criar testes unitários da importação (TDD)              | US-01                      | Implementar testes cobrindo cenários válidos e inválidos do processo de importação.                                  |

---

### Bruna — Frontend de Estoque

| ID    | Task                                              | História(s) Relacionada(s) | Descrição                                                                        |
| ----- | ------------------------------------------------- | -------------------------- | -------------------------------------------------------------------------------- |
| S1-04 | Criar tela de listagem de produtos                | US-02                      | Desenvolver página principal para exibição dos produtos cadastrados no estoque.  |
| S1-05 | Implementar visualização de quantidade em estoque | US-02                      | Exibir quantidade disponível para cada produto e indicadores visuais de estoque. |
| S1-06 | Criar testes dos componentes da listagem (TDD)    | US-02                      | Implementar testes dos componentes visuais e comportamentos da listagem.         |

---

### Bruno — API de Consulta

| ID    | Task                                              | História(s) Relacionada(s) | Descrição                                                                          |
| ----- | ------------------------------------------------- | -------------------------- | ---------------------------------------------------------------------------------- |
| S1-07 | Desenvolver API de consulta de produtos           | US-02                      | Criar endpoints REST para consulta de produtos cadastrados.                        |
| S1-08 | Implementar filtros de busca por nome e categoria | US-02                      | Adicionar parâmetros de busca e filtragem para facilitar localização dos produtos. |
| S1-09 | Criar testes unitários da consulta (TDD)          | US-02                      | Garantir cobertura dos serviços e endpoints de consulta de produtos.               |

---

### Suelen — Integração e Qualidade

| ID    | Task                                                 | História(s) Relacionada(s) | Descrição                                                                 |
| ----- | ---------------------------------------------------- | -------------------------- | ------------------------------------------------------------------------- |
| S1-10 | Integrar frontend com API de produtos                | US-02                      | Conectar a interface de listagem aos endpoints disponibilizados pela API. |
| S1-11 | Implementar paginação e atualização dos dados        | US-02                      | Adicionar paginação, atualização dinâmica e sincronização de dados.       |
| S1-12 | Criar testes de integração frontend -> backend (TDD) | US-01, US-02               | Validar o fluxo completo entre interface, API e persistência dos dados.   |

---

## Relação com Product Backlog

| História | Descrição                                      | Tasks Relacionadas                                            |
| -------- | ---------------------------------------------- | ------------------------------------------------------------- |
| US-01    | Importação de produtos via Excel               | S1-01, S1-02, S1-03                                           |
| US-02    | Consulta e visualização de produtos em estoque | S1-04, S1-05, S1-06, S1-07, S1-08, S1-09, S1-10, S1-11, S1-12 |

---

## Estrutura Técnica Entregue

### Backend

* Endpoint de importação de produtos via Excel
* Serviço de validação das planilhas
* Mapeamento automático de colunas
* API REST de consulta de produtos
* Filtros por nome e categoria
* Testes unitários da camada de negócio

### Frontend

* Tela de listagem de produtos
* Exibição de estoque disponível
* Integração com API
* Paginação de resultados
* Atualização dinâmica dos dados
* Testes dos componentes

### Qualidade

* Testes unitários backend
* Testes unitários frontend
* Testes de integração
* Cobertura mínima definida pelo projeto

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
| Bruna     | Frontend         | 3            | 11h     |
| Bruno     | API / Integração | 3            | 11h     |
| Suelen    | Full Stack / QA  | 3            | 11h     |
| **Total** |                  | **12 tasks** | **46h** |

---

## Entregáveis

* Importação de produtos via Excel
* Validação de planilhas e mapeamento de colunas
* API de consulta de produtos
* Filtros por nome e categoria
* Tela de listagem de produtos
* Visualização do estoque disponível
* Integração frontend -> backend
* Paginação dos resultados
* Testes unitários backend
* Testes unitários frontend
* Testes de integração
* Pipeline CI executando build e testes

---

## Observações Gerais

* Utilizar Git Flow e branches no padrão `feat/nome-da-task`
* Aplicar TDD nas tasks de testes previstas
* Garantir separação entre camadas Controller -> Service -> Repository
* Manter cobertura mínima definida pelo projeto
* Toda nova funcionalidade deve possuir testes correspondentes
* Validar planilhas com tratamento adequado de erros
* Garantir compatibilidade da importação com arquivos Excel padrão (.xlsx)

---

## Revisão da Sprint

Durante a Sprint Review será realizada a demonstração do fluxo completo de importação e consulta de produtos.

### Itens a demonstrar

* Importação de planilha Excel
* Validação de dados inválidos
* Cadastro dos produtos no sistema
* Consulta dos produtos pela API
* Busca por nome e categoria
* Tela de listagem integrada
* Paginação dos resultados
* Execução dos testes automatizados
* Execução do pipeline de CI

### Feedbacks Recebidos

* A preencher durante a Sprint Review.

---

## Retrospectiva

### O que funcionou bem?

*

### O que pode melhorar?

*

### Ações para a próxima sprint

* Preparar a estrutura para alertas de estoque mínimo.
* Planejar ajustes manuais de estoque.
* Evoluir a API para suportar operações de venda.
* Preparar integração com módulo de caixa.
* Revisar cobertura de testes e pipeline de CI.

---
