# Curso de Git

---

## Objetos Git

### Blobs - Trees - Commits

> echo 'conteudo' | git hash-object --stdin

fc31e91b26cf85a55e072476de7f263c89260eb1

> echo -e 'conteudo' | openssl sha1

(stdin)=  65b0d0dda479cc03cce59528e28961e498155f5c

> echo -e 'blob 9\0conteudo' | openssl sha1

(stdin)= fc31e91b26cf85a55e072476de7f263c89260eb1

---

Gerar Chave SSH

> ssh-keygen -t ed25519 -C judenilson@hotmail.com

Pegar a chave pública no diretório criado

> cat id_ed25519.pub

> eval $(ssh-agent -s)

Inserir a chave no PC

> ssh-add id_ed25519

---

- Iniciar o GIT

- Iniciar o versionamento

- Criar um commit
  
  - git init
  
  - git add \*.* (inserindo todos os arquivos no repo)
  
  - git commit -m "texto commit"
  
  - git push master

---

git configurações iniciais

> git config --global user.email "judenilson@hotmail.com"
> git config --global user.name "judenilson"

## Ciclo do GIT

Arquivos em Staged

![](C:\Users\Judenilson\AppData\Roaming\marktext\images\2022-11-14-16-12-58-image.png)

Arquivos Commitados

![](C:\Users\Judenilson\AppData\Roaming\marktext\images\2022-11-14-16-13-13-image.png)

---

No GitHUB é bom ter as mesmas configs entre máquinas.

Lista todas as configs

> git config --list

Volta para zero a config específica, para poder alterar

> git config --global --unset user.email 

Após criar o repositório no GitHub deve-se apontar o repo local para o remote

>  git remote add origin "link para o git"

Subir os arquivos

> git push origin master

Caso tenha conflitos deve-se puxar os arquivo do remoto.

> git pull origin master
