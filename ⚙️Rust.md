## 📦 **Configuração do Ambiente**
1. Instale Rust e Cargo:  
   ```sh
   curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
   ```
2. Atualize o Rust:  
   ```sh
   rustup update
   ```
3. Verifique a instalação:  
   ```sh
   rustc --version && cargo --version
   ```
4. Adicione targets (se precisar compilar para outra plataforma):  
   ```sh
   rustup target add <target-triple>
   ```
   Exemplo para WebAssembly:  
   ```sh
   rustup target add wasm32-unknown-unknown
   ```

---

## 🚀 **Comandos Essenciais do Cargo**
- Criar um novo projeto:
  ```sh
  cargo new meu_projeto
  ```
- Rodar o código:
  ```sh
  cargo run
  ```
- Compilar sem rodar:
  ```sh
  cargo build
  ```
- Compilar no modo release:
  ```sh
  cargo build --release
  ```
- Rodar testes:
  ```sh
  cargo test
  ```
- Formatar código:
  ```sh
  cargo fmt
  ```
- Analisar código e pegar erros comuns:
  ```sh
  cargo clippy
  ```

---

## 🏗️ **Estrutura Básica de um Programa em Rust**
```rust
fn main() {
    println!("Olá, Rustacean!");
}
```

---

## 📌 **Principais Tipos de Dados**
```rust
let inteiro: i32 = 42;
let flutuante: f64 = 3.14;
let booleano: bool = true;
let caractere: char = 'R';
let tupla: (i32, f64, char) = (10, 3.14, 'x');
let array: [i32; 3] = [1, 2, 3];
```

---

## 🧵 **Controle de Fluxo**
### If-Else:
```rust
let x = 10;
if x > 5 {
    println!("Maior que 5");
} else {
    println!("Menor ou igual a 5");
}
```

### Match (Switch do Rust):
```rust
let cor = "azul";
match cor {
    "vermelho" => println!("A cor é vermelha"),
    "azul" => println!("A cor é azul"),
    _ => println!("Cor desconhecida"),
}
```

### Looping:
```rust
for i in 0..5 {
    println!("Número: {}", i);
}

let mut contador = 0;
while contador < 5 {
    println!("Contador: {}", contador);
    contador += 1;
}

loop {
    println!("Loop infinito");
    break;
}
```

---

## 🔗 **Ownership, Borrowing e Lifetimes (Conceitos Essenciais)**
### **Ownership**
```rust
fn main() {
    let s = String::from("Olá");
    consumir_string(s);
    // println!("{}", s); // Erro: valor movido!
}

fn consumir_string(texto: String) {
    println!("{}", texto);
}
```

### **Borrowing (Empréstimo)**
```rust
fn main() {
    let s = String::from("Olá");
    imprimir_string(&s);
    println!("{}", s); // Funciona porque não movemos o valor, apenas emprestamos
}

fn imprimir_string(texto: &String) {
    println!("{}", texto);
}
```

### **Lifetimes (Tempo de Vida)**
```rust
fn maior<'a>(s1: &'a str, s2: &'a str) -> &'a str {
    if s1.len() > s2.len() { s1 } else { s2 }
}
```

---

## 📂 **Trabalhando com Arquivos**
```rust
use std::fs::File;
use std::io::prelude::*;

fn main() -> std::io::Result<()> {
    let mut arquivo = File::create("output.txt")?;
    arquivo.write_all(b"Olá, Rust!")?;
    Ok(())
}
```

---

## 🔥 **Concorrência com Threads**
```rust
use std::thread;
use std::time::Duration;

fn main() {
    let handle = thread::spawn(|| {
        for i in 1..5 {
            println!("Thread: {}", i);
            thread::sleep(Duration::from_millis(500));
        }
    });

    handle.join().unwrap();
}
```

---

## 🌟 **Crates Essenciais**
Adicione as dependências no `Cargo.toml`:
```toml
[dependencies]
rand = "0.8" # Gerar números aleatórios
serde = { version = "1.0", features = ["derive"] } # Serialização
tokio = { version = "1", features = ["full"] } # Assíncrono
```

Exemplo usando a crate `rand`:
```rust
use rand::Rng;

fn main() {
    let mut rng = rand::thread_rng();
    let numero: i32 = rng.gen_range(1..=100);
    println!("Número aleatório: {}", numero);
}
```

---

## 📖 **Recursos Extras**
- [Rust Book (oficial)](https://doc.rust-lang.org/book/)
- [Rustlings (exercícios interativos)](https://github.com/rust-lang/rustlings)
- [Rust By Example](https://doc.rust-lang.org/stable/rust-by-example/)
- [Playground para testar código online](https://play.rust-lang.org/)
