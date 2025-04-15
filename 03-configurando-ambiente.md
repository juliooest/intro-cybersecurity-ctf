# 💻 Configurando Seu Ambiente para CTF

Antes de cair nos desafios, bora garantir que você tá com tudo configurado certinho.

## 📌 1. Instalação do Kali Linux

O Kali Linux é o sistema operacional mais usado pra pentesting e CTF, porque já vem pronto com tudo o que você precisa.

### Como instalar?

- Baixe aqui: [Kali Linux Downloads](https://www.kali.org/get-kali/#kali-virtual-machines)
- Recomendo baixar a versão pronta pra VirtualBox:
- [VirtualBox Images](https://www.kali.org/get-kali/#kali-virtual-machines)

### Configurando no VirtualBox:

- Abra o VirtualBox.
- Vá em `Arquivo > Importar Appliance`.
- Escolha a imagem `.ova` que você baixou.
- Siga as instruções até finalizar.

---

## 🔌 2. Conectando na VPN da plataforma

Tanto **TryHackMe** quanto **HackTheBox** exigem VPN pra acessar suas máquinas.

- Acesse sua conta no TryHackMe ou HackTheBox.
- Baixe o arquivo `.ovpn` na seção de acesso VPN.

### Conexão VPN (Linux):

Abra o terminal e rode:

```
sudo openvpn caminho-do-seu-arquivo.ovpn
```
Mantenha esse terminal aberto enquanto fizer os desafios!


🛠️ 3. Atualização e instalação de ferramentas essenciais

O Kali já vem com tudo que você precisa, mas sempre é bom atualizar e garantir as ferramentas mais recentes.

Abra um terminal no Kali e rode:
```
sudo apt update && sudo apt upgrade -y
```
(vai demorar um pouquinho)

Ferramentas essenciais pra garantir:

    Nmap (scanner de rede)

    Gobuster (descobrir diretórios)

    Burp Suite (ferramenta web)

    Metasploit (exploits automáticos)]

No terminal digite:
```
sudo apt install gobuster
```
(Todas as outras ferramentas já vêm pré-instaladas no Kali.)

📂 4. Organize seu workspace

É útil criar pastas separadas pros desafios que você resolver:
```
mkdir ~/CTFs
mkdir ~/CTFs/TryHackMe
mkdir ~/CTFs/HackTheBox
```
Cada desafio novo, crie uma pasta específica pra manter tudo organizado.

🚀 Testando tudo rapidão:

Verifique se tá tudo ok fazendo um scan rápido no IP do desafio que você vai usar.
```
nmap -sV IP_DO_DESAFIO
```
Se tudo estiver funcionando e mostrando resultados, parabéns, seu ambiente tá pronto!

Agora vamos pro próximo capítulo aprender comandos básicos do Linux que vão facilitar sua vida nos desafios.

