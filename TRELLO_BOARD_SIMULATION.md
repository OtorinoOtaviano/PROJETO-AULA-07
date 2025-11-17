# Simulação de Quadro Trello - Sistema de Barbearia

## Estrutura do Quadro

Este documento simula um quadro Trello completo para um projeto de sistema de agendamento para barbearia, seguindo metodologias Ágeis (Scrum).

---

## 📋 Colunas do Quadro

### 1️⃣ Product Backlog
### 2️⃣ Sprint 1 Backlog
### 3️⃣ Em Progresso
### 4️⃣ Revisão de Código
### 5️⃣ Teste
### 6️⃣ Concluído Sprint 1
### 7️⃣ Melhorias da Retrospectiva

---

## 📝 Cartões do Product Backlog

### 🎯 Épico 1: Agendamento

#### Cartão 1: [Cliente] Ver horários disponíveis
**Título:** [Cliente] Como Cliente, eu quero ver os horários disponíveis de um barbeiro específico, para poder agendar um serviço.

**Prioridade:** Alta ⚠️

**Status:** Product Backlog

---

#### Cartão 2: [Cliente] Notificação de confirmação
**Título:** [Cliente] Como Cliente, eu quero receber uma notificação de confirmação após agendar...

**Prioridade:** Alta ⚠️

**Status:** Product Backlog

---

#### Cartão 3: [Barbeiro] Ver agenda
**Título:** [Barbeiro] Como Barbeiro, eu quero ver minha agenda do dia/semana...

**Prioridade:** Média 🔶

**Status:** Product Backlog

---

#### Cartão 4: [Cliente] Cancelar/Reagendar
**Título:** [Cliente] Como Cliente, eu quero poder cancelar ou reagendar um horário...

**Prioridade:** Média 🔶

**Status:** Product Backlog

---

#### Cartão 5: [Barbeiro] Bloquear horários
**Título:** [Barbeiro] Como Barbeiro, eu quero poder bloquear horários na minha agenda (ex: almoço)...

**Prioridade:** Média 🔶 → **Alta ⚠️ (após Sprint Review 1)**

**Status:** Product Backlog

---

### 💰 Épico 2: Financeiro

#### Cartão 6: [Barbeiro] Registrar serviços
**Título:** [Barbeiro] Como Barbeiro, eu quero registrar cada serviço prestado no app...

**Prioridade:** Alta ⚠️

**Status:** Product Backlog

---

#### Cartão 7: [Dono] Relatório de faturamento
**Título:** [Dono] Como Dono, eu quero ver um relatório simples de faturamento (dia, semana, mês)...

**Prioridade:** Média 🔶

**Status:** Product Backlog

---

#### Cartão 8: [Dono] Registrar despesas
**Título:** [Dono] Como Dono, eu quero registrar despesas simples...

**Prioridade:** Baixa 🔵

**Status:** Product Backlog

---

### 👥 Épico 3: Gestão de Clientes/Admin

#### Cartão 9: [Cliente] Cadastro/Login
**Título:** [Cliente] Como Cliente, eu quero fazer um cadastro/login simples...

**Prioridade:** Alta ⚠️

**Status:** Product Backlog

---

#### Cartão 10: [Dono] Cadastro de clientes
**Título:** [Dono] Como Dono, eu quero ter um cadastro dos meus clientes...

**Prioridade:** Média 🔶

**Status:** Product Backlog

---

#### Cartão 11: [Dono] Cadastrar barbeiros
**Título:** [Dono] Como Dono, eu quero cadastrar os barbeiros que trabalham comigo...

**Prioridade:** Média 🔶

**Status:** Product Backlog

---

## 🎯 Cartão de Feature Detalhado (Sprint 1)

### [Cliente] Ver horários disponíveis de um barbeiro específico

**Status:** ✅ Concluído Sprint 1

**Etiquetas:**
- 🟢 Nova Funcionalidade
- 🔵 UX/UI
- 🟡 Sprint 1
- 🔴 Prioridade Alta

**Descrição:**
Como cliente, eu preciso visualizar os horários disponíveis de um barbeiro específico para poder agendar um serviço de forma conveniente.

**Checklist de Implementação:**
- ✅ Desenvolver tela (front-end) de seleção de barbeiros
- ✅ Criar componente de calendário (front-end)
- ✅ Criar API (back-end) que busca horários livres
- ✅ Integrar front-end com a API
- ✅ Testar unitariamente a API
- ✅ Testar interface (responsividade)

**Comentários (Simulação de Daily Scrum):**

