## 🏗 **Instalação e Configuração**

### **1️⃣ Instalando Python**

Baixe e instale Python em [python.org](https://www.python.org/downloads/).

### **2️⃣ Verificando a Instalação**

```sh
python --version
```

ou, dependendo da configuração:

```sh
python3 --version
```

### **3️⃣ Criando e Executando um Script Python**

Crie um arquivo `script.py` e adicione:

```python
print("Olá, Python!")
```

Execute com:

```sh
python script.py
```

---

## 🏷 **Variáveis e Tipos de Dados**

```python
nome = "Carlos"    # String
idade = 25         # Inteiro
altura = 1.75      # Float
ativo = True       # Booleano
lista = [1, 2, 3]  # Lista
tupla = (4, 5, 6)  # Tupla
dicionario = {"nome": "Ana", "idade": 30}  # Dicionário
nulo = None        # NoneType
```

### **Verificando Tipo de Variável**

```python
print(type(nome))  # <class 'str'>
```

---

## 🔢 **Operadores**

```python
# Aritméticos
soma = 10 + 5  # 15
divisao = 10 / 3  # 3.3333
exponenciacao = 2 ** 3  # 8

# Comparação
print(10 == 10)  # True
print(5 != 3)  # True

# Lógicos
print(True and False)  # False
print(True or False)  # True
print(not True)  # False
```

---

## 🔄 **Estruturas Condicionais**

```python
idade = 18

if idade >= 18:
    print("Maior de idade")
elif idade >= 16:
    print("Pode votar, mas não dirigir")
else:
    print("Menor de idade")
```

### **Operador Ternário**

```python
status = "Maior" if idade >= 18 else "Menor"
```

---

## 🔁 **Loops (Laços de Repetição)**

### **For Loop**

```python
for i in range(5):
    print(i)  # 0, 1, 2, 3, 4
```

### **While Loop**

```python
contador = 0
while contador < 5:
    print(contador)
    contador += 1
```

### **Loop em Listas**

```python
frutas = ["Maçã", "Banana", "Laranja"]

for fruta in frutas:
    print(fruta)
```

---

## 🎒 **Funções**

```python
def saudacao(nome: str) -> str:
    return f"Olá, {nome}!"

print(saudacao("Carlos"))
```

### **Funções com Parâmetros Padrão e Opcionais**

```python
def mensagem(texto="Olá", nome=None):
    return f"{texto}, {nome}" if nome else texto
```

---

## 📦 **Listas e Dicionários**

### **Listas**

```python
numeros = [10, 20, 30]
numeros.append(40)  # Adiciona
numeros.pop()  # Remove último elemento
print(numeros[0])  # 10
```

### **Dicionários**

```python
pessoa = {"nome": "Ana", "idade": 30}
print(pessoa["nome"])  # Ana
pessoa["cidade"] = "São Paulo"
```

---

## 🏗 **Classes e Objetos**

```python
class Pessoa:
    def __init__(self, nome, idade):
        self.nome = nome
        self.idade = idade

    def saudacao(self):
        return f"Olá, meu nome é {self.nome}"

pessoa1 = Pessoa("Carlos", 35)
print(pessoa1.saudacao())
```

### **Herança**

```python
class Estudante(Pessoa):
    def __init__(self, nome, idade, curso):
        super().__init__(nome, idade)
        self.curso = curso
```

---

## 🌐 **Manipulação de Arquivos**

```python
# Escrever em um arquivo
with open("arquivo.txt", "w") as arquivo:
    arquivo.write("Olá, arquivo!")

# Ler um arquivo
with open("arquivo.txt", "r") as arquivo:
    conteudo = arquivo.read()
    print(conteudo)
```

---

## 🌍 **Requisições HTTP (Usando requests)**

```sh
pip install requests
```

```python
import requests

resposta = requests.get("https://jsonplaceholder.typicode.com/posts")
dados = resposta.json()
print(dados[:2])  # Mostra os 2 primeiros itens
```

---

## 🏎 **Programação Assíncrona (Async/Await)**

```python
import asyncio

async def tarefa():
    print("Iniciando...")
    await asyncio.sleep(2)
    print("Finalizado!")

asyncio.run(tarefa())
```

---

## 🧹 **Tratamento de Erros**

```python
try:
    numero = int(input("Digite um número: "))
    print(f"Você digitou {numero}")
except ValueError:
    print("Erro: Não é um número válido!")
finally:
    print("Fim do programa")
```

---

## 🛠 **Pacotes e Módulos**

### **Criando um Módulo (`meu_modulo.py`)**

```python
def somar(a, b):
    return a + b
```

### **Importando o Módulo**

```python
from meu_modulo import somar
print(somar(5, 3))  # 8
```

---

## 🕹 **Virtual Environments**

```sh
python -m venv meu_ambiente
source meu_ambiente/bin/activate  # Linux/macOS
meu_ambiente\Scripts\activate  # Windows
```

---

## 🔥 **Boas Práticas**

✅ **Usar `venv` para ambientes isolados**  
✅ **Escrever código modular e reutilizável**  
✅ **Evitar `global` e usar funções para encapsular lógica**  
✅ **Usar f-strings (`f"Olá, {nome}!"`) ao invés de `.format()`**  
✅ **Manter um código limpo e bem indentado**
