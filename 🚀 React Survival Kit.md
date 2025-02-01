### 🔹 **Criar um Novo Projeto React**

#### Com Vite (recomendado - mais rápido e leve):

```bash
npm create vite@latest meu-projeto --template react
cd meu-projeto
npm install
npm run dev
```

#### Com Create React App (CRA) (mais pesado, mas tradicional):

```bash
npx create-react-app meu-projeto
cd meu-projeto
npm start
```

---

### 🔹 **Rodar o Projeto**

```bash
npm run dev  # Vite
npm start    # CRA
```

---

### 🔹 **Instalar Bibliotecas Essenciais**

```bash
npm install axios  # Requisições HTTP
npm install react-router-dom  # Rotas
npm install @reduxjs/toolkit react-redux  # Gerenciamento de estado com Redux
npm install styled-components  # Estilização
npm install tailwindcss  # Utilitário de CSS
```

---

### 🔹 **Gerenciar Dependências**

```bash
npm install pacote  # Instalar uma biblioteca
npm uninstall pacote  # Remover uma biblioteca
npm list  # Listar pacotes instalados
npm outdated  # Ver pacotes desatualizados
npm update  # Atualizar pacotes
```

---

### 🔹 **Criar Componentes Rapidamente**

Exemplo de um componente funcional simples:

```jsx
const MeuComponente = () => {
  return <h1>Olá, mundo!</h1>;
};
export default MeuComponente;
```

---

### 🔹 **Rotas no React**

```jsx
import { BrowserRouter, Routes, Route } from "react-router-dom";
import Home from "./Home";
import About from "./About";

function App() {
  return (
    <BrowserRouter>
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
      </Routes>
    </BrowserRouter>
  );
}

export default App;
```

---

### 🔹 **Build e Deploy**

```bash
npm run build  # Gera a versão otimizada para produção
```

Para servir localmente e testar o build:

```bash
npm install -g serve
serve -s dist  # Vite
serve -s build # CRA
```

---

### 🔹 **Ambientes e Variáveis**

Criar um arquivo `.env` na raiz do projeto e adicionar:

```plaintext
VITE_API_URL=https://api.exemplo.com  # Para Vite
REACT_APP_API_URL=https://api.exemplo.com  # Para CRA
```

Usar no código:

```js
const apiUrl = import.meta.env.VITE_API_URL; // Vite
const apiUrl = process.env.REACT_APP_API_URL; // CRA
```

---

### 🔹 **Extensões Úteis para VS Code**

- **ES7+ React/Redux/React-Native snippets** → Atalhos de código
- **Prettier** → Formatação automática
- **Tailwind CSS IntelliSense** → Sugestões para Tailwind
- **React Developer Tools** → Debugging no navegador
