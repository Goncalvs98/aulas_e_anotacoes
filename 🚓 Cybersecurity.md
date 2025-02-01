# **Estudo e Aplicação dos Conceitos de Segurança, Criptografia e Firewall**

## **1. Segurança da Informação**

A Segurança da Informação visa proteger dados contra acessos não autorizados, uso indevido, modificação ou destruição.

### **1.1 Princípios Fundamentais**

- **Confidencialidade:** Protege a informação contra acessos não autorizados.
- **Integridade:** Garante que os dados não sejam alterados de forma indevida.
- **Disponibilidade:** Assegura que os dados estejam acessíveis quando necessários.
- **Autenticidade:** Garante a identidade de usuários e dispositivos.
- **Irretratabilidade:** Evita que uma parte negue a autoria de uma transação.

## **2. Criptografia**

A criptografia protege dados convertendo informações em um formato ilegível para terceiros.

### **2.1 Tipos de Criptografia**

- **Simétrica (Chave Secreta):** Usa a mesma chave para criptografar e descriptografar (AES, DES).
- **Assimétrica (Chave Pública e Privada):** Utiliza um par de chaves (RSA, ECC).
- **Hashing:** Converte dados em um hash irreversível (SHA-256, MD5).

### **2.2 Protocolos de Criptografia**

- **SSL/TLS:** Protege comunicações na web.
- **IPSec:** Garante segurança em redes privadas virtuais (VPNs).
- **PGP:** Usado para criptografia de e-mails.

## **3. Firewall e Controle de Acesso**

Os firewalls controlam o tráfego de rede com base em regras predefinidas.

### **3.1 Tipos de Firewall**

- **Filtragem de pacotes:** Analisa cabeçalhos de pacotes.
- **Firewall de estado:** Monitora conexões ativas.
- **Firewall de aplicação:** Controla acessos a nível de aplicação.

### **3.2 Listas de Controle de Acesso (ACLs)**

Permitem ou bloqueiam tráfego com base em critérios como IP, porta e protocolo.

Exemplo de ACL em Cisco:

```
access-list 100 permit ip any 192.168.1.0 0.0.0.255
```

## **4. Protocolos de Roteamento Avançado**

Roteadores utilizam protocolos para trocar informações sobre caminhos na rede.

### **4.1 OSPF (Open Shortest Path First)**

- Baseado no algoritmo de Dijkstra.
- Melhor para redes grandes.
- Métrica baseada em custo.

### **4.2 RIP (Routing Information Protocol)**

- Usa contagem de saltos como métrica.
- Melhor para redes pequenas.

### **4.3 EIGRP (Enhanced Interior Gateway Routing Protocol)**

- Protocolo híbrido (distância vetorial e estado de link).
- Métrica baseada em largura de banda e latência.

## **5. Configuração de VLANs, Proxy e VPN**

### **5.1 VLANs (Redes Locais Virtuais)**

Segmentam redes físicas em lógicas para aumentar segurança.

Exemplo de configuração de VLAN em Cisco:

```
interface FastEthernet0/1
switchport mode access
switchport access vlan 10
```

### **5.2 Proxy**

Intermedia acessos entre usuários e servidores, filtrando conteúdo.

### **5.3 VPN (Virtual Private Network)**

Cria conexões seguras em redes públicas.

Exemplo de configuração de VPN IPSec:

```
crypto isakmp policy 10
 encr AES
 hash SHA
 group 2
```

## **6. Ferramentas de Defesa e Ataque**

### **6.1 Ferramentas de Defesa**

- **Snort:** IDS/IPS de código aberto.
- **Suricata:** Monitora tráfego de rede.
- **Wireshark:** Analisador de pacotes.

### **6.2 Ferramentas de Ataque**

- **Nmap:** Scanner de redes.
- **Metasploit:** Framework de pentest.
- **John the Ripper:** Quebra de senhas.

## **7. Testes de Penetração (Pentest)**

Pentests avaliam segurança identificando vulnerabilidades.

### **7.1 Etapas do Pentest**

1. **Coleta de informação** (reconhecimento passivo e ativo).
2. **Enumeração de serviços** (identifica serviços e vulnerabilidades).
3. **Exploração** (testes práticos de invasão).
4. **Pós-exploração** (manutenção de acesso e extração de informações).

### **7.2 Ferramentas de Pentest**

- **Burp Suite:** Testes de segurança web.
- **Aircrack-ng:** Testes em redes Wi-Fi.

## **8. Conclusão**

A segurança da informação é essencial para proteger dados e infraestrutura. O estudo de criptografia, firewalls, VLANs e VPNs, aliado ao uso de ferramentas de defesa e ataque, é fundamental para manter sistemas seguros.