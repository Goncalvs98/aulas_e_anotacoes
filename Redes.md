### Survival Kit de Redes de Computadores 🔥💪

### 📌 1. Conceitos Básicos
| Termo                   | Definição                                               |
|--------------------------|-------------------------------------------------------|
| **IP (Internet Protocol)** | Endereço que identifica dispositivos em redes. IPv4 e IPv6. |
| **MAC Address**         | Identificação única da interface de rede (placa de rede). |
| **Gateway**             | Dispositivo que liga redes diferentes (roteador).       |
| **Subnet Mask**         | Define qual parte do IP é rede e qual parte é host.     |
| **DNS**                 | Traduz domínios (www.google.com) para IPs.             |

---

### 🛠️ 2. Comandos Essenciais

| Comando               | Descrição                      | Exemplo                 |
|-----------------------|--------------------------------|-----------------------|
| `ipconfig` (Windows)  | Mostra configuração de rede    | `ipconfig /all`       |
| `ifconfig` (Linux)    | Mostra config de rede          | `ifconfig eth0`       |
| `ping`               | Testa conexão com outro host    | `ping google.com`     |
| `tracert` (Windows)   | Rastreia rota dos pacotes      | `tracert google.com`   |
| `traceroute` (Linux)  | Mesmo que o tracert            | `traceroute google.com` |
| `netstat`            | Mostra conexões ativas         | `netstat -an`         |
| `nslookup`           | Resolve nome para IP           | `nslookup google.com`  |
| `nmap`               | Scanner de portas              | `nmap 192.168.0.1`    |
| `curl`               | Faz requisições HTTP           | `curl http://site.com` |
| `wireshark`          | Sniffer para análise de pacotes | Interface Gráfica     |

---

### ⚙️ 3. Modelo OSI (7 Camadas)
| Camada       | Função               | Exemplos                         |
|-------------|----------------------|----------------------------------|
| 1. Física   | Meio físico          | Cabo, Wi-Fi                    |
| 2. Enlace   | Comunicação entre nós | Ethernet, MAC                  |
| 3. Rede     | Roteamento          | IP, ICMP                       |
| 4. Transporte | Controle de Dados    | TCP, UDP                       |
| 5. Sessão   | Gerenciamento       | RPC, PPTP                      |
| 6. Apresentação | Criptografia, compressão | SSL, TLS                      |
| 7. Aplicação | Interface do Usuário | HTTP, FTP, SMTP               |

---

### 🔥 4. Protocolo TCP/IP
- **TCP**: Confiável (garante entrega)
- **UDP**: Não confiável (mais rápido)
  
| Camada TCP/IP | Equivalente OSI | Protocolos       |
|---------------|----------------|----------------|
| Aplicação    | 7, 6, 5       | HTTP, FTP, SMTP |
| Transporte   | 4             | TCP, UDP       |
| Rede        | 3             | IP, ICMP       |
| Enlace      | 2, 1          | Ethernet       |

---

### 🔑 5. Endereçamento IPv4
| Tipo            | Faixa               | Máscara        | Usado em          |
|----------------|---------------------|---------------|-----------------|
| Classe A       | 0.0.0.0 – 127.255.255.255 | 255.0.0.0   | Grandes redes    |
| Classe B       | 128.0.0.0 – 191.255.255.255 | 255.255.0.0 | Médias redes    |
| Classe C       | 192.0.0.0 – 223.255.255.255 | 255.255.255.0 | Pequenas redes |
| Classe D       | 224.0.0.0 – 239.255.255.255 | Multicast    | Streaming       |
| Classe E       | 240.0.0.0 – 255.255.255.255 | Reservado   | Pesquisa       |

---

### 🔌 6. Ferramentas de Rede
| Ferramenta    | Função                 | Onde Usar       |
|---------------|-----------------------|---------------|
| **Wireshark** | Analisador de pacotes | Troubleshooting |
| **Putty**     | SSH/Telnet           | Conexão remota |
| **Nmap**      | Scanner de portas    | Segurança       |
| **TCPDump**   | Sniffer CLI         | Linux          |
| **OpenVPN**   | VPN                 | Conexões seguras |

---

### 🔐 7. Segurança
- **Firewall**: Regras para permitir ou bloquear tráfego
- **VPN**: Criptografia para navegação segura
- **SSH**: Acesso remoto seguro
- **TLS/SSL**: Criptografia para sites

---

### 🚨 8. Diagnóstico de Rede
| Problema       | Solução                          |
|---------------|---------------------------------|
| IP inválido   | `ipconfig /renew` ou `dhclient`  |
| DNS não resolve | `nslookup site.com` + alterar DNS |
| Ping não responde | Verificar firewall e cabo     |
| Velocidade baixa | Testar via cabo e Wi-Fi       |

---

### 🎯 9. Endereços IPv4 Privados
| Classe | Faixa           | Uso      |
|-------|---------------|--------|
| A     | 10.0.0.0/8    | Grandes redes |
| B     | 172.16.0.0/12 | Redes médias |
| C     | 192.168.0.0/16 | Pequenas redes |

---

### 🔥 10. Dicas Ninja
- Use **Google DNS (8.8.8.8)** para melhorar a resolução de nomes.
- Sempre teste conexões usando **ping** antes de assumir que a rede está caída.
- Aprenda regex para usar filtros no **Wireshark**.
- Use **nmap** para testar portas abertas antes de qualquer troubleshooting.

---

### 🧠 Mentalidade de um Network Engineer
> "Se você pode pingar, mas não acessar o site, é DNS."  
> "Se você não pode pingar, mas pode acessar o site, é ICMP bloqueado."  
> "Se você não pode pingar e não pode acessar o site... bem-vindo ao inferno!"

---

### 🔥 Bônus: Sites para Testes
| Site           | Função          |
|---------------|---------------|
| https://www.speedtest.net/ | Teste de velocidade |
| https://dnsleaktest.com/   | Teste de vazamento DNS |
| https://whoer.net/        | Informações de IP público |

---
