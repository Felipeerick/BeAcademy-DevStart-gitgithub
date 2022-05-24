# Beacademy-devstart-gitegithub



Obs: coloquei uns códigos a mais para estudos;
*******************************************************************
## Criando um projeto com o git:

git init

inicia o repositório .git

git add .

vc pega todos os arquivos e salva de uma vez só


git commit -m "mensagem explicativa"

git branch -M master

troca o nome da branch

git remote add origin git@github.com: seuusuario/seurepositorio.git

adiciona a nova origin do repostitório


git push -u origin main
*******************************************************************

## Comandos

ls -al .git 

Vai listar todos os arquivos git do diretório

git log

traz as informações do autor, a ultima data alterada e o hash

git log -n 5

traz os 5 ultimos commits

git log --since=2020-10-01

todos os commits de 2020

git log --until=2020-10-01

traz os anteriores a essa data

git log --author=lipe

traz todos as alterações e commits de lipe

git log --grep="init"

ele procura por init, é uma ferramenta de pesquisa

git status

dar pra saber o que ta acontecendo no momento da operação

git rm --cached nomedoarquivo.txt

remove o arquivo

git add *.md 

vai adicionar todos os .md

git diff

mostra oq foi apagado ou adicionado

git diff staged

mostra oq foi apagado ou adicionado

depois de apagar um arquivo use o git commit -m "remove nomedoarquivo.txt"

git mv file1.txt sub/file1.txt

vai mover o arquivo para a pasta sub

git commit --amend 

ele abre o ultimo arquivo

git commit --amend -m "delete arquivo 1"

caso vc escreva sem querer de forma errada o commit essa funcionalidade
permite que vc atualize o nome do ultimo commit que vc fez

git checkout códigoHash--Nomedoarquivo

esse código serve para vc encontrar algum commit que vc queira

git clean -n

/*vai mostrar todos os arquivos q vão ser removidos para sempre*/

git clean -f

vai confirmar a remoção

git log --oneline

deixa tudo resumido em uma linha

git revert ~4

ele conta do head pra baixo na linha do tempo desa forma: HEAD -1, HEAD - 2 e assim por diante;

git revert --continue

git commit -am "modify tal arquivo"

/*quando vc modifica algum arquivo, mas ele já está sendo rastreado não 
precisa usar o git add, basta usar o git commit -am " "
*/

git revert --skip

git revert --abort

git show códigohash

/*mostra as diferenças de uma atualização para outra*/

git show códigohash -- doc/scr/*

/*vc consegue mostrar tudo oq aconteceu nesse diretório*/

git show hash -- doc/scr/css.css

/*busquei tudo oq aconteceu com esse arquivo em específico*/

cat nomedoarquivo.txt

/*serve para buscar algum arquivo e vê oq tem dentro*/
*******************************************************************
## Criando um .gitignore

caso quiser ignorar algum arquivo (tem que colocar dentro do diretório):
crie um gitignore = vim .gitignore

dentro dele coloque o nome do arquivo que vc deseja:
Exemplo: ts.txt

adicione ele: git add .gitignore
git commit -m "add gitignore"


git rm -r--cached .

/*apagando tudo o que estava sendo rastreado*/

git add .
/*coloque todos de volta*/

git comming -m "using .gitignore files"

o arquivo que estiver dentro de .gitignore vai ser ignorado.
*******************************************************************
## Criando uma branch

git checkout -b "nome do branch novo"

/*branch é tipo uma segunda ramificação onde se pode usar pra testar coisas
novas sem alterar o projeto principal*/

git checkout main

/*troca a branch*/

git merge nomedobranch

/*merge é o processo de fundir a ramificação de teste com a principal*/

git branch -d nome_da_branch

/*apaga a branch*/

git branch

/*mostra todas as branchs*/

git pull origin nome_da_branch

/*vai enviar a nova branch para a origem*/

git pull

/*Puxa os arquivos do repositorio remoto e mergeando com o local*/
*******************************************************************
## Clonando de um repositório remoto
git clone url_do_projeto

/*pega o projeto que ta no github e coloca na sua máquina*/
***********************************************************************
## Colocando arquivos no git stash

git stash

/* quando você está trabalhando em uma parte do seu projeto, as coisas estão em um estado confuso e você quer mudar de 
branch por um tempo para trabalhar em outra coisa. O problema é, você não quer fazer o commit de um trabalho incompleto
somente para voltar a ele mais tarde. A resposta para esse problema é o comando git stash.*/

git stash list
/*lista os stash*/

git stash pop
/*volta ao stash mais recente*/

git stash apply
/*aplica o stash mais recente*/

git stash apply@{2}
/*ele vai selecionar o especificado, se não for especificado ele pega o mais recente*/

git stash drop
/*faz a limpeza do git stash*/
