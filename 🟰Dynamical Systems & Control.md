## 📌 **1. Definição da Transformada de Laplace**

A Transformada de Laplace de uma função \( f(t) \), definida para \( t ≥ 0 \), é expressa como:

$$
F(s) = \mathcal{L}\{ f(t) \} = \int_0^{\infty} e^{-st} f(t) dt, \quad \text{para } s \in \mathbb{C}
$$

Essa transformação mapeia funções do domínio do tempo para o domínio complexo \( s \), sendo amplamente utilizada na resolução de equações diferenciais ordinárias (EDOs) e no estudo de sistemas dinâmicos.
A teoria desenvolvida por Laplace permite empregar métodos para soluções de equações algébricas para resolver equações diferenciais lineares invariantes no tempo.

---

## 📌 **2. Transformada Inversa de Laplace**

A Transformada Inversa de Laplace permite recuperar \( f(t) \) a partir de \( F(s) \):

$$
 f(t) = \mathcal{L}^{-1} \{ F(s) \} = \frac{1}{2\pi i} \int_{\sigma - i\infty}^{\sigma + i\infty} e^{st} F(s) ds
$$

Na prática, utilizamos métodos como **decomposição em frações parciais** e **tabelas de transformadas** para determinar \( f(t) \).

---

## 📌 **3. Propriedades Fundamentais**

| Função no tempo $$f(t)$$ | Transformada de Laplace $$F(S)$$  |
| ------------------------ | --------------------------------- |
| $$\delta(t)$$            | $$1$$                             |
| $$1$$                    | $$\frac{1}{s}$$                   |
| $$t^n$$                  | $$\frac{n!}{s^{n+1}}$$            |
| $$e^{at}$$               | $$\frac{1}{s-a}$$                 |
| $$ t^n e^{-at} $$        | $$ \frac{{n!}}{(s+a)^{n+1}} $$    |
| $$\sin(bt)$$             | $$\frac{b}{s^2 + b^2}$$           |
| $$\cos(bt)$$             | $$\frac{s}{s^2 + b^2}$$           |
| $$t\sin(bt)$$            | $$\frac{2b}{(s^2 + b^2)^2}$$      |
| $$t\cos(bt)$$            | $$\frac{s^2-b^2}{(s^2 + b^2)^2}$$ |
| $$u(t - a)$$             | $$\frac{e^{-as}}{s}$$             |

