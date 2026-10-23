# SGP Web - Sistema de Gestão de Projetos (Front-end)

Interface web do **Sistema de Gestão de Projetos**, desenvolvida com **React.js** e integrada a uma API REST em **Java e Spring Boot** com banco de dados **MySQL**. A aplicação consome a API, exibe os dados em tela e salva no banco o que o usuário cadastra.

> ⚙️ **Back-end:** [gestao-projetos-api](https://github.com/manoelamanciio/gestao-projetos-api)

## Funcionalidades

- **Dashboard** com indicadores de projetos por status (concluídos, em andamento, pendentes e cancelados) e gráficos de rosca e de barras (Chart.js).
- **Usuários:** formulário de cadastro e lista em modal, com exclusão.
- **Projetos:** formulário de cadastro com responsável e status, e lista em modal com filtro por nome e por responsável, paginação e exclusão.
- **Tarefas:** formulário de cadastro vinculado a projeto e usuário, e lista em modal com exclusão.
- Navegação entre as telas com React Router e barra de navegação responsiva.
- Interface responsiva com Bootstrap e React-Bootstrap.

## Tecnologias

- React 19 e Vite
- JavaScript (ES6+), HTML5 e CSS3
- React Router
- Bootstrap, React-Bootstrap, Bootstrap Icons e React Icons
- Axios (consumo da API REST)
- Chart.js e react-chartjs-2
- ESLint

## Demonstração

<!-- Adicione aqui 2 ou 3 prints das telas (Dashboard, Projetos, Tarefas), por exemplo:
![Dashboard](docs/dashboard.png)
-->

## Estrutura do projeto

```
src
├── Api.js                 # Instância do Axios (URL base da API)
├── main.jsx               # Ponto de entrada
├── assets                 # Logo e imagens
└── components
    ├── Home.jsx           # Rotas da aplicação
    ├── BarraNav.jsx       # Barra de navegação
    ├── Dashboard.jsx      # Indicadores e gráficos
    ├── FormUsuario.jsx    # Cadastro de usuários
    ├── FormProjeto.jsx    # Cadastro de projetos
    ├── FormTarefas.jsx    # Cadastro de tarefas
    ├── ListaDeUsuarios.jsx
    ├── ListaDeProjetos.jsx
    └── ListaDeTarefas.jsx
```

## Como executar

### Pré-requisitos

- Node.js 20 ou superior
- Back-end em execução. Siga o passo a passo do [gestao-projetos-api](https://github.com/manoelamanciio/gestao-projetos-api), que sobe a API em `http://localhost:8080`.

### Passo a passo

1. Clone o repositório:
   ```bash
   git clone https://github.com/manoelamanciio/gestao-projetos-web.git
   cd gestao-projetos-web
   ```

2. Instale as dependências:
   ```bash
   npm install
   ```

3. Inicie a aplicação:
   ```bash
   npm run dev
   ```

4. Acesse no navegador: http://localhost:5173

A URL da API está definida em `src/Api.js` (`http://localhost:8080`). O back-end já libera o acesso (CORS) para a origem `http://localhost:5173`.

### Outros comandos

| Comando | Descrição |
|---|---|
| `npm run build` | Gera a versão de produção |
| `npm run preview` | Visualiza o build localmente |
| `npm run lint` | Executa o ESLint |

## Integração com a API

| Tela | Endpoints utilizados |
|---|---|
| Dashboard | `GET /projetos`, `GET /usuarios` |
| Usuários | `POST /usuarios`, `GET /usuarios`, `DELETE /usuarios/{id}` |
| Projetos | `POST /projetos`, `GET /projetos`, `DELETE /projetos/{id}` |
| Tarefas | `POST /tarefas`, `GET /tarefas`, `DELETE /tarefas/{id}` |

A documentação completa da API está no Swagger: http://localhost:8080/swagger-ui.html

## Próximos passos

- Adicionar edição de usuários, projetos e tarefas.
- Adicionar autenticação e controle de acesso.
- Usar variável de ambiente para a URL da API (`VITE_API_URL`).
- Adicionar testes automatizados dos componentes.
- Publicar a aplicação online (deploy).

## Autor

**Manoel Amancio da Silva Neto**
Estudante de Engenharia de Software e Desenvolvedor Full Stack (formado pela Treina Recife)

[LinkedIn](https://www.linkedin.com/in/manoellamanciio) | [GitHub](https://github.com/manoelamanciio) | manoel.amanciio@gmail.com
