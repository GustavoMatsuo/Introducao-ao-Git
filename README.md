## Manual Git

* Configuração:
   * **git config --global user.name "< Seu Nome >"**
   * **git config --global user.email < Seu Email >** (Sempre com email do GITHUB)

* Para iniciar o versionamento:
    * **criar o arquivo .gitignore** (com as opções)
    * **git init** na pasta do projeto

* Para associar Git ao Github:
    * Criar um projeto 
    * Colocar no Git Bash **git remote add origin <URI do repositório remoto>** 
    * Para mudar o repositório remoto **git remote set-url origin <URI do repositório remoto>**
    * **git push -u origin master** (Para enviar o repositório local para o Github)
    * **git push** (Para enviar o novo commit)

* Para abrir pastas e voltar ( CMD ):
    * **cd "nome da pasta"** (Para abrir uma pasta seguinte)
    * **cd ..** (Para voltar uma pasta)

* Salvando versões:
    * **git status** (para ver status)
    * **git add .** (para preparar todos os arquivos e "*.txt" para adicionar todos arquivos txt por exemplo)
    * Caso tenha dado um add em um arquivo de teste **git reset HEAD "nome do arquivo"** para tirar do staged
    * **git commit -m "O titulo da versão"** (para salvar uma versão, é possível também dar **git commit -a -m "O titulo da versão"** para dar add e commit em uma linha)
    * **git commit --amend -m "O titulo da versão"** (para adicionar ao ultimo commit)
    * **git log** (para ver as modificações)
    * **git log --oneline** (para ver em apenas uma linha)
    * **git log -p** (para ver todos os detalhes e mudanças feitas, git log -p -1 para ver apenas o ultimo)
    * **gitk** (o mesmo que -p porem em uma interface)
    * **OBS: caso esqueça de colocar o nome da versão** 
      * tecla ESC
      * :q!
      * Tecle ENTER
      
* Caso tenha enviado um commit errado para o repositório remoto:
  * Precisa dar reset no repositório local primeiro 
  * Logo em seguida forçar o push com **git push origin +< nome do branch >** (geralmente MASTER), dessa forma força a atualização do repositorio
  

* Para ver o que foi alterado antes de dar commit:
    * **git diff** (para usar esse método não pode ser feito o add)
    * Caso ja tenha feito o add usar **git diff --staged**
    * Voltando a versão anterio:
    * **git checkout -- "nome do arquivo sem aspas"** (para voltar a versão do ultimo commit de um arquivo)
    * **git clean -df " e depois " git checkout -- . "**

* Desfazendo ultimo commit:
    * **git reset --soft HEAD~1** (Remover o último commit mantendo asalterações nos arquivos)
    * **git reset --hard HEAD~1** (Remover o último commit INCLUSIVE asalterações nos arquivos PERIGO!)

* Para olhar uma versão anterior:
    * **git checkout "código do commit"** (Para trocar de branch)
    *  E depois **git checkout "nome do branch ou código"** "no caso branch = master" (Para trocar novamente dessa forma não altera as versões)

* Para copiar um repositório do GITHUB:
    * Abrir o Git Bash na pasta e colocar **git clone <URI do repositório remoto>**
    * **ATENÇÃO: simplesmente copiar os arquivos NÃO traz o histórico de commits!**

* Atualizar o repositório local:
    * **git pull origin master **
    * **IMPORTANTE: o Git só deixa você continuar um trabalho e depois subi-lo para o repositório remoto, se você mantiver a sequência coerente de commits.**

* Adição de tag:
    * **git tag -a V1.0 -m "Titulo da Tag** (para adicionar uma tag)
    * **git tag** (para ver as tag em lista)
    * **git tag -d < nome da tag >**

* Para criar branch: 
    * **git branch < nome do branch >**
    * **git branch** (Para ver os branch )
    * **git checkout < nome do branch >** (para trocar de branch)
    * **git merge < nome do branch que quer juntar >** (**Atenção:** sempre o branch que estar irá modificar)
    * **git branch -d < nome do branch >** (para apagar o branch)

* Trabalhando com servidor local:**OBS: não pude conferir ainda como funciona essa parte**
    * **git init --bare** (para que todos possam ter acesso, faze isto no servidor)
    * **git clone file:////< nome do servodor > / < local do projeto >** (fazer isso na pasta onde irá clonar)
    * **git remote** (para ver o nome do servidor remoto)
    * **git push < nome do servidor > master** (gerealmente nome do servidor é "origin")
    * **git pull < nome do servidor > master** (para atualizar as alterações em tempo real para outra pessoa, comando tem que ser feito na pasta do projeto que irá atualizar)
    * **git fetch < nome do servidor > < nome do branch >** 

