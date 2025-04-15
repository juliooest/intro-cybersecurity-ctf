# 🐧 Linux Básico pra Cybersegurança e CTFs

Dominar alguns comandos básicos de Linux vai economizar um tempo absurdo nos CTFs. Aqui vão os comandos mais usados pra você já começar mandando bem.

---

## 📌 Comandos essenciais

### Navegação no terminal:

- **Listar arquivos e pastas:**
  ```
  ls           # simples
  ls -la       # com detalhes e arquivos ocultos
  ```

- Entrar numa pasta:
```
cd pasta/
```

- Ver pasta atual:
```
pwd
```

### Trabalhando com arquivos:

- Criar arquivo vazio:
```
touch arquivo.txt
```

- Ver conteúdo de arquivo:
```
cat arquivo.txt
less arquivo.txt  # mais detalhado, navegação com setas
```

### Copiar, mover ou apagar arquivos:
```
cp arquivo.txt copia.txt
mv arquivo.txt nova-pasta/
rm arquivo.txt
```

### Pesquisar arquivos ou texto:

- Localizar arquivos pelo nome:
```
find / -name arquivo.txt 2>/dev/null
```

- **Pesquisar texto dentro de arquivos:
```
grep 'palavra-chave' arquivo.txt
grep -r 'palavra-chave' pasta/
```

### Permissões de arquivos (muito útil!):

- Ver permissões:
```
ls -l arquivo.txt
```

- Mudar permissões:
```
chmod +x arquivo.sh   # tornar executável
chmod 644 arquivo.txt # permissões específicas (leitura/escrita)
```

### Usuários e privilégios:

- Ver usuário atual:
```
whoami
```

- Mudar de usuário (útil em CTF!)
```
su usuario
sudo -l  # ver o que você pode executar como sudo
```

### Monitorar processos e rede:

- Listar processos:
```
ps aux
top
```

- Checar conexões de rede:
```
netstat -tunlp
ss -tulnp
```

🎯 Dicas rápidas pro terminal:

    Use TAB pra autocompletar nomes.

    Use seta pra cima (↑) pra repetir comandos anteriores.

    Ctrl+C cancela um comando rodando.

Domina esses comandos básicos aí, que você já vai estar voando na hora dos desafios.

No próximo capítulo, vamos ver as ferramentas específicas de Cybersegurança. Bora?


