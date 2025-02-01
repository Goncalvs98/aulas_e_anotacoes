As **estruturas de dados** são fundamentais na programação, pois permitem armazenar, organizar e manipular informações de forma eficiente. Escolher a estrutura certa pode melhorar o desempenho e a escalabilidade dos sistemas.

---

## **📌 1️⃣ O que são Estruturas de Dados?**

São maneiras de organizar e armazenar dados na memória para serem manipulados de forma eficiente.

📏 **Tipos principais:**

- **Lineares** → Arranjos (vetores), listas, filas, pilhas
- **Não lineares** → Árvores, grafos
- **Baseadas em tabelas** → Tabelas hash

📌 **Exemplo:**  
Um site de e-commerce usa **listas** para armazenar produtos no carrinho, **filas** para processar pedidos e **tabelas hash** para buscar clientes rapidamente.

---

## **🧱 2️⃣ Estruturas Lineares**

### **🔹 Vetores (Arrays)**

📌 **Definição:** Estrutura mais simples, armazena elementos em **posições contíguas** da memória.

📌 **Características:**  
✅ Acesso rápido por índice (**O(1)**)  
✅ Tamanho fixo (em muitas linguagens)  
❌ Inserção e remoção são lentas (**O(n)**)

📌 **Exemplo em Python:**

```python
arr = [10, 20, 30, 40]
print(arr[2])  # Saída: 30
```

📌 **Exemplo em C++ (Arduino):**

```cpp
int valores[4] = {10, 20, 30, 40};
Serial.println(valores[2]);  // Saída: 30
```

---

### **🔹 Listas Ligadas (Linked List)**

📌 **Definição:** Coleção de nós, onde cada nó contém **um valor e um ponteiro** para o próximo nó.

📌 **Características:**  
✅ Inserção e remoção eficientes (**O(1)**)  
❌ Acesso mais lento que arrays (**O(n)**)

📌 **Exemplo em Python:**

```python
class Node:
    def __init__(self, dado):
        self.dado = dado
        self.proximo = None

# Criando nós
n1 = Node(10)
n2 = Node(20)
n1.proximo = n2  # Ligando nós
```

📌 **Uso:**

- Implementação de **pilhas e filas**
- Sistemas que exigem inserção e remoção frequentes

---

### **🔹 Pilhas (Stacks) 📚**

📌 **Definição:** Estrutura **LIFO** (**Último a Entrar, Primeiro a Sair**).

📌 **Operações principais:**

- **push(x)** → Adiciona elemento no topo (**O(1)**)
- **pop()** → Remove o topo (**O(1)**)
- **peek()** → Consulta o topo (**O(1)**)

📌 **Exemplo em Python:**

```python
pilha = []
pilha.append(10)  # push
pilha.append(20)
print(pilha.pop())  # pop (Saída: 20)
```

📌 **Uso:**

- Histórico de navegação
- Funções recursivas

---

### **🔹 Filas (Queues) 🎫**

📌 **Definição:** Estrutura **FIFO** (**Primeiro a Entrar, Primeiro a Sair**).

📌 **Operações principais:**

- **enqueue(x)** → Insere elemento no fim (**O(1)**)
- **dequeue()** → Remove o primeiro elemento (**O(1)**)

📌 **Exemplo em Python (com `deque`)**

```python
from collections import deque

fila = deque()
fila.append(10)  # enqueue
fila.append(20)
print(fila.popleft())  # dequeue (Saída: 10)
```

📌 **Uso:**

- Processamento de tarefas
- Impressoras

---

## **🌳 3️⃣ Estruturas Não Lineares**

### **🔹 Árvores (Trees) 🌳**

📌 **Definição:** Estrutura hierárquica composta de **nós e conexões (arestas)**.

📏 **Tipos:**  
✅ **Árvore Binária** → Cada nó tem até **dois filhos**  
✅ **Árvore de Busca Binária (BST)** → Elementos ordenados, busca eficiente  
✅ **Árvores Balanceadas (AVL, Red-Black)** → Garantem eficiência nas operações

📌 **Exemplo em Python:**

```python
class No:
    def __init__(self, dado):
        self.dado = dado
        self.esq = None
        self.dir = None

raiz = No(10)
raiz.esq = No(5)
raiz.dir = No(15)
```

📌 **Uso:**

- Banco de dados (B-Trees)
- Sistemas de arquivos

---

### **🔹 Grafos (Graphs) 🕸**

📌 **Definição:** Conjunto de **vértices (nós)** conectados por **arestas (ligações)**.

📏 **Tipos:**  
✅ **Direcionados** → Ligações com direção específica  
✅ **Não Direcionados** → Ligações bidirecionais  
✅ **Ponderados** → Arestas têm peso

📌 **Exemplo em Python (com dicionário):**

```python
grafo = {
    'A': ['B', 'C'],
    'B': ['A', 'D'],
    'C': ['A', 'D'],
    'D': ['B', 'C']
}
```

📌 **Uso:**

- Redes sociais
- Algoritmos de caminhos mínimos (**Dijkstra, A***).

---

## **🗃 4️⃣ Estruturas Baseadas em Tabelas**

### **🔹 Tabelas Hash (Dicionários) 🔑**

📌 **Definição:** Usa uma **função hash** para mapear chaves em valores.

📌 **Características:**  
✅ Busca rápida **O(1)**  
✅ Uso eficiente da memória  
❌ Colisões podem ocorrer

📌 **Exemplo em Python:**

```python
dicionario = {"nome": "Ana", "idade": 25}
print(dicionario["nome"])  # Saída: Ana
```

📌 **Uso:**

- Indexação rápida
- Cache de dados

---

## **📈 5️⃣ Complexidade das Estruturas**

|Estrutura|Inserção|Remoção|Busca|
|---|---|---|---|
|**Array**|O(1) / O(n)|O(n)|O(1)|
|**Lista Ligada**|O(1)|O(1)|O(n)|
|**Pilha**|O(1)|O(1)|O(1)|
|**Fila**|O(1)|O(1)|O(n)|
|**Árvore BST**|O(log n)|O(log n)|O(log n)|
|**Tabela Hash**|O(1)|O(1)|O(1)|

📌 **Resumo:**

- **Para buscas rápidas** → **Tabelas hash**
- **Para inserções e remoções rápidas** → **Listas ligadas**
- **Para organização hierárquica** → **Árvores**

---
