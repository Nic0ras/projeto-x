## Eu sou um arquivo de documentação do projeto

Sou eu que apareço na pagina inicial do projeto no GitHub

~ Anotações pessoais de como mandar um arquivo para o GitHub passo a passo ~
Objetivo da aula: Entender o que é repositório local e remoto (versionamento)
Versionamento:
Voltar a um ponto do projeto em questão por n razões

Git: Repositório local.
Github: Repositório é um repositório remoto.

Git e Github são independetes entre si?
 (O git depende do Github para existir? - NÃO, pois é possível deixar o código na máquina.)

Github não faz sentido sem o Git, pois não há maneiras de mandar nossos repositórios pra lá.

Git é um controlador de versão local:
Ela tem;
Autor, data e hora e histórico do projeto recuperável.
Todo ponto de alteração importante que fazemos no nosso projeto se chama (commit)

Github
*É a plataforma que armazena códigos (mais seguro que salvar apenas no computador)
*É um portifólio online (vale mais para o programador do que o próprio linkedin);
*Vitrine de aplicações e desafios realizados em programação.
*Mostra a linha do tempo das atividades do dono do gitHub
*Código colaborativo(Mais de um participante do projeto - empresas utlilizam
*Open source (Código público para toda a comunidade)

Atividade em aula 1- Nosso projeto no github
*Inicie o versionamento no projeto X
*Crie um repositório online para o projeto com o mesmo título que utilizou em seu computador
*Crie um commit com todos os arquivos e envie o projeto para o repositório no Github recém-criado

cd é o caminho-da-pasta
cd . está na pasta atual.
cd ./ nome-da-pasta
cd .. volta uma pasta(pasta anterior)
ls lista o que há onde estamos
ls -a ( mostra além do ls, mostra também as pastas ocultas do sistema) 
ao iniciar o Bash, encontraremos na linha de código o "~", ele representa a sua localização atual no bash (onde você está trabalhando), e quando ele é a ultima posilção, significa que estamos na pasta do usuário

git config user.name (vemos o nome do usuario atual)
git config --global user.name "Nic0ras" (configura e fala para o git o nome do usuario atual)
(usando a ferramenta git) (config faz a configuração que queremos) user.name (ação a ser executada) "nome do usuario"
--glboal (faz a configuração para todos os arquivos que iremos trabalhar.)






APLICANDO NO VSCODE (OU  GITBASH)
Criando um repositório git (git init)
git init (podemos iniciar o git init tanto numa pasta vazia, quanto numa pasta que já existe um projeto)
O git só começa a "prestar atenção" no que estamos fazendo no projeto, quando iniciamos o git init.

criando um projeto node:
1- npm init -y (comando para criar o projeto node, -y da yes para todas as perguntas)
2- index.js - nosso primeiro projeto dentro da pasta
3- git init (cria um repositório no git (repositório na máquina) )
após este comando, os arquivos exibirão um "U" ao lado, e o mesmo significa "Untracked"... quer dizer que o git não está "prestando atenção" no que estamos fazendo.
master é o nome da branch em que estamos 
(branch é uma linha do tempo paralela para fazermos testes) (versões alternativas do código)
Branchs são importantes, pois criando versões alternativas do projeto em que estamos trabalhando, as possibilidades se tornam infinitas, assim como a quantidade de pessoas trabalhando no mesmo projeto.
4- git status - mostra o status do repositório
estará em vermelho todos os arquivos que o git pode enviar ao repositório. (em vermelho por que isso ainda não foi feito)
5- git add - manda os arquivos para o git "prestar atenção"  (tudo o que está vermelho em git status, passa a se tornar verde, isso é a representação visual de que o git esta prestando atenção no que estamos fazendo)
6- "Staging area"(area de preparação)
-git area pasta/arquivo
-git restore pasta/arquivo
U- untracketd (não está prestando atenção
A- Index Add (arquivo adicionado
-1, M (ou seja qual for a quantidade de erros, modified [modificado)
git restore index.js (nome do arquivo): restaura o arquivo para o ponto onde não haviam erros.
O intuito da area de estágio é
Git reverte - volta para o commit anterior
git restore - volta para o ponto onde damos o gitt add, descarta todas as alterações feitas até o git add.
git reset index.js (nome do arquivo) deixa de monitorar os arquivos adicionados na area de estagio
git add . adiciona todos os arquivos da pasta
readme.md é o arquivo de documentação do projeto( o que o arquivo faz, como utilizar o projeto)

*CRIEI UM PROJETO GIT NA PASTA ERRADA*
ls mostra os arquivos relevantes ao usuario
ls -a mostra o .git (que é uma referencia que é um projeto git)
rm -rf .git(apaga a pasta .git): apagar uma pasta pelo terminal








se no git status esta tudo verdinho, significa que estamos prontos para fazer nosso primeiro COMMIT.

git commit -m  "primeiro commit"(m é  a mensagem)
o commit contém o seu nome, a data e hora que fizemos o commit e a mensagem do que fizemos.
retornará:
$ git commit -m "primeiro commit"
[master (root-commit) 9b67f9d] primeiro commit
 3 files changed, 14 insertions(+) (3 arquivos modificados, que é a quantidade de arquivos que temos na pasta; 14 insersões, que é a quantidade de linhas de código no total, de todos os projetos;)
 create mode 100644 README.md
 create mode 100644 index.js
 create mode 100644 package.json
;
A partir deste ponto, nossa staging area esta vazia, então precisamos utilizar o comando git add novamente.

git log mostra os commits que fizemos até então. (o histórico)
README.md é o primeiro arquivo que aparece no repositório remoto; md é uma linguagem de texto (marcação de texto)
# é o titulo no git hub
## é um titulo não tao grande no titulo do git
### menor ainda

git commit -m "alteração do README.md" (o nome dos commits devem ser o mais relevante e  breve possível, tais como:
altera READ.md ... modifica qualuqer coisa... etc...

quando temos muitos commits, o git log fica muito extenso no terminal, e uma alternativa é o:
 git log --oneline : mostra o git log mais simplificado.

git log --help (mostra todos as funcionalidades do git log)

PADRÃO DE NOMENCLATURA DO GIT
sempre usar "-" nos espaços do nome titulo.

SUBINDO ARQUIVOS PARA O GITHUB
git remote não retornará nada, pois não há um git vinculado com o projeto
git remote add origin(nome do nosso repositório remoto principal) https://github.com/Nic0ras/projeto-x.git (url do nosso repositório online)
git branch mostra o nome da branch que há
git branch -M main renomeia a branch
git push origin main: manda para o gitHub
git push -u origin(que é o repositório) main (nome da branch)
sempre que for mandar um projeto novo, é necessário fazer todos esses passos.


