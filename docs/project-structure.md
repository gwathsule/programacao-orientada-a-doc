````markdown
# Documentação da Estrutura do Projeto

## Estrutura Monorepo para React-Vite e FastAPI

```bash
techprep-ai/
├── packages/
│   ├── shared/                    # Código compartilhado entre frontend e backend
│   │   ├── types/                 # Definições de tipo TypeScript
│   │   │   ├── interview.types.ts
│   │   │   ├── user.types.ts
│   │   │   └── resume.types.ts
│   │   └── constants/
│   │       └── index.ts          # Constantes compartilhadas
│   │
│   ├── frontend/                  # Aplicação React-Vite
│   │   ├── src/
│   │   │   ├── components/       # Componentes de design atômico
│   │   │   │   ├── atoms/
│   │   │   │   │   ├── Button.tsx
│   │   │   │   │   ├── Input.tsx
│   │   │   │   │   └── Typography.tsx
│   │   │   │   │
│   │   │   │   ├── molecules/
│   │   │   │   │   ├── SearchBar.tsx
│   │   │   │   │   └── QuestionCard.tsx
│   │   │   │   │
│   │   │   │   └── organisms/
│   │   │   │       ├── InterviewChat.tsx
│   │   │   │       └── ResumeUploader.tsx
│   │   │   │
│   │   │   ├── pages/           # Componentes de página
│   │   │   │   ├── Dashboard.tsx
│   │   │   │   ├── Interview.tsx
│   │   │   │   └── Profile.tsx
│   │   │   │
│   │   │   ├── hooks/           # Hooks React personalizados
│   │   │   │   ├── useInterview.ts
│   │   │   │   └── useResume.ts
│   │   │   │
│   │   │   ├── api/            # Integração de API
│   │   │   │   └── client.ts   # Configuração Axios/fetch
│   │   │   │
│   │   │   ├── lib/            # Funções de utilidade
│   │   │   │   └── helpers.ts
│   │   │   │
│   │   │   ├── styles/         # Estilos globais e temas
│   │   │   │   └── global.css
│   │   │   │
│   │   │   ├── types/         # Tipos específicos do frontend
│   │   │   ├── main.tsx       # Ponto de entrada
│   │   │   ├── App.tsx        # Componente raiz
│   │   │   └── vite-env.d.ts  # Declarações de tipo Vite
│   │   │
│   │   ├── index.html
│   │   ├── vite.config.ts
│   │   ├── tsconfig.json
│   │   └── package.json
│   │
│   └── backend/                  # Aplicação FastAPI
│       ├── app/
│       │   ├── api/             # Rotas de API
│       │   │   ├── endpoints/
│       │   │   │   ├── interviews.py
│       │   │   │   ├── users.py
│       │   │   │   └── resumes.py
│       │   │   └── deps.py      # Dependências e utilitários
│       │   │
│       │   ├── core/            # Configurações principais
│       │   │   ├── config.py    # Configurações de ambiente
│       │   │   └── security.py  # Configurações de autenticação
│       │   │
│       │   ├── models/          # Modelos SQLAlchemy
│       │   │   ├── user.py
│       │   │   └── interview.py
│       │   │
│       │   ├── schemas/         # Schemas Pydantic
│       │   │   ├── user.py
│       │   │   └── interview.py
│       │   │
│       │   └── services/        # Lógica de negócio
│       │       ├── interview.py
│       │       └── resume.py
│       │
│       ├── tests/               # Testes de backend
│       ├── alembic/             # Migrações de banco de dados
│       ├── requirements.txt
│       └── main.py              # Ponto de entrada FastAPI
│
├── package.json                  # package.json raiz
└── turbo.json                   # Configuração Turborepo
````

-----

Esta estrutura é especificamente **otimizada para React-Vite e FastAPI** porque:

### Frontend (React-Vite):

  * Usa a extensão **.tsx** para todos os componentes React, garantindo o suporte adequado ao TypeScript.
  * Segue a estrutura de projeto recomendada pelo Vite, com `src/` como o diretório principal de origem.
  * Implementa o **design atômico** mantendo as convenções do Vite para **ativos estáticos** e **configuração**.
  * Inclui **arquivos de configuração específicos do Vite** (`vite.config.ts`) e **declarações de tipo**.

### Backend (FastAPI):

  * Segue a estrutura de projeto recomendada pelo FastAPI, com `app/` como o **pacote principal**.
  * Separa as responsabilidades em **modelos**, **schemas** e **serviços**.
  * Inclui **Alembic** para **migrações de banco de dados**.
  * Mantém a **estrutura de pacote Python** com `requirements.txt`.

### Tipos Compartilhados:

O pacote de **tipos compartilhados** ajuda a manter a **consistência entre frontend e backend** ao:

  * Definir interfaces que correspondem aos **modelos Pydantic** do FastAPI.
  * Fornecer **segurança de tipo** para respostas de API.
  * Garantir **estruturas de dados consistentes** em toda a aplicação.

<!-- end list -->