💬 **Dev Frontend (Dia 1):** "Comecei a desenvolver a tela de seleção de barbeiros. Dúvida: Como mostramos quando um barbeiro não tem horários disponíveis?"

💬 **PO (Resposta):** "Boa pergunta. Vamos mostrar 'Sem horários disponíveis para este dia' e um botão 'Ver próximo dia livre'. Mais rápido de implementar."

💬 **Dev Backend (Dia 2):** "API de horários livres pronta. Retorna slots de 30 minutos. Preciso de review."

💬 **Scrum Master (Dia 3):** "Integração front-back em andamento. No caminho certo!"

💬 **QA (Dia 4):** "Testes de responsividade concluídos. Funciona bem em mobile e desktop. ✅"

**Fluxo no Quadro:**
Sprint 1 Backlog → Em Progresso → Revisão de Código → Teste → Concluído Sprint 1

---

## 🐛 Cartão de Bug Crítico (Sprint 1)

### [BUG CRÍTICO] Usuários não conseguem resetar a senha

**Status:** ✅ Concluído Sprint 1

**Etiquetas:**
- 🔴 BUG
- ⚫ Prioridade CRÍTICA
- 🟡 Sprint 1

**Descrição:**

**O que aconteceu:** 
E-mail de "reset de senha" não está a ser enviado.

**Passos para reproduzir:**
1. Clicar em "Esqueci senha"
2. Digitar e-mail
3. Clicar em "Enviar"

**Resultado Esperado:** 
Receber e-mail com link de reset

**Resultado Atual:** 
Nada acontece. API de e-mail quebrada.

**Impacto:** 
Usuários bloqueados não conseguem acessar o sistema.

**Checklist de Correção:**
- ✅ Investigar logs da API de e-mail
- ✅ Corrigir chave de autenticação da API
- ✅ Disparar teste de envio
- ✅ Enviar para Teste QA
- ✅ Validado em produção

**Comentários:**

💬 **Dev Backend:** "Encontrei o problema! A chave de API do serviço de e-mail expirou. Atualizando credenciais."

💬 **Dev Backend:** "Correção aplicada. Testando localmente... OK! Enviando para QA."

💬 **QA:** "Testei com 5 e-mails diferentes. Todos receberam o link de reset em menos de 1 minuto. ✅ APROVADO"

**Fluxo no Quadro:**
Sprint 1 Backlog → Em Progresso → Revisão de Código → Teste → Concluído Sprint 1

---

## 📊 Estado Final do Quadro (Após Sprint 1)

### 1️⃣ Product Backlog
- [Cliente] Notificação de confirmação (Alta)
- [Barbeiro] Ver agenda (Média)
- [Cliente] Cancelar/Reagendar (Média)
- [Barbeiro] Bloquear horários (Média → Alta após Review)
- [Barbeiro] Registrar serviços (Alta)
- [Dono] Relatório de faturamento (Média)
- [Dono] Registrar despesas (Baixa)
- [Cliente] Cadastro/Login (Alta)
- [Dono] Cadastro de clientes (Média)
- [Dono] Cadastrar barbeiros (Média)

**Total: 10 cartões**

---

### 2️⃣ Sprint 1 Backlog
**(VAZIA - Sprint concluída)**

---

### 3️⃣ Em Progresso
**(VAZIA)**

---

### 4️⃣ Revisão de Código
**(VAZIA)**

*Esta coluna prova que aplicamos a melhoria da Retrospectiva!*

---

### 5️⃣ Teste
**(VAZIA)**

---

### 6️⃣ Concluído Sprint 1
✅ **5 cartões concluídos:**

1. [Cliente] Ver horários disponíveis (Feature)
2. [Cliente] Notificação de confirmação (Feature)
3. [Barbeiro] Registrar serviços (Feature)
4. [Cliente] Cadastro/Login (Feature)
5. [BUG CRÍTICO] Usuários não conseguem resetar a senha (Bug Fix)

**Velocity da Sprint 1:** 21 Story Points

---

### 7️⃣ Melhorias da Retrospectiva

#### 🎯 [AÇÃO] Implementar Code Review Obrigatório

**Contexto da Retrospectiva:**
Durante a retrospectiva da Sprint 1, a equipe identificou que alguns bugs poderiam ter sido evitados com revisão de código. O bug crítico de reset de senha, por exemplo, foi causado por credenciais hardcoded que expiraram.

**Decisão da Equipe:**
Implementar processo obrigatório de Code Review antes de mover qualquer cartão para a coluna de "Teste".

