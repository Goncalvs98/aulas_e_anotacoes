

O **Arduino** utiliza uma versão simplificada de **C++**, facilitando o desenvolvimento de projetos embarcados. Com ele, é possível **controlar sensores, motores, LEDs, displays e outros componentes eletrônicos**.

Este guia traz os principais conceitos e comandos de C++ para programar no Arduino!

---

## 🖥 **1️⃣ Estrutura Básica de um Programa Arduino**

Todo código Arduino possui **duas funções obrigatórias**:

```cpp
void setup() {
    // Configuração inicial (executado apenas 1 vez)
}

void loop() {
    // Código que roda continuamente
}
```

🔹 **setup()** – Usado para configurar pinos e iniciar comunicação serial.  
🔹 **loop()** – Código principal que roda em um loop infinito.

---

## 📌 **2️⃣ Variáveis e Tipos de Dados**

O Arduino suporta os principais tipos de variáveis do C++:

|Tipo|Descrição|Exemplo|
|---|---|---|
|`int`|Números inteiros|`int x = 10;`|
|`float`|Números decimais|`float y = 3.14;`|
|`char`|Caracteres|`char letra = 'A';`|
|`String`|Texto (cadeia de caracteres)|`String nome = "Arduino";`|
|`bool`|Verdadeiro ou falso|`bool ligado = true;`|

🔹 **Exemplo de uso:**

```cpp
int led = 13;  // Define o pino do LED como variável global
float temperatura = 25.5;  // Variável para armazenar temperatura
```

---

## 🔄 **3️⃣ Estruturas de Controle**

### 🔹 **Condicional `if-else`**

```cpp
int sensor = analogRead(A0);  

if (sensor > 500) {
    digitalWrite(13, HIGH);  // Liga o LED
} else {
    digitalWrite(13, LOW);  // Desliga o LED
}
```

### 🔹 **Laço `for` (Repetição com contador)**

```cpp
for (int i = 0; i < 10; i++) {
    Serial.println(i);  // Imprime números de 0 a 9
}
```

### 🔹 **Laço `while` (Repetição condicional)**

```cpp
int valor = 0;

while (valor < 5) {
    Serial.println(valor);
    valor++;
}
```

---

## 🔌 **4️⃣ Manipulação de Pinos**

O Arduino interage com componentes eletrônicos através dos **pinos digitais e analógicos**.

### **Saída Digital (`OUTPUT`)**

```cpp
int led = 13;

void setup() {
    pinMode(led, OUTPUT);  // Define o pino 13 como saída
}

void loop() {
    digitalWrite(led, HIGH);  // Liga o LED
    delay(1000);              // Espera 1 segundo
    digitalWrite(led, LOW);   // Desliga o LED
    delay(1000);              // Espera 1 segundo
}
```

### **Entrada Digital (`INPUT`)**

```cpp
int botao = 2;

void setup() {
    pinMode(botao, INPUT);  // Define o pino como entrada
}

void loop() {
    int estado = digitalRead(botao);  // Lê o estado do botão
    Serial.println(estado);
}
```

### **Leitura Analógica (`analogRead()`)**

```cpp
int sensor = A0;

void setup() {
    Serial.begin(9600);
}

void loop() {
    int valor = analogRead(sensor);  // Lê valor de 0 a 1023
    Serial.println(valor);
    delay(500);
}
```

### **Saída Analógica (`analogWrite()`) – PWM**

```cpp
int led = 9;

void setup() {
    pinMode(led, OUTPUT);
}

void loop() {
    for (int brilho = 0; brilho <= 255; brilho++) {
        analogWrite(led, brilho);
        delay(10);
    }
}
```

---

## 📡 **5️⃣ Comunicação Serial**

O Arduino pode se comunicar com o computador via **porta serial**.

### **Enviar dados para o PC (`Serial.println()`)**

```cpp
void setup() {
    Serial.begin(9600);  // Inicia comunicação serial
}

void loop() {
    Serial.println("Olá, Arduino!");
    delay(1000);
}
```

### **Receber dados do PC (`Serial.read()`)**

```cpp
void setup() {
    Serial.begin(9600);
}

void loop() {
    if (Serial.available() > 0) {  // Se há dados disponíveis
        char recebido = Serial.read();
        Serial.print("Recebi: ");
        Serial.println(recebido);
    }
}
```

---

## ⚙ **6️⃣ Funções em C++ para Arduino**

Funções permitem **organizar e reutilizar código**.

```cpp
void piscarLed(int pino, int tempo) {
    digitalWrite(pino, HIGH);
    delay(tempo);
    digitalWrite(pino, LOW);
    delay(tempo);
}

void loop() {
    piscarLed(13, 500);
}
```

---

## 🏗 **7️⃣ Estruturas Avançadas – Classes e Objetos**

O Arduino permite **programação orientada a objetos (OOP)** com classes e objetos.

### **Criando uma Classe para um LED**

```cpp
class LED {
  private:
    int pino;
  
  public:
    LED(int p) {
        pino = p;
        pinMode(pino, OUTPUT);
    }

    void ligar() {
        digitalWrite(pino, HIGH);
    }

    void desligar() {
        digitalWrite(pino, LOW);
    }
};

LED meuLed(13);  // Criando um objeto LED no pino 13

void loop() {
    meuLed.ligar();
    delay(1000);
    meuLed.desligar();
    delay(1000);
}
```

---

## 🚀 **Projetos Práticos com C++ no Arduino**

### 📡 **1️⃣ Controle de LED por Serial**

Acenda um LED digitando "1" no monitor serial e apague com "0".

```cpp
int led = 13;

void setup() {
    pinMode(led, OUTPUT);
    Serial.begin(9600);
}

void loop() {
    if (Serial.available()) {
        char comando = Serial.read();
        if (comando == '1') digitalWrite(led, HIGH);
        if (comando == '0') digitalWrite(led, LOW);
    }
}
```

---

### 🌡 **2️⃣ Termômetro com Sensor LM35**

Mostra a temperatura no monitor serial.

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
