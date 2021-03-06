![Introdução a Git e ao GitHub](http://matheusti.com.br/my-github-images/bootcamp-dio-localizaLabs/git-github/git-github.png)

## Aulas 1, 2 e 3
São abordados comandos básicos para terminal, tópicos fundamentais de GIT e um pouco da história do GIT.

## Aula 4
Foram apresentados os seguintes comandos
 - `git init`
 Comando utilizado para inicializar um repositório **local** no diretório ativo.
 - `git add`
 Comando utilizado para adicionar uma alteração no diretório ativo.
    - `git add *`
    - `git add .`
 - `git commit` Comando utilizado para salvar as alterações feitas.
    - `git commit -m "mensagem"`

E também foi abordado o conceito de [Markdown](https://support.typora.io/Markdown-Reference/ "Markdown Reference for Typora").

## Aula 5
 - `git status` Comando utilizado para exibir o estado do repositório e da área de 'Staged'.

- `git init`
 Inicializa o GIT naquele repositório, e todos os arquivos recebem o status de **Untracked** (não rastreado).
 - `git add`
 Faz com que nosso arquivo saia da condição de **Untracked** (não rastreado) e passe a ser **Tracked** (rastreado) e recebe o status de Staged que é uma espécie de buffer entre o diretório ativo e o histórico do projeto.
<p align="center"><img src="http://matheusti.com.br/my-github-images/bootcamp-dio-localizaLabs/git-github/01-01.png" title="Fonte: Slide da Aula"/><br/><span>Fonte: Slide da Aula</span></p>


 - **Unmodified**
 Se um arquivo não foi alterado desde que passou a ser rastreado então ele recebe o status de Unmodified (não modificado).
<p align="center"><img src="http://matheusti.com.br/my-github-images/bootcamp-dio-localizaLabs/git-github/01-02.png" title="Fonte: Slide da Aula"/><br/><span>Fonte: Slide da Aula</span></p>

 - **Modified**
 Por outro lado se o arquivo foi modificado então ele recebe o status de Modified (Modificado) e vai para a área de Staged.
<p align="center"><img src="http://matheusti.com.br/my-github-images/bootcamp-dio-localizaLabs/git-github/01-03.png" title="Fonte: Slide da Aula"/><br/><span>Fonte: Slide da Aula</span></p>

 - **Untracked**
 Se estivermos com um arquivo Unmodified e removermos ele, então esse arquivo passa a ser Untracked.
<p align="center"><img src="http://matheusti.com.br/my-github-images/bootcamp-dio-localizaLabs/git-github/01-04.png" title="Fonte: Slide da Aula"/><br/><span>Fonte: Slide da Aula</span></p>

 - `git commit` Quando o arquivo está no estado de Staged ele está se preparando para fazer parte de um commit.  Após ser feito o Commit, os arquivos voltam ao estágio Unmodified.
<p align="center"><img src="http://matheusti.com.br/my-github-images/bootcamp-dio-localizaLabs/git-github/01-05.png" title="Fonte: Slide da Aula"/><br/><span>Fonte: Slide da Aula</span></p>

## Aula 6
 - `git remote` Comando utilizado para apontar o repositório local para o repositório remoto
   - `git remote add origin URL`
 - `git push` Comando utilizado para enviar as alterações do repositório local para o repositório remoto
   - `git push origin master`
 - `git pull` Comando utilizado para receber as alterações do repositório remoto para o repositório local

## Aula 7
É abordado com podem acontecer e como resolver os conflitos nos arquivos. É também abordado o conceito de 'clone' de repositórios remotos.
 - `git clone` Comando utilizado para obter um repositório remoto.
   - `git clone URL` 