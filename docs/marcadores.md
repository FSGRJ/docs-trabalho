# Uso dos Marcadores na História (Taxonomia de Fluxo)

Este guia padroniza a aplicação e atualização de **Marcadores (Tags)** nas **Histórias de Usuário** durante todo o ciclo de vida da Sprint. O uso correto dessas etiquetas garante visibilidade em tempo real sobre filas de atendimento, gargalos técnicos e prontidão para deploy.

---

### 1. Regras Gerais de Aplicação

* **Escopo de Vinculação:** A taxonomia aplica-se às histórias vinculadas às iterações ágeis das squads de engenharia (ex.: `Projeto_Squad01 - 2026 PI3 Sprint 3`).
* **Dinâmica de Atualização:** Os marcadores são inseridos e removidos progressivamente conforme o avanço das **Tarefas de Scrum** das disciplinas envolvidas (**REQ**, **DEV**, **DML**, **QA** e **GCM**).
* **Identificação de Módulo:** O marcador técnico do componente alterado (ex.: `[modulo-servico-core]`) deve refletir exatamente o módulo definido no escopo da **História** ou registrado na **Ficha Técnica** pelo desenvolvedor.

---

### 2. Matriz de Marcadores por Estado da História

#### ⚪ Estado: `Rascunho`
Fase inicial de concepção e entendimento de negócio.

* `[Refinamento Negocial]`
* `[Refinamento Técnico]`
* `[não tem requisito]` *(aplicável quando não há documentação funcional formal)*

---

#### 🔵 Estado: `Preparado`
História refinada e apta para entrada na Sprint.

* `[Refinada]`
* `[não tem requisito]`
* `[Fila Desenvolvimento]`
* `[Ficha Técnica]`
* `[Fila Teste]`
* `[Fila Requisito]`
* `[Elaborando Requisito]` — *Incluir apenas se o Analista de Requisitos tiver criado uma Tarefa de Scrum de **REQ** com estado = **Trabalho em andamento**.*

---

#### 🟡 Estado: `Trabalho em andamento`
Execução ativa de desenvolvimento, banco de dados e documentação.

* `[Refinada]`
* `[não tem requisito]`
* `[Ficha Técnica]`
* `[modulo-servico-core]` — *Incluir conforme o módulo definido na História ou na Ficha Técnica.*
* `[Fila Teste]`
* `[Fila Requisito]`
* `[Elaborando Requisito]` — *Manter caso exista tarefa de **REQ** em **Trabalho em andamento**.*

**Marcadores Condicionais de Banco de Dados (DML):**
* `[Fila Script Banco]` — *Incluir caso o DEV tenha criado uma tarefa de **DML** com estado = **Rascunho**.*
* `[Elaborando Script Banco]` — *Incluir caso exista tarefa de **DML** com estado = **Trabalho em andamento**.*
* `[Valida Script Banco]` — *Incluir durante a etapa de revisão da tarefa de **DML** em **Trabalho em andamento**.*

---

#### 🟠 Estado: `Pronto para Teste`
Codificação concluída e aguardando início da validação de QA.

* `[Refinada]`
* `[modulo-servico-core]`
* `[não tem requisito]`
* `[Fila Teste]`
* `[Fila Requisito]`
* `[Elaborando Requisito]` — *Manter caso exista tarefa de **REQ** em **Trabalho em andamento**.*

---

#### 🟣 Estado: `Testando`
Execução ativa dos cenários de homologação pela equipe de qualidade.

* `[Refinada]`
* `[modulo-servico-core]`
* `[não tem requisito]`
* `[Em Teste]`
* `[Fila Requisito]`
* `[Elaborando Requisito]` — *Manter caso exista tarefa de **REQ** em **Trabalho em andamento**.*

---

#### 🟢 Estado: `Pronto`
Homologação técnica concluída e aguardando validação final de negócio.

* `[Refinada]`
* `[modulo-servico-core]`
* `[não tem requisito]`
* `[Aceite Gestor Interno]`

---

#### ⚫ Estado: `Concluído` (Pré-Implantação vs. Pós-Implantação)
Nesta etapa final, os marcadores diferenciam histórias que estão na esteira de mudança daquelas já entregues em produção:

**Fase A — Preparação de Release (Aguardando Janela de Mudança):**
* `[Refinada]`
* `[modulo-servico-core]`
* `[não tem requisito]`
* `[Planejar Implantacao]`
* `[Elaborando Release]`

**Fase B — Implantação Concluída em Produção (PRD):**
* `[Refinada]`
* `[modulo-servico-core]`
* `[não tem requisito]`
* `[Implantado em PRD]` — *Após a subida para produção, remover os marcadores de planejamento/release e manter apenas esta tag de encerramento.*

