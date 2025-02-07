### 🔹 **Instalação e Configuração**

1. **Baixar e instalar Node.js:** [Node.js Oficial](https://nodejs.org/)
2. **Gerenciadores de versão (recomendado):**
    - [nvm (Linux/macOS)](https://github.com/nvm-sh/nvm)
    - [nvm-windows](https://github.com/coreybutler/nvm-windows)

---

### 🔹 **Pacotes Essenciais**

✔ **Gerenciador de Pacotes:**

- `npm` (vem com o Node.js)
- `yarn` → `npm install -g yarn`
- `pnpm` (alternativa mais rápida) → `npm install -g pnpm`

✔ **Frameworks e Ferramentas Úteis:**

- **Express.js** → Servidor web minimalista → `npm install express`
- **Fastify** → Alternativa performática ao Express → `npm install fastify`
- **dotenv** → Carregar variáveis de ambiente → `npm install dotenv`
- **cors** → Para lidar com CORS → `npm install cors`
- **nodemon** → Auto-reload do servidor → `npm install -g nodemon`

✔ **Banco de Dados:**

- **PostgreSQL:** `npm install pg`
- **MongoDB:** `npm install mongoose`
- **SQLite:** `npm install sqlite3`
- **Prisma ORM:** `npm install prisma`

✔ **Autenticação e Segurança:**

- **bcryptjs** → Hash de senhas → `npm install bcryptjs`
- **jsonwebtoken (JWT)** → Autenticação → `npm install jsonwebtoken`
- **helmet** → Segurança extra para APIs → `npm install helmet`
- **express-rate-limit** → Proteção contra ataques de força bruta → `npm install express-rate-limit`

✔ **Testes e Debugging:**

- **Jest** → Testes unitários → `npm install jest`
- **Supertest** → Testes de API → `npm install supertest`
- **ESLint + Prettier** → Formatação e linting
    
    ```sh
    npm install -D eslint prettier eslint-config-prettier eslint-plugin-prettier
    ```
    

---

### 🔹 **Ferramentas de Desenvolvimento**

🛠 **Extensões do VS Code:**

- 🔹 [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- 🔹 [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
- 🔹 [REST Client](https://marketplace.visualstudio.com/items?itemName=humao.rest-client) (Alternativa ao Postman)

🖥 **Monitoramento de Logs:**

- [PM2](https://pm2.keymetrics.io/) → `npm install -g pm2`

---

### 🔹 **Comandos Úteis**

📌 **Iniciar um novo projeto**

```sh
npm init -y
```

📌 **Rodar um script com nodemon**

```sh
nodemon server.js
```

📌 **Rodar testes com Jest**

```sh
npm test
```

📌 **Executar um servidor local no Node.js (exemplo básico)**

```javascript
const express = require('express');
const app = express();

app.get('/', (req, res) => {
  res.send('Hello, Node.js!');
});

app.listen(3000, () => {
  console.log('Servidor rodando na porta 3000');
});
```

---

### 🔹 **Livros e Materiais Extras**

📖 **Documentação Oficial:** [Node.js Docs](https://nodejs.org/en/docs/)  
📘 **Livro:** "Node.js Design Patterns" – Mario Casciaro  
📘 **Livro:** "The Node.js Handbook" – Flavio Copes
