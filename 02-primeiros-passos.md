# 🛠️ Primeiros Passos no Mundo dos CTFs

Chega de enrolação. Vamos direto ao que interessa: como começar de verdade no Capture The Flag (CTF).

## ✅ Escolhendo sua plataforma: TryHackMe ou HackTheBox?

- **[TryHackMe](https://tryhackme.com/)**: Fácil pra iniciantes. Labs guiados passo a passo, ótimos pra quem tá aprendendo do zero.
- **[HackTheBox](https://www.hackthebox.com/)**: Mais hardcore. Máquinas realistas e sem muita ajuda. Ótimo pra evoluir rápido.

Minha sugestão:  
**Comece pelo TryHackMe** pra ganhar confiança, depois parta pro HackTheBox.

---

## 🔧 O que você precisa antes de começar?

### 1. **Sistema Operacional Linux**
- O ideal é o **[Kali Linux](https://www.kali.org/get-kali/)**, feito especialmente pra cybersecurity.
- Instala ele numa VM ([VirtualBox](https://www.virtualbox.org/) ou [VMware](https://www.vmware.com/products/workstation-player.html)) ou rode direto via [WSL no Windows](https://learn.microsoft.com/pt-br/windows/wsl/install).

### 2. **VPN (conexão com as plataformas)**
- Tanto o TryHackMe quanto o HackTheBox exigem que você conecte numa VPN específica pra acessar os desafios.
- Baixa a VPN diretamente na plataforma:
  - [TryHackMe - Access page](https://tryhackme.com/access)
  - [HackTheBox - VPN Access](https://app.hackthebox.com/starting-point)

### 3. **Ferramentas essenciais (já inclusas no Kali)**
- **Terminal Linux** (seu melhor amigo!)
- **Nmap** (scanner de rede e portas abertas)
- **Metasploit Framework** (exploits prontos)
- **Gobuster e dirsearch** (pra achar diretórios ocultos)
- **BurpSuite** (testar segurança de apps web)

---

## 🚀 Conectando na VPN pela primeira vez

### Exemplo TryHackMe:

Baixou seu arquivo `.ovpn`? Ótimo!

```
sudo openvpn seu-arquivo.ovpn
```

Se conectou? Testa no terminal rapidinho:

```
ping 10.10.10.10
```

Se o ping funcionar, parabéns! Você já tá pronto pra começar o primeiro desafio.

📍 Bora começar?

Com ambiente configurado, agora é partir pro primeiro desafio:

    Se escolheu TryHackMe:
    https://tryhackme.com/room/introtoctfs

    Se escolheu HackTheBox:
    https://app.hackthebox.com/starting-point

Segue no próximo capítulo, que vamos detalhar mais sobre configuração e uso das ferramentas.
