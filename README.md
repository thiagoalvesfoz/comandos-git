<h1 align="center">
  <img src="https://i.ibb.co/z2tXZRF/github.png" alt="Comandos úteis para git" width="120">
  <br>
  Comandos úteis para se dar bem no git
</h1>
<p align="center">:fire: um guia prático do dia a dia para ajudar você a contribuir em projetos open source</p>

<br>

| PROBLEMA | COMANDO |
| ------ | ------ |
| Quero alterar o comentário do meu último commit. <br><br>**Atenção**: Não amende commits que já sofreram push.| `git commit --amend -m "alterei o comentário"` |
| Quero listar as conexões remotas que meu repositório local tem incluindo a URL. | `git remote -v` |
| Quero que meu repositório local tenha mais de uma conexão remota. <br><br>**DICA:** Sério, você não é obrigado a fazer isso, mas caso queira mesmo adicionar uma nova "origin", utilize o nome **upstream**.  | `git remote add <nome> <link-repositorio-remoto>`  |
| Quero criar um ramo (branch) e ir direto para ele. | `git checkout -b <nome-da-branch>` |
| Quero remover uma branch que não utilizo mais. | `git branch -d <nome-da-branch>` |
| Quero sair da minha branch atual e voltar para a branch master. <br><br>**OBS:** O GitHub atualizou o nome padrão da branch principal, a branch **master** passou a <br>se chamar **main**. Caso o seu repositório esteja com esse novo nome na branch principal, <br>altere o nome da branch no comando ao lado antes de executar no terminal. | `git checkout master` |
| Quero baixar os últimos commits do repositório remoto, mas não quero aplicar as mudanças no meu repositório local ainda. | `git fetch <nome-do-seu-remote>` |
| Quero atualizar minha branch atual reescrevendo o histórico com as atualizações mais recentes da branch master de uma conexão remota específica.  <br><br>**DICA** certifíque-se que você está na branch que gostaria de estar. | `git rebase <nome-do-seu-remote>/<nome-da-branch>` |
| Quero atualizar minha branch atual sem reescrever o histórico.  <br><br>**DICA** certifíque-se que você está na branch que gostaria de estar. | `git merge <nome-do-seu-remote>/<nome-da-branch>` |
| Quero baixar os útimos commits e automaticamente reescrever meu repositório local na branch master. | `git pull --rebase <nome-do-seu-remote> <nome-da-branch>` |
| Quero ver todos os commits do projeto organizado visualmente. | `git –-oneline –-graph --all` |
| Quero fazer download de um pull request para a minha máquina | `git fetch origin pull/ID_PULL-REQUEST/head:NOME-DA-BRANCH` |

<br>
<h2 align="center">
  O KIT DE PRIMEIROS SOCORROS
</h2>

| PROBLEMA | COMANDO |
| ------ | ------ |
| Quero desfazer todas as minhas alterações não comitadas e retornar ao ponto do último commit. | `git clean -df`  <br>    `git checkout -- .` |
| Preciso remover o último commit, porém mantendo os arquivos do jeito que estão. | `git reset --soft HEAD~1` |
| Preciso remover o último commit, inclusive as alterações nos arquivos. <br><br> **ATENÇÃO:** Este comando não apenas descarta as alterações como também reverte todas as alterações no diretório para o estado do <br> commit em que foi especificado no comando.  | `git reset --hard HEAD~1` |
| Preciso apagar o último commit no **GitHub**. | `git push -f origin HEAD^:<nome-da-branch>` |
| Quero mudar o meu repositório remoto “origin”. | `git remote set-url origin <URL-DO-NOVO-REPOSITORIO>` |
| Quero alterar o editor padrão do git. | `git config –-global core.editor “diretório\sua-ide.extensao”` |
| Entrei no VIM por engano. Como sair? | Tecle `ESC`, depois digite `:q!` e tecle `ENTER` |


### Algumas dicas de contribuição ao open source:

- Nunca trabalhe na branch master, crie a sua própria branch.
- Não altere o que não diz respeito ao seu trabalho.
- Não toque em arquivos que não tem nada a ver com o que você está fazendo.
- Respeite os padrões de nomes, formatação, etc.

