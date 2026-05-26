# Product Backlog — E-commerce + Chatbot WhatsApp

## 1. Contexto e Objetivos
Este backlog cobre o desenvolvimento de um sistema integrado de e-commerce e automação de atendimento via WhatsApp para uma loja. O objetivo central é eliminar o gargalo de atendimento manual — onde o vendedor responde as mesmas perguntas repetidamente — e centralizar o controle de estoque e caixa em um único sistema.

### Problema principal:
* Cliente não acha produto → desiste da compra → venda perdida.
* Vendedor gasta tempo com dúvidas repetitivas no WhatsApp.
* Estoque e caixa gerenciados no Excel, sem integração.

### Solução proposta:
E-commerce com catálogo, busca inteligente e checkout autônomo, integrado a um chatbot WhatsApp que tira dúvidas, mostra produtos e encaminha pedidos diretamente ao sistema.

---

## 2. Resumo do Backlog

| Épico | User Stories | Total Pontos | Sprints | Prioridade | Status |
| :--- | :---: | :---: | :---: | :---: | :---: |
| EP-01 Catálogo | 4 stories | 24 pts | S1–S2 | Alta | Não iniciado |
| EP-02 Checkout | 4 stories | 21 pts | S1–S3 | Alta | Não iniciado |
| EP-03 Estoque | 3 stories | 11 pts | S2–S3 | Alta | Não iniciado |
| EP-04 Caixa | 3 stories | 11 pts | S3–S4 | Média | Não iniciado |
| EP-05 Clientes | 3 stories | 10 pts | S2–S4 | Alta | Não iniciado |
| EP-06 Chatbot | 5 stories | 41 pts | S3–S4 | Alta | Não iniciado |
| **TOTAL** | **22 stories** | **118 pts** | **4 Sprints** | **—** | **—** |

---

## 3. Backlog Detalhado por Épico

### EP-01 — Catálogo de Produtos

| ID | User Story | Critérios de Aceite | Prior. | Esforço | Sprint |
| :--- | :--- | :--- | :---: | :---: | :---: |
| US-01 | Como admin, quero importar produtos do Excel para não precisar recadastrar tudo manualmente. | Upload de .xlsx; mapear colunas; importar nome, preço, estoque, foto. | Alta | 8 pts | S1 |
| US-02 | Como cliente, quero ver foto, preço e descrição do produto para decidir a compra. | Página de produto com galeria, preço destacado e estoque disponível. | Alta | 5 pts | S1 |
| US-03 | Como cliente, quero buscar produtos e receber sugestões similares para não desistir quando não achar. | Busca textual + fallback com sugestões de produtos relacionados. | Alta | 8 pts | S1 |
| US-04 | Como admin, quero categorizar produtos para facilitar a navegação do cliente. | CRUD de categorias; produto vinculado a uma ou mais categorias. | Média | 3 pts | S2 |

### EP-02 — Carrinho e Checkout

| ID | User Story | Critérios de Aceite | Prior. | Esforço | Sprint |
| :--- | :--- | :--- | :---: | :---: | :---: |
| US-05 | Como cliente, quero adicionar produtos ao carrinho e revisar antes de comprar. | Carrinho persistente; alterar quantidade; remover item; subtotal. | Alta | 5 pts | S1 |
| US-06 | Como cliente, quero calcular o frete antes de finalizar o pedido. | Frete grátis acima de R$150; abaixo disso, valor fixo por faixa de distância. | Alta | 5 pts | S2 |
| US-07 | Como cliente, quero finalizar meu pedido escolhendo forma de pagamento. | Suporte a Pix, cartão de crédito e boleto; confirmação por e-mail. | Alta | 8 pts | S2 |
| US-08 | Como cliente, quero ver o status do meu pedido após a compra. | Página de acompanhamento com status: recebido, em separação, saiu para entrega. | Média | 3 pts | S3 |

### EP-03 — Gestão de Estoque

| ID | User Story | Critérios de Aceite | Prior. | Esforço | Sprint |
| :--- | :--- | :--- | :---: | :---: | :---: |
| US-09 | Como admin, quero que o estoque baixe automaticamente ao confirmar uma venda. | Ao mudar status do pedido para 'confirmado', debitar quantidade vendida. | Alta | 5 pts | S2 |
| US-10 | Como admin, quero receber alerta quando um produto estiver acabando. | Notificação (e-mail/painel) quando estoque atingir quantidade mínima configurável. | Alta | 3 pts | S2 |
| US-11 | Como admin, quero ajustar o estoque manualmente em casos de devolução ou perda. | Formulário de ajuste de estoque com motivo obrigatório e log de histórico. | Média | 3 pts | S3 |

