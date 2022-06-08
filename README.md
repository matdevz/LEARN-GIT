<h1 style=text-align:center>Aprender Git</h1>

## Comandos

### Os principais comandos

```bash

git-add
# Adiciona o conteúdo dos arquivos ao índice.

git-am
# Aplica uma série de patches vindos de uma caixa de e-mails.

git-archive
# Cria um histórico dos arquivos a partir de uma determinada árvore.

git-bisect
# Utilize a procura binária para localizar o commit que introduziu um bug.

git-branch
# Lista, cria ou exclui os ramos.

git-bundle
# Mova os objetos e as refs através do histórico.

git-checkout
# Mova os ramos ou restaura os arquivos da árvores de trabalho.

git-cherry-pick
# Aplica as mudanças introduzidas por alguns commits já existentes.

git-citool
# Uma alternativa gráfica ao git-commit.

git-clean
# Remove os arquivos da árvore de trabalho sem monitoramento.

git-clone
# Clona um repositório em um novo diretório.

git-commit
# Grava as alterações para o repositório.

git-describe
# Dá a um objeto um nome em um formato legível para humanos com base em um "ref" disponível.

git-diff
# Exiba as alterações entre os commits, o commit, árvore de trabalho, etc.

git-fetch
# Faz o download dos objetos e dos refs vindo de outro repositório.

git-format-patch
# Prepara os patches para serem enviados por e-mail.

git-gc
# Exclui os arquivos desnecessários e otimiza o repositório local.

git-grep
# Imprima as linhas que coincidam com um padrão.

git-gui
# Uma interface gráfica portátil para o Git.

git-init
# Cria um repositório vazio para o Git ou reinicializa um repositório já existente.

git-log
# Exibe os registros logs de um commit.

git-merge
# Une dois ou mais históricos de desenvolvimento juntos.

git-mv
# Move ou renomeia um arquivo, um diretório ou um link simbólico.

git-notes
# Adiciona ou inspeciona as anotações dos objetos.

git-pull
# Capture de e o integre com um outro repositório ou em um outro ramo local.

git-push
# Atualiza os refs remotos através da associação dos objetos.

git-range-diff
# Compara os dois intervalos de um commit (duas versões de um ramo por exemplo).

git-rebase
# Reaplica os commits no topo do outro cume da base.

git-reset
# Redefine o HEAD atual para o para a condição determinada.

git-restore
# Restaura as árvores de trabalho.

git-revert
# Reverte alguns commits já existentes.

git-rm
# Remove os arquivos da árvore de trabalho e do índice.

git-shortlog
# Faça um resumo da saída do git log.

# git-show
Exiba os vários tipos de objetos.

git-sparse-checkout
# Alter e inicialize a averiguação esparsa.

git-stash
# Armazene as alterações em um diretório fora do diretório de trabalho.

git-status
# Exiba a condição atual da árvore de trabalho.

git-submodule
# Inicializa, atualiza ou inspeciona submódulos.

git-switch
# Alterna entre os ramos.

git-tag
# Cria, lista, exclui ou verifica uma tag do objeto com assinatura GPG.

git-worktree
# Manipula as diversas árvores de trabalho.

gitk
# O navegador do repositório Git.

```

## Git init

Um repositório é o maior bem de qualquer projeto controlado por versão. Para transformar qualquer diretório em um repositório GIT, o simples comando git init <directory> pode ser utilizado. Uma pasta chamada .git também deve começar a existir no diretório em que o comando foi executado.

## Fluxo de trabalho

Agora que o repositório está pronto, vamos falar sobre a estrutura que é mantida pelo GIT.

Cada repositório local consiste em três árvores: o diretório de trabalho que contém os arquivos reais; O índice que desempenha o papel de uma área de teste e o HEAD que é um ponteiro para o último commit feito pelo usuário.

Então, é assim que o fluxo de trabalho pode ser explicado: o usuário adiciona um arquivo ou alterações do diretório de trabalho para o índice (a área de teste) e uma vez revistos, o arquivo ou as alterações são finalmente comprometidos com o HEAD.

## Git add e commit

Alterações ou adições de arquivos propostas são adicionadas ao índice usando o comando add. Para adicionar qualquer arquivo, o comando é:

    git add <nome_do_arquivo>

Se você está realmente confiante o suficiente para fazer essas mudanças no HEAD, então você pode usar o comando commit:

    git commit –m “Adicionar qualquer mensagem sobre o commit aqui”

## Dando continuidade com as mudanças

Depois de confirmar as alterações (e acreditar que elas estão prontas para serem enviadas para o repositório original), você pode usar o comando `push`.

Uma vez que o `git push origin master` é executado de dentro do diretório de trabalho, as mudanças presentes no HEAD são enviadas para o repositório remoto. No comando acima mencionado, o master pode ser alterado para o nome do branch ao qual você deseja que as alterações sejam comprometidas.

Se, no entanto, um repositório existente ainda não tiver sido clonado e você pretende estabelecer uma ligação entre o seu repositório e um servidor remoto, execute o seguinte comando:
