# Encurtador de URLs — wvshort-url

Este repositório é um projeto de demonstração para ilustrar como escrever histórias de usuário e critérios de aceitação para um MVP de um encurtador de URLs.

Objetivo
--------
Criar uma aplicação simples que permita que usuários autentiquem-se via Google, encurtem URLs longas, salvem suas URLs encurtadas e sejam redirecionados para as URLs originais quando acessarem os links curtos.

Status
------
O repositório contém as especificações funcionais e não funcionais do MVP. A implementação deve seguir a stack e as restrições descritas em `specs/00-requisitos-nao-funcionais.md`.

Funcionalidades do MVP
-----------------------
- Login social (Google): autenticação via OAuth para criar/associar contas de usuário.
- Encurtar URL: gerar um código curto único a partir de uma URL válida.
- Salvar URLs encurtadas: persistir o mapeamento associado ao usuário com metadados (URL original, código curto, data de criação, contagem de cliques).
- Redirecionamento: responder `GET /{codigo}` com redirecionamento 301 para a URL original e incrementar a contagem de cliques.

Onde estão as especificações
----------------------------
As histórias de usuário e critérios de aceitação em Gherkin estão em `specs/`:

- `specs/00-requisitos-nao-funcionais.md` — stack, segurança e arquitetura.
- `specs/01-encurtar-url.md` — validação e geração do link curto.
- `specs/02-redirecionamento.md` — redirecionamento para a URL original.
- `specs/03-login-google.md` — autenticação via Google.
- `specs/04-salvar-urls.md` — persistência das URLs do usuário.

## Recursos — User Stories e Gherkin

Links úteis para aprender a escrever histórias de usuário e referência para Gherkin:

- **Atlassian (pt-br)**: Guia prático sobre como escrever User Stories — https://www.atlassian.com/br/agile/project-management/user-stories

- **Mountain Goat Software (Mike Cohn)**: Conceitos e boas práticas para User Stories — https://www.mountaingoatsoftware.com/agile/user-stories

- **Agile Alliance**: Definição e contexto de User Stories — https://www.agilealliance.org/glossary/user-stories/

- **Gherkin / Cucumber**: Documentação e referência do Gherkin (linguagem de especificação) — https://cucumber.io/docs/gherkin/

- **Referência técnica do Gherkin**: https://cucumber.github.io/gherkin/