### EP-04 — Controle de Caixa

| ID | User Story | Critérios de Aceite | Prior. | Esforço | Sprint |
| :--- | :--- | :--- | :---: | :---: | :---: |
| US-12 | Como admin, quero ver o faturamento do dia agrupado por forma de pagamento. | Dashboard com total de vendas, ticket médio, formas de pagamento do dia. | Alta | 5 pts | S3 |
| US-13 | Como admin, quero exportar relatório de vendas por período. | Filtro por data; exportar CSV/Excel com pedidos, valor, forma de pagamento. | Média | 3 pts | S3 |
| US-14 | Como admin, quero registrar saídas de caixa (despesas) para ter saldo real. | Lançamento de despesas com categoria; saldo = entradas - saídas. | Média | 3 pts | S4 |

### EP-05 — Cadastro e Fidelização de Clientes

| ID | User Story | Critérios de Aceite | Prior. | Esforço | Sprint |
| :--- | :--- | :--- | :---: | :---: | :---: |
| US-15 | Como cliente, quero me cadastrar e ver meu histórico de compras. | Perfil com nome, contato, endereços e lista de pedidos anteriores. | Alta | 5 pts | S2 |
| US-16 | Como admin, quero ver um ranking de clientes que mais compram para fidelizá-los. | Lista ordenada por volume de compras; exportável; com último pedido e ticket médio. | Alta | 3 pts | S3 |
| US-17 | Como admin, quero adicionar tags/observações em clientes para personalizar o atendimento. | Campo de notas livre por cliente; visível apenas para o admin. | Baixa | 2 pts | S4 |

### EP-06 — Chatbot WhatsApp

| ID | User Story | Critérios de Aceite | Prior. | Esforço | Sprint |
| :--- | :--- | :--- | :---: | :---: | :---: |
| US-18 | Como cliente, quero consultar produtos disponíveis diretamente no WhatsApp. | Bot responde com lista de produtos, foto e preço ao receber mensagem de busca. | Alta | 13 pts | S3 |
| US-19 | Como cliente, quero tirar dúvidas frequentes sem precisar esperar o vendedor. | Bot responde: preço, prazo de entrega, formas de pagamento, horário de funcionamento. | Alta | 5 pts | S3 |
| US-20 | Como cliente, quero iniciar um pedido pelo WhatsApp e ter confirmado no sistema. | Pedido criado no bot já aparece no painel admin com estoque e caixa atualizados. | Alta | 13 pts | S4 |
| US-21 | Como vendedor, quero ser acionado pelo bot apenas em casos complexos. | Handoff automático: após 2 tentativas sem resposta adequada, transfere para humano. | Alta | 5 pts | S4 |
| US-22 | Como admin, quero configurar as respostas automáticas do bot sem precisar de programação. | Painel para editar perguntas frequentes e respostas do bot. | Média | 5 pts | S4 |

---

## 4. Planejamento de Sprints
*Sugestão de distribuição considerando sprints de 2 semanas (8 semanas no total para MVP completo).*

| Sprint | Foco | User Stories | Pontos | Entrega Esperada |
| :--- | :--- | :--- | :---: | :--- |
| **Sprint 1** | Base do catálogo e carrinho | US-01 a US-03, US-05 | 26 pts | Catálogo navegável com busca e carrinho funcional |
| **Sprint 2** | Checkout, frete, estoque e clientes | US-04, US-06, US-07, US-09, US-10, US-15 | 29 pts | Cliente consegue comprar de ponta a ponta; estoque baixa automaticamente |
| **Sprint 3** | Caixa, fidelização e chatbot básico | US-08, US-11, US-12, US-13, US-16, US-18, US-19 | 25 pts | Dashboard de caixa + bot respondendo no WhatsApp |
| **Sprint 4** | Chatbot completo e refinamentos | US-14, US-17, US-20, US-21, US-22 | 28 pts | Bot processa pedidos; handoff para vendedor; controle total do caixa |

---

