# Survival Kit de Criptografia 🔐

### 📌 1. Conceitos Básicos
| Termo             | Definição                          |
|-----------------|----------------------------------|
| Criptografia    | Ciência de proteger informações através de codificação. |
| Chave           | Informação usada para cifrar ou decifrar dados. |
| Criptografia Simétrica | Mesma chave para cifrar e decifrar. |
| Criptografia Assimétrica | Chaves diferentes para cifrar (pública) e decifrar (privada). |
| Hash            | Função que gera um resumo fixo de dados (irreversível). |

---

### 🔑 2. Tipos de Criptografia

#### Criptografia Simétrica
| Algoritmo | Descrição | Tamanho da Chave |
|-----------|----------|-----------------|
| AES       | Padrão atual mais seguro | 128, 192, 256 bits |
| DES       | Antigo padrão (inseguro hoje) | 56 bits |
| RC4       | Fluxo rápido, mas considerado inseguro | Variável |

#### Criptografia Assimétrica
| Algoritmo | Descrição | Uso |
|-----------|----------|-----|
| RSA       | Baseado em números primos | Assinaturas digitais, chaves públicas |
| ECC       | Criptografia mais leve e segura | IoT, Certificados digitais |
| Diffie-Hellman | Troca segura de chaves | VPNs |

#### Hashing
| Algoritmo | Tamanho | Uso |
|-----------|--------|-----|
| SHA-256   | 256 bits | Blockchain, Senhas |
| MD5       | 128 bits (Inseguro) | Checksums antigos |
| bcrypt    | Variável + Salt | Armazenamento seguro de senhas |

---

### 🔥 3. Ferramentas
| Ferramenta   | Função         | Uso                  |
|-------------|---------------|---------------------|
| OpenSSL     | Criptografia e Assinaturas | Criação de certificados |
| GPG         | Criptografia de arquivos | Criptografia de emails |
| Hashcat     | Quebra de Hashes | Teste de força de senhas |
| VeraCrypt   | Criptografia de disco | Proteção de arquivos |

---

### 🔍 4. Técnicas de Criptografia
| Técnica               | Descrição                  |
|----------------------|---------------------------|
| Criptografia por Substituição | Substitui caracteres por outros (Cifra de César) |
| Criptografia por Transposição | Reordena os caracteres |
| Steganografia        | Oculta mensagens dentro de imagens ou áudio |
| Assinatura Digital    | Garante integridade e autenticidade de mensagens |

---

### 🔐 5. Segurança
- **Salts**: Evita ataques de Rainbow Table em Hashes.
- **IV (Initialization Vector)**: Evita padrões em mensagens cifradas.
- **PFS (Perfect Forward Secrecy)**: Gera chaves únicas por sessão.
- **TLS**: Criptografia em comunicações web.

---

### 🚨 6. Ataques Comuns
| Ataque              | Descrição                  | Proteção       |
|-------------------|--------------------------|-------------|
| Brute Force       | Teste de todas combinações | Senhas fortes + Bcrypt |
| Man-in-the-Middle | Interceptação de dados    | TLS + VPN    |
| Replay Attack     | Reenvio de pacotes antigos | Nonces       |
| Rainbow Table     | Hash pré-computado       | Hash + Salt  |

---

### 🧠 Mentalidade de um Criptógrafo
> "Se você acha que sua criptografia é inquebrável, você apenas não tentou quebrá-la o suficiente."

---

### 🌐 Dicas
- Sempre use bibliotecas bem testadas (OpenSSL, PyCryptodome).
- Nunca implemente seus próprios algoritmos criptográficos do zero.
- Prefira **AES-256 + SHA-256** para a maioria das aplicações.
- Use **bcrypt ou Argon2** para armazenar senhas.

---

### 🔗 Links Úteis
- [Cryptography Playground](https://cryptopals.com/)
- [CyberChef](https://gchq.github.io/CyberChef/)
- [Hashcat](https://hashcat.net/)
- [OpenSSL](https://www.openssl.org/)
