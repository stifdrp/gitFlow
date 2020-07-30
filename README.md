# GitFlow TIFDRP

## Criar um repositório

**GitHub**

- Criar o repositório

**Máquina Local**

- Clonar o repositório:
  - `git clone git@repoaddress/repo.git`
  - `cd repo/`
- Criar um branch chamado develop:
  - `git checkout -b develop`
- Mandar o branch develop para o remoto:
  - `git push origin develop`
- Trackear o branch develop local o com develop remoto:
  - `git branch --set-upstream-to=origin/develop`
  
<br>

## Nova Funcionalidade

**GitHub**

- Criar issue

**Máquina Local**

- Clonar o repositório, se não tiver:
  - `git clone git@repoaddress/repo.git`
  - `cd repo/`
- Entrar no branch master e atualizá-lo:
  - `git checkout master`
  - `git pull`
- Entrar no develop e atualizá-lo:
  - `git checkout develop`
  - `git pull`
- Criar um branch novo a partir do branch develop para resolver a issue:
  - `git checkout -b issue-issueid`
- Criar a nova funcionalidade.
- Commit das alterações:
  - `git add .`
  - `git commit -m "msg do commit resolve #issueid`
- Merge do branch da issue para develop:
  - `git checkout develop`
  - `git merge --no-ff issue-issueid`
- Mandar o branch develop pro remoto:
  - `git push origin develop`
- Conferir o servidor de homologação.

**GitHub**

- Entrar no branch develop.
- Fazer Pull Request para master.
- Se possível, pedir para alguém revisar o código.
- Se estiver tudo ok com o código fazer um merge da PR para master.
- Conferir o servidor de produção.

<br>

## Hotfix

**Máquina Local**

- Clonar o repositório, se não tiver:
  - `git clone git@repoaddress/repo.git`
  - `cd repo/`
- Entrar no branch master e atualizá-lo:
  - `git checkout master`
  - `git pull`
- Criar um branch novo a partir do master para reolver o hotfix:
  - `git checkout -b hotfix-keyword`
- Commit das alterações:
  - `git add .`
  - `git commit -m "msg do commit"`
- Merge do branch do hotfix para master:
  - `git checkout master`
  - `git merge --no-ff hotfix-keyword`
- Mandar o branch master pro remoto:
  - `git push origin master`
- Conferir o servidor de produção