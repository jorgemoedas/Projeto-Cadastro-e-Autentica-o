
# API de Autenticação com JWT

## 🔧 Tecnologias Utilizadas
- Node.js com TypeScript
- Express.js
- JWT (JSON Web Token)
- Bcrypt para hash de senhas
- PostgreSQL ou MySQL

## 📁 Estrutura de Diretórios
```
/src
├── controllers
├── middlewares
├── routes
├── services
├── models
└── utils
```

## 🚀 Endpoints da API

| Método | Rota        | Descrição                               |
|--------|-------------|-----------------------------------------|
| POST   | /usuarios   | Cadastro de novo usuário                |
| POST   | /login      | Autenticação e geração de token         |
| GET    | /perfil     | Retorna dados do usuário autenticado    |
| GET    | /logs       | Retorna logs do sistema (admin apenas)  |

## 🔐 Lógica de Autenticação
1. Usuário envia e-mail e senha para `/login`.
2. API valida credenciais e gera token JWT.
3. Front-end armazena o token.
4. Requisições protegidas usam o token no header `Authorization`.
5. Middleware valida o token antes de liberar acesso.

## 🔒 Segurança e LGPD
- Senhas são criptografadas com bcrypt.
- Tokens têm tempo de expiração.
- Usuários acessam apenas seus dados.
- Logs são restritos ao administrador.

## ▶️ Execução
```bash
npm install          # Instala as dependências
cp .env.example .env # Configure as variáveis de ambiente
npm run dev          # Inicia o servidor em modo desenvolvimento
```

API disponível em `http://localhost:3000` (por padrão).
