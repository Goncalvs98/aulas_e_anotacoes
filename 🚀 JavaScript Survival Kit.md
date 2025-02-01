### 🔹 **Como Adicionar JavaScript ao HTML**

#### 1️⃣ **Script Interno (Dentro do HTML)**

```html
<script>
    console.log("Olá, mundo!");
</script>
```

#### 2️⃣ **Script Externo (Recomendado)**

```html
<script src="script.js"></script>
```

```js
// script.js
console.log("Olá, mundo!");
```

#### 3️⃣ **Script no Head vs. no Body**

Colocar `<script>` no **final do `<body>`** ou usar `defer` no `<head>` para evitar que o JS bloqueie o carregamento da página.

```html
<script src="script.js" defer></script>
```

---

## 📌 **Variáveis e Constantes**

```js
var nome = "João";   // Variável global (evite usar)
let idade = 25;      // Variável local (recomendado)
const PI = 3.1415;   // Constante (não pode ser alterada)
```

---

## 🧮 **Tipos de Dados**

```js
let numero = 42;              // Number
let texto = "Olá";            // String
let verdade = true;           // Boolean
let lista = [1, 2, 3];        // Array
let pessoa = { nome: "Ana", idade: 30 }; // Objeto
let indefinido;               // undefined
let nulo = null;              // null
```

---

## ✨ **Operadores**

|Operador|Descrição|Exemplo|
|---|---|---|
|`+` `-` `*` `/` `%`|Aritméticos|`10 + 5 // 15`|
|`++` `--`|Incremento/Decremento|`x++`|
|`==` `!=`|Comparação (não verifica tipo)|`5 == "5" // true`|
|`===` `!==`|Comparação estrita (verifica tipo)|`5 === "5" // false`|
|`&&` `||!`|

---

## 🏷 **Estruturas Condicionais**

```js
let idade = 18;

if (idade >= 18) {
    console.log("Maior de idade");
} else {
    console.log("Menor de idade");
}

// Operador Ternário
let status = (idade >= 18) ? "Maior" : "Menor";
```

```js
let cor = "azul";

switch (cor) {
    case "azul":
        console.log("A cor é azul");
        break;
    case "vermelho":
        console.log("A cor é vermelha");
        break;
    default:
        console.log("Outra cor");
}
```

---

## 🔄 **Loops (Laços de Repetição)**

### **For**

```js
for (let i = 0; i < 5; i++) {
    console.log("Número " + i);
}
```

### **While**

```js
let contador = 0;
while (contador < 5) {
    console.log("Contador: " + contador);
    contador++;
}
```

### **ForEach (Arrays)**

```js
let lista = ["Maçã", "Banana", "Laranja"];

lista.forEach((fruta) => {
    console.log(fruta);
});
```

---

## 🎒 **Funções**

```js
function saudacao(nome) {
    return "Olá, " + nome;
}
console.log(saudacao("Carlos"));
```

### **Função Anônima**

```js
const soma = function (a, b) {
    return a + b;
};
console.log(soma(3, 7));
```

### **Arrow Function (ES6)**

```js
const multiplicar = (a, b) => a * b;
console.log(multiplicar(3, 4));
```

---

## 📦 **Objetos e Arrays**

### **Objeto**

```js
let pessoa = {
    nome: "Ana",
    idade: 30,
    falar: function () {
        console.log("Olá!");
    }
};

console.log(pessoa.nome);
pessoa.falar();
```

### **Array**

```js
let numeros = [10, 20, 30];

console.log(numeros[0]); // 10
numeros.push(40); // Adiciona ao final
numeros.pop(); // Remove o último elemento
```

---

## 🎭 **Manipulação do DOM**

### **Selecionando Elementos**

```js
let titulo = document.getElementById("titulo");
let paragrafo = document.querySelector(".paragrafo");
```

### **Modificando Elementos**

```js
titulo.innerText = "Novo Título";
paragrafo.style.color = "red";
```

### **Eventos**

```js
document.getElementById("btn").addEventListener("click", function () {
    alert("Botão clicado!");
});
```

---

## 🔗 **Local Storage**

Salvar e recuperar dados no navegador:

```js
localStorage.setItem("nome", "Carlos");
console.log(localStorage.getItem("nome"));
```

---

## 🌐 **Requisições HTTP (Fetch API)**

```js
fetch("https://jsonplaceholder.typicode.com/posts")
    .then(response => response.json())
    .then(data => console.log(data))
    .catch(error => console.error("Erro:", error));
```

---

## 🕒 **Promises e Async/Await**

```js
async function carregarDados() {
    try {
        let resposta = await fetch("https://jsonplaceholder.typicode.com/posts");
        let dados = await resposta.json();
        console.log(dados);
    } catch (erro) {
        console.error("Erro ao carregar:", erro);
    }
}
carregarDados();
```

---

## 🎭 **Destructuring e Spread Operator**

### **Destructuring**

```js
let pessoa = { nome: "Carlos", idade: 28 };
let { nome, idade } = pessoa;
console.log(nome, idade);
```

### **Spread Operator**

```js
let numeros = [1, 2, 3];
let copia = [...numeros, 4, 5];
console.log(copia);
```

---

## 🔥 **Boas Práticas**

✅ **Usar `let` e `const` em vez de `var`**  
✅ **Usar arrow functions sempre que possível**  
✅ **Evitar funções muito grandes** (manter código modular)  
✅ **Utilizar template literals ( ) ao invés de concatenar strings**  
✅ **Evitar manipular diretamente o DOM (usar frameworks como React)**
