
---

# Documentação da stack de Tecnologias

## Frontend

### Framework Principal e Ferramentas de Build
* **React 18** com **TypeScript**
* **Vite** para ferramentas de build e servidor de desenvolvimento
* **TypeScript** para segurança de tipos
* **React Router** para navegação

### UI e Estilização
* **Tailwind CSS** para estilização utilitária (utility-first)
* **Material UI** para componentes principais
* **Shadcn UI** para componentes aprimorados
* **CSS Modules** para estilos específicos de componentes

### Gerenciamento de Estado
* **React Context API** para estado global
* **Hooks personalizados** para gerenciamento de estado local
* **React Query** para gerenciamento de estado do servidor

### Formulários e Validação
* **React Hook Form** para gerenciamento de formulários
* **Zod** para validação de esquema
* **TypeScript** para verificação de tipos

## Backend

### Framework Principal
* **FastAPI** para API REST
* **Python 3.11+**
* **Uvicorn** como servidor ASGI

### Banco de Dados e ORM
* **PostgreSQL** no Railway
* **Prisma** como ORM
* Gerenciamento de **migrações de banco de dados**

### Autenticação
* **Auth0** para autenticação
* Gerenciamento de **token JWT**
* **Login social** (Google)

### Integração de IA
* **OpenAI API** para:
    * Simulações de entrevista
    * Análise de currículo
    * Avaliação de respostas
    * Geração de perguntas

## Infraestrutura

### Implantação (Deployment)
* **Vercel** para hospedagem do frontend
* **Railway** para hospedagem do banco de dados
* Implantação do backend **FastAPI** no Hetzner/Coolify

### Ferramentas de Desenvolvimento
* **Git** para controle de versão
* **GitHub** para o repositório
* **GitHub Actions** para CI/CD
* **ESLint** e **Prettier** para formatação de código
* **Husky** para git hooks

### Monitoramento e Rastreamento de Erros
* **Sentry** para rastreamento de erros
* Integração básica de **análise de dados (analytics)**
* **Monitoramento de desempenho**

### Testes
* **Jest** para testes de frontend
* **Pytest** para testes de backend
* **Cypress** para testes E2E (End-to-End)

## Segurança
* **Aplicação de HTTPS**
* **Recursos de segurança Auth0**
* **Rate limiting** da API
* **Validação de entrada**
* **Prevenção de SQL injection**

---
