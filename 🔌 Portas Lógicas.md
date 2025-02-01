As **portas lógicas** são os blocos fundamentais da eletrônica digital. Elas realizam operações booleanas e são a base para circuitos como **microcontroladores, processadores e sistemas embarcados**.

---

## 📌 **1️⃣ O que são Portas Lógicas?**

Portas lógicas são **circuitos digitais** que recebem **sinais de entrada (0 ou 1)** e produzem uma **saída (0 ou 1)** de acordo com uma regra lógica.

📏 **Estados possíveis:**

- **0** → Baixo (0V)
- **1** → Alto (5V, 3.3V ou outro nível lógico)

📏 **Exemplo de uso:**

- Em **Arduino e IoT**, as portas lógicas ajudam na **tomada de decisões**.
- Nos **processadores**, são a base para cálculos e operações lógicas.

---

## 🏗 **2️⃣ Principais Tipos de Portas Lógicas**

| Porta                    | Símbolo | Tabela Verdade                              |
| ------------------------ | ------- | ------------------------------------------- |
| **NOT** (Inversora)      | 🔄      | A → Q; 0 → 1; 1 → 0                         |
| **AND**                  | ✖       | A B → Q; 0 0 → 0; 0 1 → 0; 1 0 → 0; 1 1 → 1 |
| **OR**                   | ➕       | A B → Q; 0 0 → 0; 0 1 → 1; 1 0 → 1; 1 1 → 1 |
| **NAND** (NOT AND)       | 🚫✖     | A B → Q; 0 0 → 1; 0 1 → 1; 1 0 → 1; 1 1 → 0 |
| **NOR** (NOT OR)         | 🚫➕     | A B → Q; 0 0 → 1; 0 1 → 0; 1 0 → 0; 1 1 → 0 |
| **XOR** (OU Exclusivo)   | ⊕       | A B → Q; 0 0 → 0; 0 1 → 1; 1 0 → 1; 1 1 → 0 |
| **XNOR** (XOR Invertido) | 🚫⊕     | A B → Q; 0 0 → 1; 0 1 → 0; 1 0 → 0; 1 1 → 1 |

---

## 🔄 **3️⃣ Explicação das Portas**

### 🔹 **NOT (Inversora) 🔄**

**Descrição:** Inverte o valor da entrada.

📌 **Símbolo:**

```
    ─┬──  
 A ─▷|── Q  
    ─┴──  
```

📌 **Exemplo:**

- Entrada: **0** → Saída: **1**
- Entrada: **1** → Saída: **0**

📌 **Aplicação:**

- Inversão de sinais lógicos.
- Circuitos de controle.

---

### 🔹 **AND (E) ✖**

**Descrição:** A saída é **1** **somente se ambas as entradas forem 1**.

📌 **Símbolo:**

```
     ┌───┐  
 A ─▷|   |── Q  
 B ─▷|AND|  
     └───┘  
```

📌 **Exemplo:**

- 0 + 0 → 0
- 0 + 1 → 0
- 1 + 1 → 1

📌 **Aplicação:**

- Controle de motores: **Só liga quando dois sensores estão ativados**.

---

### 🔹 **OR (OU) ➕**

**Descrição:** A saída é **1 se pelo menos uma entrada for 1**.

📌 **Símbolo:**

```
     ┌───┐  
 A ─▷|   |── Q  
 B ─▷| OR|  
     └───┘  
```

📌 **Exemplo:**

- 0 + 0 → 0
- 0 + 1 → 1
- 1 + 1 → 1

📌 **Aplicação:**

- Sensores de alarme: **Dispara se qualquer sensor ativar**.

---

### 🔹 **NAND (Não-E) 🚫✖**

**Descrição:** **Inversão da porta AND** (tudo que era **1 vira 0** e vice-versa).

📌 **Símbolo:**

```
     ┌────┐  
 A ─▷|    |── Q  
 B ─▷|NAND|  
     └────┘  
```

📌 **Exemplo:**

- 0 + 0 → 1
- 0 + 1 → 1
- 1 + 1 → 0

📌 **Aplicação:**

- Circuitos de segurança: **Ativa um alarme quando uma condição não é atendida**.

---

### 🔹 **NOR (Não-OU) 🚫➕**

**Descrição:** **Inversão da porta OR**.

📌 **Símbolo:**

```
     ┌────┐  
 A ─▷|    |── Q  
 B ─▷| NOR|  
     └────┘  
```

📌 **Exemplo:**

- 0 + 0 → 1
- 0 + 1 → 0
- 1 + 1 → 0

📌 **Aplicação:**

- Circuitos de controle lógico.

---

### 🔹 **XOR (OU Exclusivo) ⊕**

**Descrição:** A saída é **1 apenas se as entradas forem diferentes**.

📌 **Símbolo:**

```
     ┌────┐  
 A ─▷|    |── Q  
 B ─▷| XOR|  
     └────┘  
```

📌 **Exemplo:**

- 0 + 0 → 0
- 0 + 1 → 1
- 1 + 1 → 0

📌 **Aplicação:**

- **Operações matemáticas** (soma binária).

---

### 🔹 **XNOR (XOR Invertido) 🚫⊕**

**Descrição:** A saída é **1 apenas se as entradas forem iguais**.

📌 **Símbolo:**

```
     ┌────┐  
 A ─▷|    |── Q  
 B ─▷|XNOR|  
     └────┘  
```

📌 **Exemplo:**

- 0 + 0 → 1
- 0 + 1 → 0
- 1 + 1 → 1

📌 **Aplicação:**

- **Comparadores de igualdade** em circuitos digitais.

---

## 🔌 **4️⃣ Aplicação Prática em Arduino**

### **Simulando uma Porta AND**

```cpp
int entrada1 = 2;
int entrada2 = 3;
int saida = 4;

void setup() {
    pinMode(entrada1, INPUT);
    pinMode(entrada2, INPUT);
    pinMode(saida, OUTPUT);
}

void loop() {
    int A = digitalRead(entrada1);
    int B = digitalRead(entrada2);
    digitalWrite(saida, A && B);
}
```

---

### **Criando um XOR com Transistores**

🔹 Um **XOR** pode ser criado com **4 transistores e resistores**.

📌 **Fórmula booleana do XOR:**

$Q= (A \cdot \overline{B}) + (\overline{A} \cdot B)$

---
