# Padrão de Ficha Técnica e Auditoria de Entrega

Este guia define o fluxo operacional de verificação de artefatos de desenvolvimento e os templates padronizados de **Ficha Técnica** utilizados antes da liberação de histórias para homologação e mudança (**Azure DevOps** e **GitLab**).

---

### 1. Fluxo de Validação e Montagem (Passo a Passo)

Antes de consolidar a documentação na **História de Usuário**, o Analista de Configuração executa a seguinte rotina de conferência:

1. **Conferência de Status:** Acessar as **Tarefas de Scrum** e confirmar se a task de Desenvolvimento (**DEV**) encontra-se no estado **[Concluído]**.
2. **Auditoria de Artefatos:** Abrir a tarefa concluída e validar se o desenvolvedor preencheu os metadados técnicos básicos. Caso esteja ausente, solicitar a inclusão antes de prosseguir.
3. **Coleta de Dados Brutos:** Extrair as informações fornecidas pelo desenvolvedor no padrão de entrada:
   ```text
   Repositório: projeto-servico-core
   Branch: feature/STRY0000000-nome-funcionalidade
   Commit: N/A
   Pull Request: N/A
   System Properties: N/A
   SWAGGER: N/A
   Fila: N/A
   Integração: N/A
   Banco de dados: N/A
   Desenvolvedor: Nome do Desenvolvedor
   ```
4. **Rastreio de Links no Repositório:** Acessar a plataforma de versionamento correspondente (**Azure DevOps** ou **GitLab**), localizar o repositório e a `Branch DEV` informada e copiar a URL direta da branch.
5. **Verificação de Scripts DML (Banco de Dados):** Caso existam alterações de banco de dados, validar o link direto do script no repositório. Se não tiver sido informado, navegar até o diretório padrão de scripts na `Branch DEV` (ex.: `/docs/scripts`) para anexar a referência exata de execução e rollback.
6. **Consolidação:** Preencher o template correspondente abaixo e anexar na **História** para rastreabilidade de QA e GCM.

---

### 2. Template: Ficha Técnica de Entrega — Azure DevOps

Utilize o bloco abaixo para entregas versionadas no **Azure Repos** (clique no ícone superior direito para copiar):

```text
1. Objetivo - Azure DevOps

Prezados,
Informamos a conclusão e disponibilização da codificação referente ao item de backlog, conforme detalhamento técnico abaixo.

2. Ficha Técnica

Repositório   ======= projeto-servico-core
Branch DEV    ======= feature/STRY0000000-nome-funcionalidade
Link Branch   ======= https://azure.com

3. Informações Complementares System Properties (Library)

SWAGGER       ======= N/A
Fila          ======= N/A
Integração    ======= N/A
Library       ======= LIB-PROJETO-CONFIGURACAO-DES
Variáveis     ======= _ENV.DB_MAX_SIZE ======= 32

4. Informações Banco de Dados (DML) - [instancia_db]

Execução      ======= N/A
Rollback      ======= N/A

5. Informações Código Fonte

Revisão por Pares ======= N/A
Code Review       ======= N/A

6. Responsável pelo Desenvolvimento

Desenvolvedor ======= Nome do Desenvolvedor

7. Observações

Durante a implementação, foram incorporadas e mergeadas as seguintes branches:
  • feature/implementacoes-base
  • feature/00000000-servico-integracao-core
  • feature/00000000-consulta-status-transacao

8. Status da Entrega

✅ Codificação concluída e disponibilizada no repositório informado.
✅ Branch de desenvolvimento disponível para consulta e validação.
✅ Informações técnicas registradas nesta documentação.

9. Encerramento

Permanecemos à disposição para esclarecimentos adicionais, suporte durante as etapas de validação e acompanhamento da implantação.
```

---

### 3. Template: Ficha Técnica de Entrega — GitLab

Utilize o bloco abaixo para entregas versionadas no **GitLab** (clique no ícone superior direito para copiar):

```text
1. Objetivo - GitLab

Prezados,
Informamos a conclusão e disponibilização da codificação referente ao item de backlog, conforme detalhamento técnico abaixo.

2. Ficha Técnica

Repositório   ======= GRUPO/projeto-servico-core
Branch DEV    ======= feature/STRY0000000-nome-funcionalidade
Link Branch   ======= https://gitlab.com

3. Informações Complementares System Properties (Library)

SWAGGER       ======= N/A
Fila          ======= N/A
Integração    ======= N/A
Library       ======= LIB-PROJETO-CONFIGURACAO-DES
Variáveis     ======= _ENV.DB_MAX_SIZE ======= 32

4. Informações Banco de Dados (DML) - [instancia_db]

Execução      ======= N/A
Rollback      ======= N/A

5. Informações Código Fonte

Revisão por Pares ======= N/A
Code Review       ======= N/A

6. Responsável pelo Desenvolvimento

Desenvolvedor ======= Nome do Desenvolvedor

7. Observações

Durante a implementação, foram incorporadas e mergeadas as seguintes branches:
  • feature/implementacoes-base
  • feature/00000000-servico-integracao-core
  • feature/00000000-consulta-status-transacao

8. Status da Entrega

✅ Codificação concluída e disponibilizada no repositório informado.
✅ Branch de desenvolvimento disponível para consulta e validação.
✅ Informações técnicas registradas nesta documentação.

9. Encerramento

Permanecemos à disposição para esclarecimentos adicionais, suporte durante as etapas de validação e acompanhamento da implantação.
```

