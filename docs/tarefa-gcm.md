# Playbook: Gerenciamento de Configuração e Mudança (GCM)

**Contexto do Processo**  
`[GCM] - Validação de Artefatos e Liberação de Release para Produção (PRD)`

**Objetivo**  
Garantir a rastreabilidade, conformidade técnica e integridade das entregas antes da promoção de módulos para o ambiente produtivo, alinhando o ciclo ágil (Scrum) aos controles de mudança (ITSM).

---

### 1. Matriz de Sincronização de Estados (História vs. Tarefas)

Para manter a consistência do fluxo no board e nas métricas de sprint, a transição de status entre a **História de Usuário** e as **Tarefas de Scrum** segue as regras de governança abaixo:

| Estado da História | Estado das Tarefas de Scrum | Regra de Governança |
| :--- | :--- | :--- |
| **Rascunho** | `Rascunho` | Fase de refinamento e levantamento inicial. |
| **Preparado** | `Preparado` | Escopo definido e pronto para entrar na Sprint. |
| **Trabalho em andamento** | `Trabalho em andamento` | Execução ativa pelas frentes técnicas. |
| **Pronto** | `Concluído` | Alterado exclusivamente pelo **Analista de GCM** após auditoria completa. |

---

### 2. Checklist de Auditoria e Quality Gate (Pré-Release)

Antes de alterar o estado da **História** para **Pronto** e habilitar a criação da Requisição de Mudança (RDM), o responsável por GCM executa as seguintes validações:

1. **Documentação Técnica:** Confirmar se a *Ficha Técnica* (artefato com inventário de componentes, scripts e dependências) está devidamente anexada à história.
2. **Conclusão Multifuncional:** Verificar se todas as subtasks das equipes envolvidas (**Requisitos, Desenvolvimento e QA**) foram finalizadas sem pendências bloqueantes.
3. **Transição de Homologação:** Validar a aprovação em ambiente de testes e atualizar o status de `(Testando)` para `(Pronto)`.

---

### 3. Padrão de Registro e Rastreabilidade (Audit Trail)

Para fins de auditoria e compliance, toda validação concluída é documentada nas **Anotações de Trabalho** do ticket utilizando o template padronizado abaixo:

```text
Validações e atividades realizadas:
1 - Ficha Técnica adicionada e validada na história.
2 - Verificação de conclusão das tarefas técnicas (REQ, DEV, QA).
3 - Transição de status de (Testando) para (Pronto) realizada com sucesso.
```

---

### 4. Encerramento do Ciclo

Após o registro da evidência de auditoria:
* Atualizar o campo **[Estado]** da tarefa de GCM para **[Concluído]**.
* Salvar o registro para consolidar o encerramento automático das **[Tarefas de Scrum]** e da **[História]**, liberando o pacote para a esteira de deploy em **PRD**.
