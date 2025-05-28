# SurfBoard

Sistema de gerenciamento completo para escolas de surf.

---

## 🎯 Objetivo do Sistema

O sistema **SurfBoard** tem como principal objetivo gerenciar todos os aspectos operacionais de uma escola de surf. Ele permite a organização eficiente de alunos, professores, mensalidades e agendamentos de aulas, centralizando as informações e proporcionando uma experiência fluida para todos os usuários envolvidos.

### Metas do Sistema

- Facilitar o cadastro e a gestão de alunos e professores.
- Automatizar o controle de planos e mensalidades.
- Prover uma interface intuitiva para agendamento de aulas práticas.
- Permitir o acesso seguro e personalizado para administradores, professores e alunos.
- Melhorar o controle financeiro e a produtividade da escola de surf.

---

## 👤 Perfis de Usuários

O sistema SurfBoard contempla três perfis principais de usuários, cada um com permissões e funcionalidades específicas:

### 1. Administrador
- Cadastro e gerenciamento de professores e alunos.
- Controle completo sobre planos e mensalidades.
- Acesso a relatórios e estatísticas gerais.
- Gerenciamento das configurações do sistema.

### 2. Professor
- Visualizar sua lista de alunos.
- Agendar e gerenciar suas aulas.
- Confirmar presença dos alunos nas aulas.
- Consultar histórico de aulas ministradas.

### 3. Aluno
- Visualizar sua agenda de aulas.
- Consultar status e histórico das mensalidades.
- Receber notificações sobre aulas e pagamentos.

---

## ⚙️ Funcionalidades Principais

O sistema SurfBoard oferece as seguintes funcionalidades principais para atender às necessidades da escola de surf:

### Cadastro e Gerenciamento
- Cadastro de professores com informações pessoais, especializações e status.
- Cadastro de alunos com dados pessoais, plano contratado e situação financeira.
- Gerenciamento e atualização de planos e mensalidades.

### Mensalidades
- Controle de planos (mensal, trimestral, anual).
- Registro de pagamentos e geração de histórico financeiro.
- Emissão de boletos ou registro manual de pagamentos.

### Agendamento de Aulas
- Criação e visualização de aulas com data, horário e professor responsável.
- Gerenciamento da capacidade máxima de alunos por aula.
- Inscrição e confirmação de presença dos alunos nas aulas agendadas.

### Relatórios e Estatísticas
- Relatórios financeiros e de presença.
- Indicadores de desempenho para professores e alunos.

---

## 🧭 Fluxo Básico do Sistema

O SurfBoard possui um fluxo simples e eficiente para cada tipo de usuário, garantindo usabilidade e controle:

### Administrador
1. Realiza login no sistema.
2. Acessa o painel administrativo.
3. Cadastra e gerencia professores e alunos.
4. Configura planos e controla mensalidades.
5. Consulta relatórios e realiza ajustes gerais.

### Professor
1. Faz login na plataforma.
2. Visualiza sua agenda de aulas.
3. Agenda novas aulas e gerencia horários.
4. Confirma presença dos alunos nas aulas.
5. Consulta histórico e relatórios pessoais.

### Aluno
1. Efetua login no sistema.
2. Visualiza suas aulas agendadas.
3. Confirma presença nas aulas (quando permitido).
4. Consulta status e histórico de mensalidades.
5. Recebe notificações sobre aulas e pagamentos.

---

## 🧰 Tecnologias (.NET Stack)

O projeto SurfBoard será desenvolvido utilizando tecnologias do ecossistema .NET para garantir performance, escalabilidade e segurança:

### Backend
- **ASP NET Core Web API:** Implementação da API RESTful responsável pela lógica de negócio e comunicação com o banco de dados.
- **Entity Framework Core:** ORM para acesso e manipulação do banco de dados relacional.
- **ASP NET Core Identity:** Gerenciamento de autenticação e autorização de usuários.

### Frontend
- **ASP NET MVC:** Interface administrativa para o painel de controle dos administradores (server-side rendering).
- **SPA (React / Angular / Blazor WebAssembly):** Aplicação interativa para professores e alunos gerenciarem agendamentos e aulas.

### Banco de Dados
- **SQL Server** Banco de dados relacional para armazenamento das informações do sistema.

### Outros
- **JWT (JSON Web Tokens):** Autenticação baseada em tokens para comunicação segura entre frontends e backend.
- **Docker:** Containerização para facilitar o deploy e a escalabilidade do sistema.

## Estrutura de Solução

A solução SurfBoard será organizada em múltiplos projetos para garantir modularidade, separação de responsabilidades e fácil manutenção.

### Estrutura Geral
```
SurfBoard.sln
│
├── src/
│   ├── SurfBoard.Domain/               # Entidades, regras de negócio, interfaces do domínio (Core)
│   ├── SurfBoard.Application/          # Casos de uso, lógica de aplicação, serviços (Use Cases)
│   ├── SurfBoard.Infrastructure/       # Implementações técnicas (EF Core, repositórios, serviços externos)
│   ├── SurfBoard.API/                  # Projeto Web API - interface externa (Controllers)
│   ├── SurfBoard.AdminMVC/             # Projeto MVC para admin (interface web)
│   ├── SurfBoard.SPA/                  # Frontend SPA (React, Angular, Blazor)
│   └── SurfBoard.Identity/             # Serviço de autenticação/autorização (IdentityServer, ASP.NET Identity)
│
├── tests/
│   ├── SurfBoard.Domain.Tests/          # Testes unitários de domínio
│   ├── SurfBoard.Application.Tests/     # Testes unitários de aplicação
│   ├── SurfBoard.Infrastructure.Tests/  # Testes de infraestrutura (ex: acesso a dados)
│   └── SurfBoard.API.Tests/             # Testes de integração para API
│
└── docs/
```
