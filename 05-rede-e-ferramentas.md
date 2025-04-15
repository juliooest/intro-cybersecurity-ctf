# 🌐 Redes e Ferramentas Essenciais em CTFs

Você não precisa virar engenheiro de redes, mas entender o básico já te coloca 10 passos na frente. Quase todo CTF envolve rede de algum jeito.

---

## 📡 Conceitos de Rede que você PRECISA entender

### 🔹 IP e Porta

- IP é o endereço do host na rede (tipo o CEP).
- Porta é como se fosse uma porta de entrada específica da casa (serviço).
  - Ex: `192.168.0.1:80` → porta 80 geralmente é um site (HTTP).

### 🔹 TCP vs UDP

- **TCP** = mais confiável, usado em web, FTP, SSH etc.
- **UDP** = mais rápido, usado em DNS, streaming, etc.

### 🔹 Ping e ICMP

- Usa o comando `ping` pra testar se o host tá online:

```
ping 10.10.10.10
```

🧰 Ferramentas que você vai usar SEMPRE (consideradas padrões para CTF's)
1. Nmap — Scanner de portas e serviços
```
nmap -sV -Pn 10.10.10.10
```
-sV: detecta versões dos serviços

-Pn: ignora ping (caso esteja bloqueado)

-A: ativa detecção de OS + scripts

Exemplo completo:
```
nmap -sC -sV -A -oN scan.txt 10.10.10.10
```


2. Netcat — Canivete suíço da rede
Pra abrir uma conexão reversa, escutar uma porta, ou mandar arquivos.

Escutar:
```
nc -lvnp 4444
```

Conectar:
```
nc 10.10.10.10 4444
```

3. Gobuster — Força bruta de diretórios em sites
```
gobuster dir -u http://10.10.10.10 -w /usr/share/wordlists/dirb/common.txt
```
Vai listar páginas e diretórios ocultos.


4. Burp Suite — Interceptar e modificar requisições HTTP
Use pra mexer nos parâmetros de um site e testar vulnerabilidades.

Já vem instalado no Kali.
Só abrir com:
```
burpsuite
```
Configura o navegador pra proxy 127.0.0.1:8080 e intercepta tudo.

5. Whois / nslookup / dig — Info sobre domínios
```
whois dominio.com
nslookup dominio.com
dig dominio.com
```
Úteis quando você pega um desafio que envolve DNS ou recon online.

6. curl — Faz requisições via terminal
```
curl http://10.10.10.10
curl -X POST -d "user=admin&pass=123" http://10.10.10.10/login
```

🚀 Checklist pro CTF:

✅ Scan de portas com Nmap
✅ Exploração web com Gobuster/Burp
✅ Comunicação com Netcat
✅ Coleta de info com whois/dig
✅ Testes manuais com curl ou browser

No próximo capítulo, bora partir pro teu primeiro desafio no TryHackMe. Tá na hora de meter a mão na massa.



