## 🏗 **Instalação e Configuração**

### **1️⃣ Instalando o .NET SDK**

Baixe e instale o .NET SDK em [dotnet.microsoft.com](https://dotnet.microsoft.com/download).

### **2️⃣ Criando um Projeto C#**

```sh
dotnet new console -n MeuProjeto
cd MeuProjeto
dotnet run
```

### **3️⃣ Compilando e Executando um Arquivo C#**

Crie um arquivo `program.cs` e adicione:

```csharp
using System;

class Program {
    static void Main() {
        Console.WriteLine("Olá, C#!");
    }
}
```

Compile e execute com:

```sh
dotnet run
```

---

## 🏷 **Variáveis e Tipos de Dados**

```csharp
string nome = "Carlos";
int idade = 25;
double altura = 1.75;
bool ativo = true;
char letra = 'C';
var linguagem = "C#"; // Inferência de tipo
```

---

## 🔢 **Operadores**

```csharp
// Aritméticos
int soma = 10 + 5;
double divisao = 10.0 / 3.0;
int modulo = 10 % 3;

// Comparação
bool igual = (10 == 10);
bool diferente = (5 != 3);

// Lógicos
bool resultado = (true && false) || !false;
```

---

## 🔄 **Estruturas Condicionais**

```csharp
if (idade >= 18) {
    Console.WriteLine("Maior de idade");
} else if (idade >= 16) {
    Console.WriteLine("Pode votar, mas não dirigir");
} else {
    Console.WriteLine("Menor de idade");
}

// Operador Ternário
string status = (idade >= 18) ? "Maior" : "Menor";
```

---

## 🔁 **Loops (Laços de Repetição)**

### **For Loop**

```csharp
for (int i = 0; i < 5; i++) {
    Console.WriteLine(i);
}
```

### **While Loop**

```csharp
int contador = 0;
while (contador < 5) {
    Console.WriteLine(contador);
    contador++;
}
```

### **Foreach Loop**

```csharp
string[] frutas = { "Maçã", "Banana", "Laranja" };
foreach (string fruta in frutas) {
    Console.WriteLine(fruta);
}
```

---

## 🎒 **Funções**

```csharp
static int Somar(int a, int b) {
    return a + b;
}

Console.WriteLine(Somar(3, 5)); // 8
```

### **Funções com Parâmetros Opcionais e Default**

```csharp
static void Saudacao(string nome = "Visitante") {
    Console.WriteLine($"Olá, {nome}!");
}
```

---

## 📦 **Arrays e Listas**

### **Arrays**

```csharp
int[] numeros = { 1, 2, 3, 4 };
Console.WriteLine(numeros[0]); // 1
```

### **Listas**

```csharp
using System.Collections.Generic;

List<string> nomes = new List<string> { "Ana", "Carlos" };
nomes.Add("Pedro");
nomes.Remove("Carlos");
Console.WriteLine(nomes.Count); // 2
```

---

## 🏗 **Classes e Objetos**

```csharp
class Pessoa {
    public string Nome { get; set; }
    public int Idade { get; set; }

    public void Saudacao() {
        Console.WriteLine($"Olá, meu nome é {Nome}");
    }
}

Pessoa p = new Pessoa { Nome = "Carlos", Idade = 30 };
p.Saudacao();
```

### **Herança**

```csharp
class Estudante : Pessoa {
    public string Curso { get; set; }
}
```

---

## 🔐 **Modificadores de Acesso**

|Modificador|Descrição|
|---|---|
|`public`|Acessível de qualquer lugar|
|`private`|Acessível apenas dentro da classe|
|`protected`|Acessível na classe e subclasses|
|`internal`|Acessível dentro do mesmo assembly|

```csharp
class Conta {
    private double saldo = 0;

    public void Depositar(double valor) {
        saldo += valor;
    }

    public double ConsultarSaldo() {
        return saldo;
    }
}
```

---

## 🔄 **Enums**

```csharp
enum Status {
    Pendente,
    EmAndamento,
    Concluido
}

Status tarefa = Status.EmAndamento;
```

---

## 🏎 **Generics**

```csharp
class Caixa<T> {
    public T Valor { get; set; }
}

Caixa<int> caixaInt = new Caixa<int> { Valor = 10 };
Caixa<string> caixaStr = new Caixa<string> { Valor = "Olá" };
```

---

## 🌍 **Manipulação de Arquivos**

```csharp
using System.IO;

// Escrever em um arquivo
File.WriteAllText("arquivo.txt", "Olá, arquivo!");

// Ler um arquivo
string conteudo = File.ReadAllText("arquivo.txt");
Console.WriteLine(conteudo);
```

---

## 🕸 **Requisições HTTP (Usando HttpClient)**

```csharp
using System.Net.Http;
using System.Threading.Tasks;

async Task<string> ObterDados() {
    using HttpClient client = new HttpClient();
    string resposta = await client.GetStringAsync("https://jsonplaceholder.typicode.com/posts");
    return resposta;
}
```

---

## 🏎 **Programação Assíncrona (Async/Await)**

```csharp
using System.Threading.Tasks;

async Task ExemploAsync() {
    await Task.Delay(2000);
    Console.WriteLine("Tarefa concluída!");
}

await ExemploAsync();
```

---

## 🧹 **Tratamento de Erros**

```csharp
try {
    int numero = int.Parse(Console.ReadLine());
    Console.WriteLine($"Você digitou {numero}");
} catch (FormatException) {
    Console.WriteLine("Erro: Não é um número válido!");
} finally {
    Console.WriteLine("Fim do programa");
}
```

---

## 🛠 **Namespaces e Módulos**

### **Criando um Namespace**

```csharp
namespace MeuApp {
    class Util {
        public static void Mensagem() {
            Console.WriteLine("Olá, Namespace!");
        }
    }
}
```

### **Usando um Namespace**

```csharp
using MeuApp;

Util.Mensagem();
```

---

## 🔥 **Boas Práticas**

✅ **Usar `var` apenas quando o tipo for óbvio**  
✅ **Nomear classes e métodos seguindo `PascalCase`**  
✅ **Usar `camelCase` para variáveis e parâmetros**  
✅ **Evitar métodos longos e código duplicado**  
✅ **Usar `async` para operações IO pesadas**

---