## 5. Definition of Done (Definição de Pronto)
Uma User Story é considerada pronta quando:
* Funcionalidade implementada e testada pelo desenvolvedor.
* Critérios de aceite validados com o Product Owner.
* Código revisado e integrado à branch principal.
* Sem erros críticos em ambiente de homologação.
* Documentação de uso atualizada (se aplicável).

---

## 6. Considerações Técnicas

### Integrações necessárias:
* API WhatsApp Business (Meta) ou provedor como Twilio / Z-API para o chatbot.
* Gateway de pagamento (ex: Stripe, PagSeguro, Mercado Pago) para Pix, cartão e boleto.
* API de frete ou tabela configurável para calcular valor de entrega por Uber/motoboy.

### Premissas:
* O dono da loja possui conta verificada no WhatsApp Business.
* Os produtos do Excel estão minimamente padronizados (nome, preço, estoque, foto).
* A equipe de desenvolvimento tem acesso às APIs citadas acima.

### Riscos:
* Integração WhatsApp (EP-06) é a parte mais complexa e instável — priorizar POC no início da Sprint 3.
* Busca inteligente (US-03) pode exigir ajuste fino — reservar tempo para refinamento.



# Sprint Planning — Sprint 1

## Informações Gerais

**Projeto:** E-commerce + Chatbot WhatsApp  
**Sprint:** Sprint 1  
**Duração:** 2 semanas  
**Objetivo da Sprint:** Desenvolver a base funcional do catálogo de produtos e do carrinho de compras, permitindo navegação, busca e importação inicial de produtos.

---

## Objetivo da Sprint

A Sprint 1 tem como foco a construção do **MVP inicial do e-commerce**, entregando funcionalidades essenciais para que o cliente consiga visualizar produtos, pesquisar itens e iniciar o processo de compra através do carrinho.

### Funcionalidades Prioritárias
- Importação de produtos via Excel
- Página de produto
- Busca inteligente de produtos
- Carrinho de compras funcional

---

## User Stories Selecionadas

| ID | User Story | Prioridade | Esforço |
|----|------------|------------|----------|
| US-01 | Como admin, quero importar produtos do Excel para não precisar cadastrar tudo manualmente | Alta | 8 pts |
| US-02 | Como cliente, quero ver foto, preço e descrição do produto para decidir a compra | Alta | 5 pts |
| US-03 | Como cliente, quero buscar produtos e receber sugestões similares para não desistir da compra | Alta | 8 pts |
| US-05 | Como cliente, quero adicionar produtos ao carrinho e revisar antes de comprar | Alta | 5 pts |

**Total da Sprint:** **26 Story Points**

---

## Planejamento das Tasks

### Nicolas
Responsável pela funcionalidade de importação de produtos.

| Task ID | Descrição | Story |
|----------|------------|--------|
| T1 | Implementar backend da importação de produtos via Excel (.xlsx) | US-01 |
| T2 | Desenvolver validações e mapeamento das colunas do Excel | US-01 |
| T3 (TDD) | Criar testes unitários da importação | US-01 |

### Bruna
Responsável pela página de produto.

| Task ID | Descrição | Story |
|----------|------------|--------|
| T4 | Criar interface da página do produto | US-02 |
| T5 | Implementar galeria de imagens e atualização de estoque | US-02 |
| T6 (TDD) | Criar testes unitários dos componentes da página | US-02 |

### Bruno
Responsável pela busca inteligente.

| Task ID | Descrição | Story |
|----------|------------|--------|
| T7 | Desenvolver sistema de busca textual | US-03 |
| T8 | Implementar sugestão de produtos similares | US-03 |
| T9 (TDD) | Criar testes unitários da busca | US-03 |

### Suelen
Responsável pelo carrinho de compras.

| Task ID | Descrição | Story |
|----------|------------|--------|
| T10 | Implementar adicionar/remover itens do carrinho | US-05 |
| T11 | Criar persistência do carrinho e subtotal | US-05 |
| T12 (TDD) | Criar testes unitários do carrinho | US-05 |

---

## Estratégia de Desenvolvimento

A equipe adotará **TDD (Test-Driven Development)** durante toda a sprint.

### Fluxo de trabalho:
1. **Red** → escrever o teste antes da implementação.  
2. **Green** → desenvolver o mínimo necessário para passar no teste.  
3. **Refactor** → melhorar o código mantendo os testes aprovados.

---

## Capacidade da Equipe

| Desenvolvedor | Quantidade de Tasks |
|----------------|---------------------|
| Nicolas | 3 |
| Bruna | 3 |
| Bruno | 3 |
| Suelen | 3 |