**Ação Concreta:**
- ✅ Criar coluna "Revisão de Código" no quadro Trello
- ✅ Definir que ao menos 1 desenvolvedor deve revisar o código
- ✅ Atualizar Definition of Done para incluir "Code Review aprovado"
- 📋 Configurar GitHub para exigir aprovação antes de merge (Próxima Sprint)

**Responsável:** Scrum Master
**Prazo:** Implementado durante esta Sprint

**Resultado Esperado:**
Reduzir bugs em produção e melhorar qualidade do código.

---

## 📈 Métricas da Sprint 1

| Métrica | Valor |
|---------|-------|
| Story Points Planejados | 25 |
| Story Points Concluídos | 21 |
| Velocity | 21 |
| Taxa de Conclusão | 84% |
| Bugs Encontrados | 1 (Crítico) |
| Bugs Resolvidos | 1 |
| Tempo Médio em "Em Progresso" | 1.5 dias |
| Tempo Médio em "Revisão de Código" | 0.5 dias |
| Tempo Médio em "Teste" | 0.8 dias |

---

## 🎓 Aprendizados da Sprint 1

### ✅ O que funcionou bem:
1. Daily Scrums foram eficazes para comunicação
2. Priorização clara do Product Backlog
3. Resposta rápida ao bug crítico
4. Boa colaboração entre PO e Dev Team

### ⚠️ O que pode melhorar:
1. Implementar Code Review obrigatório (Ação tomada!)
2. Melhorar estimativas (alguns cartões foram subestimados)
3. Automatizar testes de integração
4. Documentar APIs durante o desenvolvimento

### 🚀 Ações para Sprint 2:
1. ✅ Coluna de Code Review adicionada
2. Incluir tempo para testes automatizados no planejamento
3. Criar template de documentação de API
4. Revisar e refinar estimativas com Planning Poker

---

## 📸 Visualização do Quadro Final

```
┌─────────────────┬─────────────────┬─────────────────┬─────────────────┬─────────────────┬─────────────────┬─────────────────┐
│  Product        │  Sprint 1       │  Em Progresso   │  Revisão de     │  Teste          │  Concluído      │  Melhorias da   │
│  Backlog        │  Backlog        │                 │  Código         │                 │  Sprint 1       │  Retrospectiva  │
├─────────────────┼─────────────────┼─────────────────┼─────────────────┼─────────────────┼─────────────────┼─────────────────┤
│ 📌 10 cartões   │                 │                 │                 │                 │ ✅ Feature:     │ 🎯 [AÇÃO]       │
│                 │    (VAZIA)      │    (VAZIA)      │    (VAZIA)      │    (VAZIA)      │ Ver horários    │ Implementar     │
│ • Notificação   │                 │                 │                 │                 │                 │ Code Review     │
│ • Ver agenda    │                 │                 │                 │                 │ ✅ Feature:     │ Obrigatório     │
│ • Cancelar      │                 │                 │                 │                 │ Notificação     │                 │
│ • Bloquear      │                 │                 │                 │                 │                 │                 │
│ • Registrar $   │                 │                 │                 │                 │ ✅ Feature:     │                 │
│ • Relatório $   │                 │                 │                 │                 │ Registrar       │                 │
│ • Despesas      │                 │                 │                 │                 │ serviços        │                 │
│ • Login         │                 │                 │                 │                 │                 │                 │
│ • Cadastro      │                 │                 │                 │                 │ ✅ Feature:     │                 │
│ • Barbeiros     │                 │                 │                 │                 │ Login           │                 │
│                 │                 │                 │                 │                 │                 │                 │
│                 │                 │                 │                 │                 │ 🐛 BUG:         │                 │
│                 │                 │                 │                 │                 │ Reset senha     │                 │
└─────────────────┴─────────────────┴─────────────────┴─────────────────┴─────────────────┴─────────────────┴─────────────────┘
```

---

## 🎯 Conclusão

Este quadro Trello demonstra a aplicação prática de metodologias Ágeis (Scrum) em um projeto real de desenvolvimento de software. Pontos-chave:

1. **Product Backlog organizado** por épicos e prioridades
2. **Sprint 1 concluída** com 84% de taxa de sucesso
3. **Coluna de Code Review** implementada como melhoria da Retrospectiva
4. **Bug crítico** identificado e resolvido rapidamente
5. **Melhorias contínuas** documentadas e implementadas

A simulação mostra como o fluxo Scrum funciona na prática, desde o planejamento até a retrospectiva, incluindo adaptações baseadas em aprendizados.
