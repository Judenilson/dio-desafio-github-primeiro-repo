# Git Class

---

## Git Objects

### Blobs - Trees - Commits

> echo 'conteudo' | git hash-object --stdin

fc31e91b26cf85a55e072476de7f263c89260eb1

> echo -e 'conteudo' | openssl sha1

(stdin)=  65b0d0dda479cc03cce59528e28961e498155f5c

> echo -e 'blob 9\0conteudo' | openssl sha1

(stdin)= fc31e91b26cf85a55e072476de7f263c89260eb1

---

Create SSH key

> ssh-keygen -t ed25519 -C judenilson@hotmail.com

To take a public key in created directory

> cat id_ed25519.pub

> eval $(ssh-agent -s)

To Insert the key in PC

> ssh-add id_ed25519

---

- Start GIT

- Start versioning 

- Create a commit 
  
  - git init
  
  - git add \*.* (Insert all archives in repo)
  
  - git commit -m "text commit"
  
  - git push master

---

git initial settings

> git config --global user.email "judenilson@hotmail.com"
> git config --global user.name "judenilson"

## GIT Cycle

Staged Archives

![staged](https://github.com/Judenilson/dio-github-first-repository-challenge/blob/main/img/staged.png "staged")

Commits Archives

![commit](https://github.com/Judenilson/dio-github-first-repository-challenge/blob/main/img/commits.png "commit")

---

In GitHUB is good to have the same settings between computers.

Lista all settings

> git config --list

Be back to blank the specific setting, to take change.

> git config --global --unset user.email 

After create repo in GitHub we must to point the local repository to remote.

>  git remote add origin "link para o git"

Upload archives

> git push origin master

If there are conflicts we must pull remote archives.

> 
