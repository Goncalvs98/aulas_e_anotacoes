### 🔹 **Como Adicionar CSS**

Existem três formas principais de aplicar CSS a um documento HTML:

#### 1️⃣ **CSS Externo (Recomendado)**

```html
<link rel="stylesheet" href="styles.css">
```

```css
/* styles.css */
body {
    background-color: #f0f0f0;
    font-family: Arial, sans-serif;
}
```

#### 2️⃣ **CSS Interno (Dentro do HTML)**

```html
<style>
    body {
        background-color: lightgray;
    }
</style>
```

#### 3️⃣ **CSS Inline (Evite quando possível)**

```html
<p style="color: blue; font-size: 20px;">Texto Azul</p>
```

---

## 📌 **Seletores Essenciais**

|Seletor|Descrição|Exemplo|
|---|---|---|
|`*`|Seleciona todos os elementos|`* { margin: 0; }`|
|`elemento`|Seleciona todos os elementos do tipo|`p { color: red; }`|
|`#id`|Seleciona um elemento pelo ID|`#titulo { font-size: 24px; }`|
|`.classe`|Seleciona todos os elementos com a classe|`.destaque { background: yellow; }`|
|`[atributo]`|Seleciona elementos com atributo específico|`input[type="text"] { border: 1px solid black; }`|
|`elemento1, elemento2`|Seleciona múltiplos elementos|`h1, h2 { color: green; }`|
|`elemento elemento`|Seleciona elementos dentro de outro|`div p { color: blue; }`|
|`elemento > elemento`|Seleciona filhos diretos|`ul > li { font-weight: bold; }`|

---

## 🎨 **Propriedades Básicas**

### 🏗 **Box Model (Modelo de Caixa)**

Cada elemento HTML é tratado como uma caixa com:

- **width (largura)**
- **height (altura)**
- **padding (espaço interno)**
- **border (borda)**
- **margin (espaço externo)**

```css
.box {
    width: 200px;
    height: 100px;
    padding: 10px;
    border: 2px solid black;
    margin: 20px;
}
```

---

### 📌 **Cores e Background**

```css
body {
    background-color: #f5f5f5; /* Cor de fundo */
    color: #333; /* Cor do texto */
}

.container {
    background-image: url('imagem.jpg'); /* Fundo com imagem */
    background-size: cover;
    background-position: center;
}
```

---

### 📝 **Tipografia**

```css
p {
    font-family: Arial, sans-serif;
    font-size: 16px;
    font-weight: bold; /* negrito */
    font-style: italic; /* itálico */
    text-align: center;
    text-transform: uppercase; /* Maiúsculas */
    text-decoration: underline;
    line-height: 1.5;
}
```

---

### 🔲 **Bordas e Sombras**

```css
.box {
    border: 2px solid black;
    border-radius: 10px; /* Cantos arredondados */
    box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.3); /* Sombra */
}
```

---

### 📐 **Display e Position**

|Propriedade|Descrição|
|---|---|
|`display: block;`|Elemento ocupa toda a largura disponível|
|`display: inline;`|Elemento ocupa apenas o espaço do conteúdo|
|`display: flex;`|Ativa o **Flexbox** (alinhamento avançado)|
|`display: grid;`|Ativa o **CSS Grid** (layout avançado)|

```css
.container {
    display: flex;
    justify-content: center; /* Centraliza horizontalmente */
    align-items: center; /* Centraliza verticalmente */
}
```

### **Posicionamento (`position`)**

|Valor|Descrição|
|---|---|
|`static`|Padrão|
|`relative`|Posiciona relativo à posição original|
|`absolute`|Posiciona em relação ao elemento pai|
|`fixed`|Fixa na tela (exemplo: menus fixos)|
|`sticky`|Fixa apenas quando rolar a página|

```css
.menu {
    position: fixed;
    top: 0;
    width: 100%;
    background: white;
}
```

---

### 🏗 **Layouts com Flexbox**

```css
.container {
    display: flex;
    justify-content: space-between;
    align-items: center;
}
```

|Propriedade|Descrição|
|---|---|
|`justify-content: center;`|Centraliza horizontalmente|
|`justify-content: space-between;`|Espaçamento igual entre elementos|
|`align-items: center;`|Alinha elementos verticalmente|

---

### 📊 **CSS Grid (Layouts Avançados)**

```css
.container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 10px;
}
```

---

## 🎭 **Transições e Animações**

### 🎬 **Transições**

```css
button {
    background: blue;
    color: white;
    transition: background 0.3s ease;
}

button:hover {
    background: red;
}
```

### 🎡 **Animações**

```css
@keyframes girar {
    from { transform: rotate(0deg); }
    to { transform: rotate(360deg); }
}

.icone {
    animation: girar 2s linear infinite;
}
```

---

## 🌍 **Responsividade (Mobile First)**

```css
@media (max-width: 768px) {
    body {
        background-color: lightblue;
    }
}
```

---

## 🔥 **Boas Práticas**

✅ **Organizar CSS externo** para facilitar manutenção  
✅ **Usar classes em vez de IDs** para reutilização  
✅ **Utilizar rem/em** ao invés de px para acessibilidade  
✅ **Manter um código limpo e indentado**