| Propriedade                        | Expressão Matemática                                                     |
| ---------------------------------- | ------------------------------------------------------------------------ |
| **Linearidade**                    | $$\mathcal{L} \{ a f(t) + b g(t) \} = aF(s) + bG(s)$$                    |
| **Derivação no Tempo**             | $$\mathcal{L} \{ f'(t) \} = sF(s) - f(0)$$                               |
| **Derivada Segunda**               | $$\mathcal{L} \{ f''(t) \} = s^2 F(s) - s f(0) - f'(0)$$                 |
| **Integração**                     | $$\mathcal{L} \{ \int_0^t f(\tau) d\tau \} = \frac{F(s)}{s}$$ |
| **Multiplicação por \( e^{at} \)** | $$\mathcal{L} \{ e^{at} f(t) \} = F(s - a)$$                             |
| **Deslocamento no Tempo**          | $$\mathcal{L} \{ u(t - a) f(t - a) \} = e^{-as} F(s)$$                   |
| **Convolução**                     | $$\mathcal{L} \{ f * g \} = F(s) G(s)$$                                  |

---

## 📌 **4. Teorema do valor final**

Para analisar a resposta de um sistema em regime estacionário aplica-se o teorema do valor final que é definido por:

$$
\lim_{ t \to \infty } f(t)=\lim_{ s \to 0 } F(S) 
$$

Se uma transformada de Laplace é multiplicada por "s", o valor do produto fazendo "s" tender a zero é o valor da transformada inversa com "t" tendendo a infinito.

Onde f(t) é uma função qualquer no domínio do tempo.

$$
f(0^+)=\lim_{ t \to 0 } f(t)=\lim_{ S \to \infty } S F(S)  
$$

Se uma transformada de Laplace é multiplicada por “s”, o valor do produto fazendo “s” tender a infinito é o valor da transformada inversa com “t” tendendo a zero.

---

## 📌 **5. Decomposição em Frações Parciais**

Quando \( F(s) \) é uma função racional, podemos utilizar **frações parciais** para encontrar sua inversa:

1. Fatoramos o denominador de \( F(s) \).
2. Expressamos \( F(s) \) como soma de frações simples.
3. Determinamos os coeficientes resolvendo um sistema linear.
4. Aplicamos a Transformada Inversa de Laplace.

Exemplo:

Dado $$F(s) = \frac{5}{(s+2)(s+3)}$$
buscamos coeficientes \( A \) e \( B \) tais que:

$$ \frac{5}{(s+2)(s+3)} = \frac{A}{s+2} + \frac{B}{s+3} $$

#### Resolvendo A:

$$
A = \frac{5}{(S+2)(S+3)}(S+3); onde: S+3=0\to S=-3
$$

$$
A=\frac{5}{-3+2}\to A=-5
$$

$$
A = \frac{5}{(S+2)(S+3)}(S+3); onde: S+3=0\to S=-3
$$
#### Resolvendo B:
$$
B = \frac{5}{(S+2)(S+3)}(S+2); onde: S+2=0\to S=-2
$$

$$
B=\frac{5}{-2+3}\to A=5
$$
#### Portanto:
$$
 \frac{5}{(s+2)(s+3)} = \frac{-5}{s+2} + \frac{5}{s+3} 
$$
$$
f(t)=-5e^{-2t}+5e^{-3t}
$$

---

## 📌 **6. Aplicações**

### **Solução de Equações Diferenciais**

Exemplo 1:

$$
\begin{equation}
    \frac{d^2 y(t)}{dt^2} + 1.7 \frac{d y(t)}{dt} + 0.5 y(t) = 0.1
\end{equation}
$$

Tomando a transformada de Laplace:

$$
\begin{equation}
    s^2 Y(s) + 1.7s Y(s) + 0.5 Y(s) = \frac{0.1}{s}
\end{equation}
$$

$$
\begin{equation}
    Y(s) (s^2 + 1.7s + 0.5) = \frac{0.1}{s}
\end{equation}
$$

$$
\begin{equation}
    Y(s) = \frac{0.1}{s (s^2 + 1.7s + 0.5)}
\end{equation}
$$

Resolvendo as raízes da equação característica:

$$
\begin{equation}
    \lambda = \frac{-1.7 \pm \sqrt{(1.7)^2 - 4(0.5)}}{2}
\end{equation}
$$

$$
\begin{equation}
    \lambda = \frac{-1.7 \pm 0.94}{2} = -1.32, -0.38
\end{equation}
$$

$$
\begin{equation}
    Y(s) = \frac{0.1}{s(s+1.32)(s+0.38)}
\end{equation}
$$

Expandindo em frações parciais:

$$
\begin{equation}
    \frac{0.1}{s(s+1.32)(s+0.38)} = \frac{A_1}{s} + \frac{A_2}{s+1.32} + \frac{A_3}{s+0.38}
\end{equation}
$$

$$
A_{1}=\frac{0.1}{s(s+1.32)(s+0.38)} \times s; s=0 → A_{1}=\frac{0.1}{(1.32)(0.38)} = \frac{0.1}{0.5}=0.2
$$

$$
A_{2}=\frac{0.1}{s(s+1.32)(s+0.38)} \times (s+1.32); s=-1.32 → A_{2}=\frac{0.1}{(-1.32)(-0.94)} = \frac{0.1}{1.24}=0.08
$$

$$
A_{3}=\frac{0.1}{s(s+1.32)(s+0.38)} \times (s+0.38); s=-0.38 → A_{3}=\frac{0.1}{(-0.38)(0.94)} = -\frac{0.1}{0.36}=-0.28
$$

Após a resolução dos coeficientes:

$$
\begin{equation}
    Y(s) = \frac{0.2}{s} + \frac{0.08}{s+1.32} - \frac{0.28}{s+0.38}
\end{equation}
$$

Tomando a transformada inversa:
$$
\begin{equation}
    y(t) = 0.2 + 0.08 e^{-1.32t} - 0.28 e^{-0.38t}
\end{equation}
$$

Verificação para \( t = 0 \):

$$
\begin{equation}
    y(0) = 0.2 + 0.08 - 0.28 = 0
\end{equation}
$$

Verificação para ( t = ∞):

$$
y(\infty) = 0.2 + 0.08 e^{-\infty} - 0.28 e^{-\infty}=0.2 + 0 + 0 = 0.2
$$

Ex2:
Função de transferência:

$$
\begin{equation}
    F(s) = \frac{2s^2}{2s^2 + 4s + 1}
\end{equation}
$$

Analisando o valor inicial:

$$
\begin{equation}
    VI = \lim_{s \to \infty} s F(s) = \lim_{s \to \infty} s\frac{2s^2}{2s^2 + 4s + 1}
\end{equation}
$$

$$
\begin{equation}
    VI = \frac{2s}{2 + \frac4s + \frac{1}{s^2}} = \frac{\infty}{2}= +\infty
\end{equation}
$$

$$
VF = \lim_{s \to 0} s F(s) = \lim_{s \to 0} s\frac{2s^2}{2s^2 + 4s + 1}
$$

$$
VF=\frac{2(0)^3}{2(0)^2 + 4(0) + 1} = \frac{0}{1}=0
$$

---

## **📌 7. Função de Transferência**

**Exemplo 2:**

$$
F(s) = \frac{2s^2}{2s^2 + 4s + 1}
$$

Analisando o valor inicial:

$$
VI = \lim_{s \to \infty} s F(s) = \lim_{s \to \infty} s\frac{2s^2}{2s^2 + 4s + 1} = +\infty
$$

E o valor final:

$$
VF = \lim_{s \to 0} s F(s) = \lim_{s \to 0} s\frac{2s^2}{2s^2 + 4s + 1} = 0
$$

---

## 📌 **8. Diagrama de Blocos**
![[Pasted image 20250407173358.png]]

$$
G(S)=\frac{Y(S)→S. Saída}{U(S)→S. Entrada}=\frac{\delta Saída}{\delta Entrada}
$$

$$
\frac{Y(S)}{U(S)}=G(S)→Y(S)=G(S)U(S)
$$

$$
G(S)=\frac{a_{0}S+a_{1}S²+a_{2}S^3+\dots+a_{m-1}S^m}{b_{0}S+b_{1}S²+b_{2}S^3+\dots+b_{n-1}S^n}
$$

Exemplo: A seguinte função 

$$
F(S)=\frac{S+0.1}{(S+1)(S+2)(S+3)}
$$

Tem os seguintes zeros:

$$
S+0.1=0→S=-0.1
$$

E os seguinte polos:

$$
S+1=0→S=-1
$$

$$
S+2=0→S=-2
$$

$$
S+3=0→S=-3
$$

![[Pasted image 20250407175044.png]]
- Se todos os polos estão no semi-plano real-negativo, o sistema é estável
- Se pelo menos um polo estiver no semi-plano real-posistovo, o sistema é instável

---
## Série

![[Pasted image 20250407175551.png]]

$$
U(S)G_{1}(S)G_{2}(S)=Y(S)
$$

---

## Paralelo
![[Pasted image 20250407180336.png]]

$$
U(S)[G_{1}(S)±G_{2}(S)±G_{3}(S)]=Y(S)
$$

---

## Realimentação

![[Pasted image 20250407173111.png]]

$$
C=(R±CH)G
$$

$$
C=RG±CHG
$$

$$
C±CHG=RG
$$

$$
C(1±HG)=RG
$$

$$
\frac{C}{R}=\frac{G}{1±GH}
$$

---
#### Exercícios

##### 1.

![[Pasted image 20250410171146.png]]

##### 2.

![[Pasted image 20250410171848.png]]
