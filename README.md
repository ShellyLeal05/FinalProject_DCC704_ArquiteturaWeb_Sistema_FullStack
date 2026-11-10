# TechParts · Aplicação Web Full Stack

**Projeto acadêmico de Arquitetura Web** | React · Node.js · Express · MongoDB

O **TechParts** é uma aplicação web full stack para catálogo e gerenciamento de produtos. O sistema reúne uma interface SPA em React, uma API REST em Node.js/Express e persistência de dados com MongoDB, incluindo autenticação de usuários e permissões de acesso.

> **Contexto:** projeto desenvolvido em equipe como trabalho final de uma disciplina de Arquitetura Web. Não se trata de experiência profissional ou de um sistema publicado em produção.

## Minha participação

Participei do desenvolvimento do **frontend e do backend** do TechParts, em colaboração com **Eduardo Izidório**. O trabalho envolveu as duas camadas da aplicação; as funcionalidades descritas a seguir pertencem ao projeto como um todo e não representam uma divisão individual das entregas.

## Demonstração

[▶ Assistir ao vídeo de demonstração](https://youtu.be/Zmi-gzpOHY8)

## Funcionalidades do projeto

- Cadastro e login de usuários;
- Autenticação com JWT e proteção de rotas;
- Diferenciação de permissões entre perfis `admin` e `user`;
- Listagem pública e visualização de detalhes de produtos;
- Operações de **criação, leitura, atualização e exclusão (CRUD)** de produtos para administradores;
- Consumo da API pelo frontend React, incluindo estados de carregamento e mensagens de erro.

## Tecnologias

| Camada | Tecnologias e recursos |
| --- | --- |
| Frontend | React, Vite, React Router, Axios, CSS |
| Backend | Node.js, Express, API REST |
| Persistência | MongoDB, Mongoose |
| Autenticação | JWT e bcryptjs |
| Organização | Separação entre `client/` e `server/`, com pastas de componentes, rotas, controladores e modelos |

## Estrutura simplificada

```text
TechParts/
├── client/             # Interface React
│   └── src/
│       ├── components/
│       ├── contexts/
│       ├── pages/
│       ├── routes/
│       └── services/
├── server/             # API Express
│   ├── config/
│   ├── controllers/
│   ├── middlewares/
│   ├── models/
│   └── routes/
└── README.md
```

## Como executar localmente

### Pré-requisitos

- Node.js e npm;
- MongoDB local ou MongoDB Atlas.

**1. Clone o repositório:**

```bash
git clone https://github.com/ShellyLeal05/FinalProject_DCC704_ArquiteturaWeb_Sistema_FullStack.git
cd FinalProject_DCC704_ArquiteturaWeb_Sistema_FullStack
```

**2. Configure e inicie o backend:**

```bash
cd server
npm install
```

Crie um arquivo `server/.env` com valores de desenvolvimento apropriados:

```dotenv
PORT=5000
MONGO_URI=mongodb://127.0.0.1:27017/ecommerce_db
JWT_SECRET=substitua_por_uma_chave_local_segura
```

Depois, execute:

```bash
npm run dev
```

**3. Inicie o frontend em outro terminal:**

```bash
cd client
npm install
npm run dev
```

Por padrão, o frontend fica disponível em `http://localhost:5173`, e o backend em `http://localhost:5000`.

> Não publique valores reais de `.env`, senhas, tokens ou chaves de acesso. Ajuste os endereços e as variáveis conforme a configuração do seu ambiente.

## Exemplos de rotas da API

| Método | Endpoint | Finalidade |
| --- | --- | --- |
| `POST` | `/api/auth/register` | Cadastrar usuário |
| `POST` | `/api/auth/login` | Autenticar usuário |
| `GET` | `/api/products` | Listar produtos |
| `GET` | `/api/products/:id` | Consultar produto |
| `POST` | `/api/products` | Cadastrar produto (admin) |
| `PUT` | `/api/products/:id` | Editar produto (admin) |
| `DELETE` | `/api/products/:id` | Excluir produto (admin) |

## Melhorias futuras

- Incluir capturas de tela de páginas e fluxos relevantes;
- Adicionar testes automatizados;
- Documentar a divisão de responsabilidades da equipe, se ambos os autores concordarem;
- Revisar o passo a passo de instalação em uma máquina limpa;
- Publicar uma demonstração online, caso o projeto seja preparado para deploy.

## Autoria

Projeto acadêmico desenvolvido por:

- [Shelly Leal](https://github.com/ShellyLeal05)
- [Eduardo Izidório](https://github.com/EhoKira)

---

*Este repositório é apresentado como parte do portfólio acadêmico de desenvolvimento de software.*
