## 🔹 **Instalação e Configuração**

### **1️⃣ Instalando o TypeScript**

```sh
npm install -g typescript
```

### **2️⃣ Criando um Arquivo TypeScript**

```ts
// arquivo.ts
const mensagem: string = "Olá, TypeScript!";
console.log(mensagem);
```

### **3️⃣ Compilando o Código**

```sh
tsc arquivo.ts
```

Isso gera um `arquivo.js` que pode ser executado no Node ou no navegador.

---

## 🎯 **Vantagens do TypeScript**

✅ Tipagem estática  
✅ Melhor autocompletar no VSCode  
✅ Código mais seguro e fácil de manter  
✅ Suporte a ES6+ e features avançadas

---

## 📌 **Tipos Básicos**

### **Declaração de Variáveis**

```ts
let nome: string = "Carlos";
let idade: number = 25;
let ativo: boolean = true;
let lista: number[] = [1, 2, 3];
let tupla: [string, number] = ["João", 30]; // Tupla
```

### **Any, Null, Undefined e Void**

```ts
let qualquerCoisa: any = "Pode ser qualquer coisa"; 
let semRetorno: void = undefined;
let valorNulo: null = null;
let indefinido: undefined;
```

---

## 🏷 **Funções**

### **Função com Tipos**

```ts
function saudacao(nome: string): string {
    return `Olá, ${nome}!`;
}
```

### **Função com Parâmetros Opcionais e Default**

```ts
function mensagem(texto: string = "Olá", nome?: string): string {
    return nome ? `${texto}, ${nome}!` : texto;
}
```

### **Funções Assíncronas**

```ts
async function buscarDados(): Promise<string> {
    return "Dados carregados!";
}
```

---

## 📦 **Objetos e Interfaces**

### **Criando Objetos Tipados**

```ts
let usuario: { nome: string; idade: number } = {
    nome: "Ana",
    idade: 28
};
```

### **Interfaces**

```ts
interface Usuario {
    nome: string;
    idade: number;
    ativo?: boolean; // Propriedade opcional
}

let pessoa: Usuario = {
    nome: "Carlos",
    idade: 35
};
```

---

## 🔄 **Enums**

```ts
enum Status {
    Pendente,
    EmAndamento,
    Concluido
}

let tarefa: Status = Status.EmAndamento;
```

---

## 🎭 **Type Aliases e Union Types**

### **Alias de Tipo**

```ts
type ID = string | number;

let userId: ID = 123; 
let postId: ID = "abc123";
```

### **Union Type**

```ts
function imprimirID(id: string | number): void {
    console.log(`ID: ${id}`);
}
```

---

## 🏗 **Classes e Herança**

```ts
class Pessoa {
    nome: string;
    idade: number;

    constructor(nome: string, idade: number) {
        this.nome = nome;
        this.idade = idade;
    }

    saudacao(): string {
        return `Olá, meu nome é ${this.nome}`;
    }
}
```

### **Herança**

```ts
class Estudante extends Pessoa {
    curso: string;

    constructor(nome: string, idade: number, curso: string) {
        super(nome, idade);
        this.curso = curso;
    }

    detalhes(): string {
        return `${this.nome} está no curso de ${this.curso}`;
    }
}
```

---

## 🔐 **Modificadores de Acesso**

|Modificador|Descrição|
|---|---|
|`public`|Acessível de qualquer lugar|
|`private`|Acessível apenas dentro da classe|
|`protected`|Acessível na classe e subclasses|
|`readonly`|Apenas leitura|

```ts
class Conta {
    private saldo: number = 0;

    depositar(valor: number): void {
        this.saldo += valor;
    }

    consultarSaldo(): number {
        return this.saldo;
    }
}
```

---

## 🏎 **Generics**

```ts
function identidade<T>(valor: T): T {
    return valor;
}

console.log(identidade<string>("Teste"));
console.log(identidade<number>(10));
```

---

## 🔄 **Interfaces vs. Type Aliases**

|**Feature**|**Interface**|**Type Alias**|
|---|---|---|
|Expansível|✅ Sim|❌ Não|
|Usado para Objetos|✅ Sim|✅ Sim|
|Union Types|❌ Não|✅ Sim|

```ts
// Interface
interface Carro {
    marca: string;
    modelo: string;
}

// Type Alias
type Carro2 = {
    marca: string;
    modelo: string;
};
```

---

## 🌐 **Manipulação do DOM**

```ts
const botao = document.querySelector("#meuBotao") as HTMLButtonElement;

botao.addEventListener("click", () => {
    console.log("Botão clicado!");
});
```

---

## 🕸 **Requisições HTTP com Fetch e Async/Await**

```ts
async function obterDados(): Promise<void> {
    const resposta = await fetch("https://jsonplaceholder.typicode.com/posts");
    const dados = await resposta.json();
    console.log(dados);
}
```

---

## 🔥 **Boas Práticas**

✅ **Usar `const` e `let` ao invés de `var`**  
✅ **Usar interfaces para estruturar dados**  
✅ **Evitar `any` sempre que possível**  
✅ **Organizar código em módulos**  
✅ **Usar Generics para flexibilidade**
