# 📚 Base de Conhecimento & Playbooks Técnicos

[![GitHub Pages](https://shields.io)](https://github.io)
[![Docsify](https://shields.io)](https://js.org)
[![Markdown](https://shields.io)](https://markdownguide.org)
[![License](https://shields.io)](#)

Repositório dedicado à centralização de **playbooks operacionais, checklists de governança, engenharia de configuração e boas práticas de entrega contínua (CI/CD)**.

🔗 **Acesse a documentação online interativa:** **[https://github.io](https://github.io)**

---

## 🎯 Sobre o Projeto

Este projeto transforma procedimentos técnicos do dia a dia em uma **Wiki estruturada, pesquisável e de fácil manutenção**, conectando metodologias ágeis (**Scrum**) aos controles de qualidade e gerenciamento de mudanças (**ITSM / ITIL**).

> **Nota de Privacidade:** Todos os fluxos, repositórios, URLs e nomenclaturas contidos neste repositório foram generalizados e sanitizados para fins educacionais e de portfólio técnico.

---

## 🛠️ Arquitetura da Solução

A documentação utiliza **Docsify** hospedado gratuitamente via **GitHub Pages**, eliminando a necessidade de processos de build estático (como Jekyll ou Hugo) e renderizando arquivos Markdown diretamente no navegador:

```text
docs-trabalho/
├── README.md                  # Apresentação do repositório (este arquivo)
└── docs/                      # Diretório servido pelo GitHub Pages
    ├── index.html             # Configuração do Docsify, tema escuro e plugins
    ├── .nojekyll              # Libera a leitura de arquivos iniciados com "_"
    ├── _sidebar.md            # Estrutura hierárquica do menu lateral
    ├── README.md              # Página inicial da documentação online
    ├── tarefa-gcm.md          # Playbook de Gerenciamento de Configuração e Mudança
    ├── ficha-tecnica.md       # Padrão de auditoria e templates (Azure DevOps / GitLab)
    └── marcadores.md          # Taxonomia de tags e rastreabilidade de histórias
```

### Principais Recursos Ativados
* **Tema Escuro Customizado:** Paleta inspirada em ambientes de desenvolvimento e Azure DevOps.
* **Busca Instantânea:** Indexação automática de títulos e conteúdos em português.
* **Cópia Rápida (Copy-to-Clipboard):** Botão integrado nos blocos de código para agilizar o preenchimento de tickets e anotações de trabalho.

---

## ➕ Como Adicionar Novas Páginas

1. Crie um novo arquivo `.md` dentro da pasta `docs/` (ex.: `docs/novo-playbook.md`).
2. Adicione o link correspondente no menu lateral editando o arquivo `docs/_sidebar.md`.
3. Faça o **commit** e **push** na branch `main` — o GitHub Pages atualizará o site automaticamente em instantes.

---

### 📚 Base de Conhecimento & Playbooks Técnicos

Documentação técnica interativa desenvolvida com **Docsify + GitHub Pages**, reunindo processos padronizados de **Engenharia de Configuração, Governança de Mudanças (GCM/ITSM), Auditoria de Artefatos (Azure DevOps / GitLab) e Taxonomia Ágil**.

* 🔗 **Acessar Documentação Online:** [fsgrj.github.io/docs-trabalho](https://github.io)
* 💻 **Repositório Fonte:** [://github.com](https://://github.com)


## 👨‍💻 Autor

Desenvolvido e mantido por **Fabiano Gonçalves (FSGRJ)** — Analista de Configurações | DevOps & CI/CD | Cloud | RPA.

* 🌐 **Portfólio:** [https://github.io](https://github.io)
* 🐙 **GitHub:** [@FSGRJ](https://github.com)


<div style="background-color: #161b22; border: 1px solid #30363d; border-radius: 8px; padding: 20px; margin: 20px 0; font-family: system-ui, -apple-system, sans-serif; color: #c9d1d9;">
  <div style="display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 10px;">
    <h3 style="margin: 0; color: #58a6ff; font-size: 1.2rem;">
      📚 Base de Conhecimento & Playbooks Técnicos
    </h3>
    <span style="background-color: #1f6feb26; color: #58a6ff; border: 1px solid #1f6feb66; padding: 3px 10px; border-radius: 12px; font-size: 0.75rem; font-weight: 600;">
      Docsify • DevOps • Governança
    </span>
  </div>

  <p style="margin: 12px 0 16px 0; font-size: 0.95rem; line-height: 1.5; color: #8b949e;">
    Portal interativo de documentação operacional com foco em Gestão de Configuração e Mudança (GCM), templates de Ficha Técnica (Azure DevOps &amp; GitLab) e taxonomia de rastreabilidade ágil.
  </p>

  <div style="display: flex; gap: 12px; flex-wrap: wrap;">
    <a href="https://github.io" target="_blank" rel="noopener noreferrer" style="background-color: #238636; color: #ffffff; text-decoration: none; padding: 8px 16px; border-radius: 6px; font-size: 0.875rem; font-weight: 600;">
      🌐 Acessar Documentação
    </a>
    <a href="https://github.com" target="_blank" rel="noopener noreferrer" style="background-color: #21262d; color: #c9d1d9; border: 1px solid #363b42; text-decoration: none; padding: 8px 16px; border-radius: 6px; font-size: 0.875rem; font-weight: 600;">
      🐙 Ver Código-Fonte
    </a>
  </div>
</div>
