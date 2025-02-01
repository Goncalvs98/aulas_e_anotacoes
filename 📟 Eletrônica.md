A **eletrônica** é a base dos circuitos modernos, permitindo a criação de **Arduino, IoT, automação, microcontroladores e dispositivos inteligentes**. Este guia cobre desde os **conceitos básicos até aplicações práticas**.

---

## ⚡ **1️⃣ Diferença entre Eletricidade e Eletrônica**

🔹 **Eletricidade** → Trata do fluxo de corrente elétrica de forma **macro** (fios, motores, redes elétricas).  
🔹 **Eletrônica** → Trabalha com o **controle da eletricidade** em circuitos usando **componentes como resistores, transistores e microcontroladores**.

Exemplo:

- Ligar uma lâmpada → **Elétrica**
- Criar um dimmer para controlar o brilho → **Eletrônica**

---

## 📏 **2️⃣ Grandezas Elétricas Fundamentais**

### 🔹 **Tensão (V) – Voltagem**

É a **força** que empurra os elétrons pelo circuito.  
📏 **Unidade:** Volt (V)

**Exemplo:**

- Pilha: **1,5V**
- USB: **5V**
- Tomada: **127V ou 220V**

---

### 🔹 **Corrente (I)**

É o **fluxo de elétrons** pelo circuito.  
📏 **Unidade:** Ampere (A)

**Dois tipos principais:**  
✅ **Corrente Contínua (CC/DC)** – Usada em baterias e eletrônicos.  
✅ **Corrente Alternada (CA/AC)** – Usada em redes elétricas.

---

### 🔹 **Resistência (R)**

Oposição ao fluxo de corrente em um circuito.  
📏 **Unidade:** Ohm (Ω)

**Lei de Ohm:**

V=R×IV = R \times I

Exemplo: Se um LED suporta **20mA** e opera a **2V**, e usamos uma fonte de **5V**, qual resistência devemos usar?

R=5V−2V0.02A=150ΩR = \frac{5V - 2V}{0.02A} = 150Ω

---

### 🔹 **Potência (P)**

Indica a energia consumida por um dispositivo.  
📏 **Unidade:** Watt (W)

P=V×IP = V \times I

**Exemplo:**  
Se um motor funciona em **12V** e consome **2A**, sua potência será:

P=12V×2A=24WP = 12V \times 2A = 24W

---

## 🔩 **3️⃣ Principais Componentes Eletrônicos**

### 🔹 **Resistores**

**Aplicação:** Controlar corrente.
Limitam a corrente no circuito. Identificamos seu valor por **código de cores**.

⚪ Branco → 9
⚪ Cinza → 8
🟣 Violeta → 7
🔵 Azul → 6
🟢 Verde → 5
🟡 Amarelo → 4
🟠 Laranja → 3
🔴 Vermelho → 2 
🟤 Marrom → 1  
⚫ Preto → 0  

**Exemplo de código de cores (10kΩ):**  

🟤 Marrom → 1  
🟠 Laranja → 3

---

$1 \times 10^3$ = 10kΩ

---

### 🔹 **Capacitores**

Armazenam energia temporariamente.  
📏 **Unidade:** Farad (F)

**Tipos:**

- **Eletrolítico** (grande capacidade, polarizado)
- **Cerâmico** (pequena capacidade, não polarizado)

**Aplicação:**

- Filtros em fontes de alimentação.
- Estabilização de sinais.

---

### 🔹 **Diodos**

Permitem passagem de corrente apenas em um sentido.

📏 **Tipos Comuns:**

- **1N4007** – Retificação de corrente.
- **1N4148** – Uso em sinais de alta frequência.
- **LED** – Diodo emissor de luz.

---

### 🔹 **Transistores**

Funcionam como **chaves eletrônicas ou amplificadores**.

📏 **Tipos:**

- **BJT (BC548, TIP120)** – Controle de pequenos sinais.
- **MOSFET (IRF540, IRFZ44N)** – Controle de altas correntes.

**Exemplo de uso:**

- Acionar um motor com **TIP120**.

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

### 🔹 **Circuitos Integrados (CIs)**

São conjuntos de transistores, resistores e capacitores miniaturizados.

**Exemplos:**

- **555** – Temporizador usado em osciladores e PWM.
- **LM7805** – Regulador de tensão de **5V**.
- **ATmega328** – Microcontrolador do Arduino.

---

## 🏗 **4️⃣ Tipos de Circuitos**

### **Circuito em Série**

A corrente é a mesma para todos os componentes.

Rtotal=R1+R2+R3R_{total} = R_1 + R_2 + R_3

### **Circuito em Paralelo**

A tensão é a mesma, mas a corrente se divide.

1Rtotal=1R1+1R2\frac{1}{R_{total}} = \frac{1}{R_1} + \frac{1}{R_2}

---

## 🔌 **5️⃣ Fontes de Alimentação**

### **Transformadores e Fontes Lineares**

Convertem **220V/127V** em **12V, 5V, 3.3V**, mas dissipam calor.

### **Fontes Chaveadas**

Mais eficientes e compactas.

### **Baterias**

- **AA (1,5V)** – Pequenos dispositivos.
- **9V** – Eletrônica básica.
- **Lítio-Íon (3,7V)** – Smartphones e drones.
- **Chumbo-Ácido (12V)** – No-breaks e carros.

---

## 📟 **6️⃣ Aplicações Práticas**

### **🔹 Acendendo um LED com Arduino**

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

### **🔹 Medindo Temperatura com LM35**

```cpp
int sensor = A0;

void setup() {
    Serial.begin(9600);
}

void loop() {
    int leitura = analogRead(sensor);
    float temperatura = (leitura * 5.0 / 1023.0) * 100.0;
    Serial.print("Temperatura: ");
    Serial.print(temperatura);
    Serial.println("°C");
    delay(1000);
}
```

---

### **🔹 Controle de Motor DC com PWM**

```cpp
int motor = 9;

void setup() {
    pinMode(motor, OUTPUT);
}

void loop() {
    analogWrite(motor, 150);  // 60% da potência
    delay(2000);
    analogWrite(motor, 0);  // Desliga
    delay(2000);
}
```

---
