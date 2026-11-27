# CI/CD com GitHub Actions e Cloudflare Pages

Este projeto foi desenvolvido como parte de um laboratório prático de DevOps, com o objetivo de aplicar conceitos de versionamento de código, automação de pipelines CI/CD e publicação de aplicações web.

A aplicação consiste em um site HTML simples, integrado a um pipeline de automação utilizando GitHub Actions e publicado por meio do Cloudflare Pages.

## Objetivo

Implementar um fluxo básico de integração e entrega contínua (CI/CD), permitindo que alterações realizadas no código sejam versionadas pelo Git, verificadas automaticamente pelo GitHub Actions e disponibilizadas por meio do Cloudflare Pages.

## Tecnologias:
- **HTML5** — estruturação do site.
- **Git** — controle de versionamento.
- **GitHub** — hospedagem do repositório.
- **GitHub Actions** — automação do pipeline CI/CD.
- **Cloudflare Pages** — hospedagem e publicação do site.

## Estrutura do projeto

```text
meu-site-devops/
│
├── index.html
│
└── .github/
    └── workflows/
        └── ci.yml
```

### Arquivos

| Arquivo | Descrição |
|---|---|
| `index.html` | Página principal do site. |
| `.github/workflows/ci.yml` | Configuração do pipeline de automação CI/CD. |


- O pipeline foi desenvolvido utilizando GitHub Actions, sendo acionado automaticamente quando ocorre um push na branch `main`.

O fluxo está organizado em quatro etapas:

```text
Desenvolvimento
      │
      ▼
  Git Commit
      │
      ▼
  Git Push (main)
      │
      ▼
 GitHub Actions
      │
      ▼
 ┌──────────────┐
 │    Setup     │
 └──────────────┘
      │
      ▼
 ┌──────────────┐
 │  Validation  │
 └──────────────┘
      │
      ▼
 ┌──────────────┐
 │    Build     │
 └──────────────┘
      │
      ▼
 ┌──────────────┐
 │    Deploy    │
 └──────────────┘
      │
      ▼
 Cloudflare Pages
      │
      ▼
 Site publicado
```

## Cloudflare Pages

O projeto foi integrado ao Cloudflare Pages, que permite a publicação do site a partir do repositório GitHub.

Após a integração, as alterações enviadas para a branch configurada são utilizadas no processo automático de atualização do site.

### Site publicado

🔗 https://meu-site-devops-41z.pages.dev/

