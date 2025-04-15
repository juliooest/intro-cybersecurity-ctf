# 💀 Seu Primeiro CTF no HackTheBox

Agora que você já deu os primeiros passos no TryHackMe, é hora de subir um pouco o nível com o **HackTheBox (HTB)**. Aqui os desafios são menos guiados e mais próximos do mundo real.

---

## 🎯 1. Criando sua conta no HTB

- Acesse: [https://www.hackthebox.com/](https://www.hackthebox.com/)
- Crie uma conta (gratuita também)
- Confirma o e-mail
- Pronto pra começar

---

## 🔐 2. Comece pelo “Starting Point”

O **Starting Point** é perfeito pra quem tá começando, pois te dá máquinas com instruções passo a passo.

🔗 Acesse: [https://app.hackthebox.com/starting-point](https://app.hackthebox.com/starting-point)

---

## 🔌 3. Conectando na VPN

- Acesse: [https://app.hackthebox.com/htb/access](https://app.hackthebox.com/htb/access)
- Escolha o servidor mais próximo
- Baixe seu arquivo `.ovpn`
- Conecte com:

```
sudo openvpn nome-do-arquivo.ovpn
```
Mantém esse terminal aberto pra continuar conectado.


🧠 4. Entendendo o fluxo

Nas máquinas do HTB:

    Você liga a máquina (Start Machine)

    Recebe um IP da máquina virtual

    Escaneia ela com nmap

    Acha uma falha

    Explora a falha até pegar uma flag (ex: HTB{exemplo_de_flag})

🛠️ 5. Ferramentas que você vai usar

    Nmap: escaneamento inicial

    Gobuster / dirsearch: descobrir caminhos ocultos

    BurpSuite: interceptar requisições web

    Netcat: conexões reversas

    Enum4linux / smbclient: se tiver Samba

    Searchsploit: procurar vulnerabilidades conhecidas


⚠️ Diferença importante do TryHackMe
O HackTheBox não pega na sua mão. Aqui é você por você. As instruções são mínimas, o que te força a investigar de verdade.


✅ Missão do capítulo:

    Cria sua conta no HTB

    Acesse o Starting Point

    Conecta na VPN

    Escolhe uma máquina e tenta pegar sua primeira flag

No próximo capítulo, vamos falar de técnicas úteis que aparecem direto nos desafios: enumeração, brute force, exploit e muito mais.