**Total de Tasks:** **12**

Distribuição equilibrada para garantir paralelismo no desenvolvimento e reduzir gargalos.

---

## Riscos Identificados

### R1 — Problemas na importação do Excel
**Impacto:** Alto  
**Mitigação:** Criar validações de formato e testes unitários.

### R2 — Busca retornar poucos resultados relevantes
**Impacto:** Médio  
**Mitigação:** Implementar sugestões similares como fallback.

### R3 — Persistência do carrinho apresentar inconsistências
**Impacto:** Médio  
**Mitigação:** Criar testes cobrindo fluxo completo do carrinho.

---

## Critérios de Sucesso da Sprint

A Sprint 1 será considerada bem-sucedida se:

- [x] Produtos forem importados corretamente via Excel  
- [x] Página do produto estiver funcional  
- [x] Busca retornar produtos e sugestões similares  
- [x] Carrinho permitir adicionar/remover itens  
- [x] Subtotal for calculado corretamente  
- [x] Todos os testes unitários estiverem aprovados  
- [x] Código integrado sem erros críticos

---

## Entrega Esperada

Ao final da Sprint 1, será entregue um **catálogo navegável com busca e carrinho funcional**, formando a base do MVP do e-commerce.



# Sprint Backlog — Sprint 1

## Objetivo da Sprint
Entregar a base funcional do catálogo e carrinho do e-commerce, incluindo:

- Importação de produtos via Excel
- Página de produto funcional
- Busca de produtos com sugestões
- Carrinho de compras funcional

**User Stories da Sprint:**
- US-01 — Importação de produtos via Excel
- US-02 — Página de produto
- US-03 — Busca inteligente
- US-05 — Carrinho de compras

---

## Distribuição das Tasks

| Dev | Task ID | Task | User Story |
|------|---------|------|-------------|
| Nicolas | T1 | Implementar backend da importação de produtos via Excel (.xlsx), incluindo leitura do arquivo e persistência no banco | US-01 |
| Nicolas | T2 | Criar lógica de mapeamento de colunas do Excel (nome, preço, estoque e imagem) e validações da importação | US-01 |
| Nicolas | T3 (TDD) | Criar testes unitários da importação de Excel (arquivo válido, inválido e validação de campos obrigatórios) | US-01 |
| Bruna | T4 | Desenvolver interface da página do produto (imagem, descrição, preço e disponibilidade) | US-02 |
| Bruna | T5 | Implementar galeria de imagens e atualização dinâmica do estoque na tela do produto | US-02 |
| Bruna | T6 (TDD) | Criar testes unitários dos componentes da página do produto e renderização de dados | US-02 |
| Bruno | T7 | Desenvolver sistema de busca textual de produtos no catálogo | US-03 |
| Bruno | T8 | Implementar sugestão de produtos similares quando não houver resultado na busca | US-03 |
| Bruno | T9 (TDD) | Criar testes unitários da busca (produto encontrado, não encontrado e sugestões similares) | US-03 |
| Suelen | T10 | Implementar funcionalidade do carrinho (adicionar, remover e alterar quantidade de produtos) | US-05 |
| Suelen | T11 | Desenvolver persistência do carrinho e cálculo automático do subtotal | US-05 |
| Suelen | T12 (TDD) | Criar testes unitários do carrinho (adição, remoção, persistência e subtotal) | US-05 |

---

## Estratégia de Desenvolvimento — TDD

A sprint seguirá o modelo **TDD (Test-Driven Development)**:

### 1. Red
Criar o teste unitário antes da implementação da funcionalidade.

### 2. Green
Implementar o mínimo necessário para que o teste passe.

### 3. Refactor
Refatorar o código mantendo todos os testes funcionando.

---

## Critérios de Pronto (Definition of Done)

Uma task será considerada concluída quando:

- Funcionalidade implementada
- Testes unitários criados e aprovados
- Código revisado pela equipe
- Sem erros críticos
- Integrado à branch principal
- Critérios de aceite da User Story atendidos

---

## Entrega Esperada da Sprint 1

Ao final da Sprint 1 o sistema deverá possuir:

✅ Importação de produtos via Excel funcionando  
✅ Catálogo navegável com página de produto  
✅ Busca de produtos com sugestões similares  
✅ Carrinho funcional com subtotal automático  
✅ Testes unitários implementados seguindo TDD  
