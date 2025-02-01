A **eletricidade** é a base da eletrônica e da automação, sendo essencial para quem trabalha com **Arduino, IoT, automação industrial e sistemas elétricos**. Neste guia, abordaremos os **princípios fundamentais da elétrica**, desde conceitos básicos até cálculos práticos.

---

## 🏗 **1️⃣ Conceitos Básicos de Eletricidade**

### 🔹 **O que é Eletricidade?**

A eletricidade é o **movimento dos elétrons** através de um condutor. Esse movimento gera **corrente elétrica**, que pode ser usada para alimentar circuitos e dispositivos.

### 🔹 **Carga Elétrica (Q)**

A carga elétrica é uma propriedade fundamental da matéria e pode ser **positiva (+)** ou **negativa (-)**. Ela é medida em **Coulombs (C)**.

### 🔹 **Tensão Elétrica (V) – Voltagem**

A **tensão elétrica**, ou **diferença de potencial (DDP)**, é a força que impulsiona os elétrons em um circuito.  
📏 **Unidade:** Volt (V)

**Exemplos:**

- Pilha AA: **1,5V**
- Tomada residencial no Brasil: **127V ou 220V**

### 🔹 **Corrente Elétrica (I)**

A **corrente elétrica** é o fluxo de elétrons em um circuito. Pode ser de dois tipos:  
✅ **Corrente Contínua (CC/DC)** – Usada em baterias, eletrônicos e Arduino.  
✅ **Corrente Alternada (CA/AC)** – Usada em redes elétricas residenciais e industriais.

📏 **Unidade:** Ampere (A)

### 🔹 **Resistência Elétrica (R)**

A **resistência** limita o fluxo de corrente em um circuito. Quanto maior a resistência, menor a corrente que passa.

📏 **Unidade:** Ohm (Ω)

**Exemplo:** Resistores são usados para limitar a corrente em LEDs e outros componentes.

---

## 🔢 **2️⃣ Lei de Ohm – Cálculo de Circuitos**

A **Lei de Ohm** é fundamental para calcular a relação entre tensão, corrente e resistência:

V=R×IV = R \times I

Onde:

- **V** = tensão (volts)
- **R** = resistência (ohms)
- **I** = corrente (amperes)

**Exemplo de cálculo:**  
Se temos uma resistência de **100Ω** e uma tensão de **5V**, qual será a corrente?

I=VR=5V100Ω=0.05A(50mA)I = \frac{V}{R} = \frac{5V}{100Ω} = 0.05A (50mA)

---

## ⚡ **3️⃣ Potência Elétrica**

A **potência elétrica (P)** mede a quantidade de energia consumida por um dispositivo.

P=V×IP = V \times I

📏 **Unidade:** Watt (W)

**Exemplo:**  
Se um motor opera com **12V** e consome **2A**, sua potência será:

P=12V×2A=24WP = 12V \times 2A = 24W

---

## 🔌 **4️⃣ Tipos de Circuitos Elétricos**

### 🔹 **Circuito em Série**

A corrente é a mesma para todos os componentes. A tensão é dividida entre eles.

Rtotal=R1+R2+R3R_{total} = R_1 + R_2 + R_3

**Exemplo:** Se temos três resistores de **10Ω** em série, a resistência total será:

Rtotal=10Ω+10Ω+10Ω=30ΩR_{total} = 10Ω + 10Ω + 10Ω = 30Ω

---

### 🔹 **Circuito em Paralelo**

A tensão é a mesma em todos os componentes. A corrente se divide entre eles.

1Rtotal=1R1+1R2+1R3\frac{1}{R_{total}} = \frac{1}{R_1} + \frac{1}{R_2} + \frac{1}{R_3}

**Exemplo:** Para dois resistores de **10Ω** em paralelo:

1Rtotal=110+110=210=15\frac{1}{R_{total}} = \frac{1}{10} + \frac{1}{10} = \frac{2}{10} = \frac{1}{5} Rtotal=5ΩR_{total} = 5Ω

---

## 🏠 **5️⃣ Rede Elétrica Residencial**

### 📌 **Tensão da Tomada**

No Brasil, a tensão pode ser **127V ou 220V**, dependendo da região.

### 📌 **Fios e Disjuntores**

- **Fase** – Fio que leva energia (marron, preto ou vermelho).
- **Neutro** – Retorno da corrente (azul).
- **Terra** – Proteção contra descargas elétricas (verde/amarelo).

### 📌 **Cálculo do Disjuntor**

Para calcular o disjuntor ideal, usamos:

I=PVI = \frac{P}{V}

**Exemplo:**  
Se temos um chuveiro de **5500W** em **220V**:

I=5500220=25AI = \frac{5500}{220} = 25A

Portanto, o disjuntor deve ser de **25A ou mais**.

---

## 🔋 **6️⃣ Baterias e Fontes de Alimentação**

### 🔹 **Tipos de Baterias**

- **Pilhas AA (1,5V)** – Pequenos dispositivos.
- **Baterias de 9V** – Eletrônicos simples.
- **Lítio-Íon (3,7V)** – Smartphones e drones.
- **Chumbo-Ácido (12V)** – Carros e sistemas solares.

---

## 🚀 **7️⃣ Aplicações Práticas na Eletrônica e Arduino**

### 🔹 **Ligando um LED no Arduino**

Se um LED suporta **20mA** e **2V**, qual o resistor necessário para usar em **5V**?

R=V−VLEDI=5V−2V0.02A=150ΩR = \frac{V - V_{LED}}{I} = \frac{5V - 2V}{0.02A} = 150Ω

```cpp
int led = 13;

void setup() {
    pinMode(led, OUTPUT);
}

void loop() {
    digitalWrite(led, HIGH);
    delay(1000);
    digitalWrite(led, LOW);
    delay(1000);
}
```

---

### 🔹 **Ligando um Motor com Transistor**

Motores precisam de mais corrente do que o Arduino pode fornecer. Um transistor (como o **TIP120**) pode ser usado como chave.

```cpp
int motor = 9;

void setup() {
    pinMode(motor, OUTPUT);
}

void loop() {
    analogWrite(motor, 255);  // Velocidade máxima
    delay(2000);
    analogWrite(motor, 0);  // Desliga
    delay(2000);
}
```

---


