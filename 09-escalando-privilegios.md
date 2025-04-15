# 🔼 Escalando Privilégios (Privilege Escalation)

Beleza, você invadiu a máquina. Agora o próximo passo é **escalar privilégios** pra se tornar root (ou administrador). É aqui que você mostra que entende do rolê.

---

## 🧠 O que é Escalada de Privilégio?

É o processo de sair de um usuário limitado (tipo `www-data`, `user`, `nobody`) e virar **root**, que é o dono da porra toda no sistema.

Você precisa disso pra:

- Acessar arquivos protegidos (como `/root/root.txt`)
- Instalar ou remover programas
- Controlar tudo no sistema

---

## 🛠️ O que procurar?

### 🔎 1. Comandos básicos de reconhecimento:

```
whoami
id
hostname
uname -a
sudo -l
```

 2. Coisas suspeitas:

    Permissões exageradas (ex: arquivos com SUID)
```
find / -perm -4000 -type f 2>/dev/null
```
O que é esse 2>/dev/null? você deve estar se perguntando...
👉 2>/dev/null serve pra ignorar mensagens de erro no terminal Linux.
2> = redireciona o stderr (que são os erros).
/dev/null = um "buraco negro", tudo que vai pra lá é descartado.

Comandos que você pode rodar como root sem senha:
```
sudo -l
```

Crontabs rodando scripts automaticamente:
```
cat /etc/crontab
```

Scripts com permissão de escrita:
```
find / -writable -type f -name "*.sh" 2>/dev/null
```


🚀 Ferramentas que ajudam MUITO
🧩 linpeas

Script que escaneia o sistema todo e mostra possíveis vetores de escalada.

    Baixa no seu Kali:

wget https://github.com/carlospolop/PEASS-ng/releases/latest/download/linpeas.sh
chmod +x linpeas.sh

Transfere pra máquina alvo (ex: via python -m http.server) e executa:

    ./linpeas.sh

Ele te mostra TUDO: permissões erradas, bins inseguros, variáveis do sistema, etc.



⚠️ Vetores comuns de escalada

    sudo mal configurado

    Scripts no crontab executados como root

    Binários com SUID (/usr/bin/find, vim, less)

    PATH mal definido (dá pra injetar comandos falsos)

    Serviços vulneráveis rodando localmente (ex: mysql com senha fraca)



🔥 Exemplo de escalada com sudo:

sudo /usr/bin/find . -exec /bin/sh \; -quit

Se sudo -l mostrar que você pode rodar o find como root, isso aí te dá uma shell root direto.


✅ Dica final

Sempre que invadir uma máquina:

    Enumere tudo.

    Veja o que pode rodar como root.

    Busque permissões e scripts suspeitos.

    Rode o linpeas.

    Escale e finalize a missão.


No último capítulo vou deixar uma lista de links, wordlists, cheatsheets e tudo que vai te ajudar a continuar evoluindo.
Parabéns por chegar até aqui. Você já tá muito mais preparado que a maioria.

