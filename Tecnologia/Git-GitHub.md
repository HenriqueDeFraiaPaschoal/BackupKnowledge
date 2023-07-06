# Git
<details>
  <summary>

  ## O que são Git e GitHub?
  </summary>

### Git
Desenvolvido por Linus Torvalds para o desenvolvimento do kernel Linux, o [Git](https://pt.wikipedia.org/wiki/Git) é uma ferramenta de versionamento de arquivos open-source mais utilizada no mercado.  
Possui funcionalidades que facilitam verificar quando, o que e por quem e onde houve alterações em arquivos. Motivando implementação de testes/experimentos que podem ser reversíveis conforme as marcações feitas.  
Sua versão mais atual junto à sua documentação pode ser encontrada em: https://git-scm.com/

Principais características:
- Não necessita de conexão com internet
- Grátis e código aberto
- Sistema de controle de versionamento
- Guarda trajetória das mudanças, não cópias dos arquivos
- Utilizando o prompt de comando
  
### GitHub
O [GitHub](https://en.wikipedia.org/wiki/GitHub) é uma plataforma de hospedagem de código muito utilizada como ponte de conexão para arquivos que serão trabalhados em equipe com uso de git.
Possuí várias funcionalidades para facilitar a comunicação/trabalho em equipe junto à aprovações de modificações/versionamentos.
A plataforma permite que repositórios públicos possam colocar sites simples na internet com livre acesso [GitHub-Pages](https://docs.github.com/pt/pages/getting-started-with-github-pages/about-github-pages).
A plataforma está acessível em: https://github.com/

Principais características:
- Gratuito para os serviços mais usuais
- Acessível globalmente (necessita de internet)
- É um repositório(pasta) para guardar códigos/arquivos
- Pode ser utilizado pelo prompt de comando ou pelo site
</details>

## Repositórios
  Repositórios podem ser considerados como pastas ou diretórios de um computador onde foi iniciado um versionamento utilizando git.
  Um repositório git possui obrigatoriamente no diretório principal/pai o diretório oculto:  
  - **.git**: diretório com arquivos gerenciadores do versionamento do repositório.  
    - Deletar esse diretório "desversiona" a pasta no estado atual

  O arquivo **.gitignore** é utilizado para definir os arquivos que serão ignorados no versionamento e não serão submetidos nas plataformas de hospedagem.  
  Seu conteúdo segue a seguinte regra:  
  - Arquivo: 'nome arquivo'
  - Tipagem: *.'extensão' Ex: *.orig (arquivos de merge)
  - Diretório: diretório/  
  - Caso ignorado tipagem, pode-se escolher arquivo a NÃO ser ignorado com !arquivo.extensão
  Utilizando quebra de linha a cada arquivo.

  O versionamento do git e github funcionam focados em 4 áreas:
- **working directory**: diretório de trabalho, diretório padrão.
- **Staging area**: local onde as mudanças podem ser armazenadas para depois ser commitadas/versionadas.
- **repository/commited**: Mudanças já versionadas e salvas.
- **remote**: seria a ultima etapa no fluxo de trabalho onde as mudanças são submetidas para uma plataforma online. Onde no comando origin é um alias para a URL que será cadastrada.

## Comandos
Recomendável ler sobre comandos do [Linux](/Linux.md)
As aspas simples foram utilizadas para demonstrar textos que podem/devem ser alterados conforme situação

<details open>
<summary>

### Git
</summary>

renomear/recortar-corlar arquivos e copiar e renomear arquivos muito semelhantes, pode causar confusão no git onde, apesar do resultado final ser o mesmo, a ação que foi considerada para chegar naquele resultado pode estar equivocada
[Git comandos](https://git-scm.com/docs)

git help 'comando': mostra detalhes sobre o comando

#### Básicos
- **git config --global user.name "'Seu nome'"**: Configura o nome do usuário
- **git config --global user.email "'Seu email'"**: Configura o email do usuário
- **git init 'Nome diretório'**: Inicia o versionamento na pasta atual 
- **git status**: Mostra o status da branch atual
- **git add 'nome do arquivo'**: Manda as modificações do arquivo para a staging area
  - . : Adiciona tudo do diretório atual e abaixo
  - *-A* : Adicionar tudo e verificar arquivos que foram movidos, renomeados, criados ou deletados
  - *-u* : Verifica renomeação e movimentação de arquivos
- **git commit**: Abre o editor de texto para mandar o commit
- **git commit -m 'descrição'**: Manda tudo que estava na staging area etiquetado com a descrição (m de message)
- **git commit -am 'etiqueta'**: Manda as mudanças de arquivos monitorados para o staging e commita  
- **git ls-files**: Mostra os arquivos do git
- **git rm "file"**: remove o arquivo e já adiciona a mudança ao stage
- git --version

#### Logs
- **git log**: Mostra os commits da branch atual(Q+enter para sair)
- **git log --abbrev-commit**: Mesma coisa mas com o id simplificado
- **git log --all --oneline --graph --decorate**: Mostra todos commits, resumido e de maneira gráfica e decorada
- **git log 'idcommit'...'idcommit'**: Mostra o log entre dois commits
- **git log --since="3 days ago"**: Mostra os commit dos ultimos 3 dias
- **git log -- 'nomeArquivo'**: Mostra os commits que abrangeram aquele arquivo
- **git log --follow -- 'nomeArquivo'**: Mostra os commits que abrangem aquele arquivo, mesmo se tiver sido renomeado
- **git show 'idCommit'**: Mostra detalhes de um commit

#### Configurações
- **git version**: Mostra a versão do git instalada
- **git config --global user.name "'Seu nome'"**: Configura o nome do usuário
- **git config --global user.email "'Seu email'"**: Configura o email do usuário
- **git config --global --list**: Mostra as configurações globais
- **git config --global alias.'nomeComando' "'comando'"**
  - Ex. git config --global alias.'hist' "log --all --oneline --graph --decorate"
- **git reflog**: mostra tudo que foi feito nos ultimos 90dias

#### Comparação
- **git diff**: compara o working directory com o staged
- **git diff HEAD**: compara o working directory com o ultimo commit da branch atual
- **git diff --staged HEAD**
- **git diff -- 'nomeArquivo'**: compara apenas um arquivo
- **git diff 'idcommit/tag' 'idcommit/tag'**: compara dois commits
- **git diff HEAD HEAD^**: compara o ultimo commit com o anterior a ele
- **git diff master origin/master**:

#### Stage
- **git reset**: Tira as alterações do stage

migração de master para main
- **git branch -m main** --->
- **git init -b main 'Diretório'** --->
- **git config --global init.defaultBranch main** --->
- git branch ---> mostra as branchs locais
- git branch -a ---> mostra local e as cópias locais das remote branches
- git branch -r ---> mostra as cópias locais das remote branches
- git branch 'nome-branch' ---> cria uma branch
- git ls-remote ---> busca a lista de branchs remotas
- git fetch origin ---> atualiza as cópias locais das branchs remotas com as branchs remotas
- git branch -vv ---> mostra todas as branchs locais com mais informações
- git branch --delete --remote 'nome branch' --> deleta uma trackingbranch
- git push --delete 'branch' --> para deletar uma branch do github e local
- git branch --track branchname origin/branchname ---> cria uma branch com uma trackingbranch
- git checkout 'nomeBranch' ---> muda para a branch
- git checkout . ou git restore .---> reverte todas alterações até o ultimo commit
- git switch 'nomeBranch' ---> muda para a branch
- git checkout 'idCommit' ---> muda para o commit na branch atual
- git branch -m 'nomeBranch' 'novoNomeBranch' ---> renomea a branch
- git branch -d 'nomeBranch' ---> deleta branch sem ser a atual do usuário (se for D maiusculo ele força a deleção)
- git checkout -b 'nomeBranch' ---> muda e já cria nova branch
- git switch -c 'nome-branch' ---> muda e já cria nova branch
- git clean -dn ---> mostra os arquivos não rastreados que serão deletados 
- git clean -df ---> deleta os arquivos não rastreados que serão deletados
- git reset --hard HEAD~n --> volta n commits atrás, 1,2,...(pode ser adicionado --soft para deletar o commit sem deletar arquivos adicionados após o commit)

MERGES
O merge pode ser fast-forward(caso n houver alteração na main após a criação da branch) e non-fast-forward-recursive|octopus|ours|subtree
- git merge 'nomeBranch' ---> faz merge da branch atual trazendo as modificações da especificada(trazendo todos commits)
- git merge --no-ff 'nomeBranch' ---> faz merge da branch atual trazendo as modificações da especificada(trazendo todos commits) sem usar fast forward, criando um commit de merge
- git merge --squash ---> mesma coisa do merge mas junta tudo deixando no stage aguardando um commit que será o unico commit do merge
- git merge 'nomeBranch' --no-ff ---> mesma coisa mas adiciona um commit, mantendo o histórico de existencia da branch (usar esse)
- git merge 'nomeBranch' -m 'commit/texto' ---> faz um merge etiquetando ele com o texto
- **git commit --amend -m "descrição"**: Permite alterar o título do commit  
- **git ls-files**: Mostra os arquivos que estão sendo monitorados no repositório
- **git reset HEAD^1 'nomeArquivo'**: Volta o arquivo ao estado de um commit atrás do último, se o arquivo for omitido, voltará tudo ao estado de um commit anterior ao último
- **git reset 'commitId'** ou **git checkout 'commitId'**: Volta à um commit específico
- **git checkout -- 'nomeArquivo'**: Cancela as modificações em um arquivo, voltando ele para o ultimo commit
- **git restore -- 'nomeArquivo'**: Cancela as modificações em um arquivo, voltando ele para o ultimo commit
- git merge --abort --> em situação de conflito pode cancelar o merge
- git cherry-pick 'commitId' --> traz um commit especifico para a branch atual, fazendo um "merge" apenas daquele commit

CONFLITOS
Caso durante um merge haja alterações no mesmo documento e o git não saiba o que fazer, o usuário entra em estado de merging, não é cleanworking directory nem staged area,
Ele altera o documento separando as partes em   
`<<<<<<` BRANCH1  
ipsum  
`======`  
hipsun  
`>>>>>>` BRANCH2

Pode usar uma ferramenta para ajudar no merge ou alterar o arquivo e fazer um commit para finalizar o merge

REBASE
REBASE NÃO TRAZ OS COMMITS, CRIA OS MESMOS COMMITS COM OUTROS #, não é recomendado rebase na master com repositórios que tenham remotos. Rebase é recomendado em branchs de features que necessitam de uma nova função da master, sendo feito o rebase na feature
- git rebase 'branch' ---> atualiza a branch atual com a branch especificada
- git rebase --abort ---> cancela o rebase em caso de conflito
- git rebase --continue ---> continua o rebase enquanto o usuário vai resolvendo os conflitos
- git pull --rebase 'origin master' ---> 

- git fetch ---> traz as mudanças do remote para o local de maneira não destrutiva

STASH
Armazenamento temporário de alterações unstaged e uncommited
- git stash save---> guarda as alterações sem ter que dar add e commit, facilitando uma mudança para trabalho urgente sem necessidade de gerenciar branchs
- git stash apply ---> aplica as mudanças guardadas
- git stash list ---> lista as mudanças que foram guardadas
- git stash drop 'index' ---> limpa as mudanças guardadas do ultimo stash
- git stash -u ---> guarda tudo incluindo arquivos não versionados pelo git(untrackedfiles)
- git stash pop 'index' ---> apply junto com drop
- git stash save 'commit/texto' ---> guarda tudo mas com etiqueta
- git stash push -m 'commit/texto' ---> guarda tudo mas com etiqueta
- git stash show 'stashId' ---> mostra os arquivos mudados daquele stash
- git stash apply 'stashId' ---> aplica as mudanças de um stash especifico
- git stash drop 'stashId' ---> deleta o stash especificado
- git stash clear ---> limpa todos os stash
- git stash branch 'nomeBranch' ---> cria uma nova branch com as stashs aplicadas

TAGS
Podem ser utilizadas para demarcar pontos específicos ou releases/lançamentos do arquivo para facilitar o gerenciamento
lightweighttag são como a HEAD das branchs, anotatedtags 
- git tag ---> mostra as tags existentes
- git tag 'nomeTag' ---> cria uma etiqueta simples no commit atual
- git tag --list ---> mostra uma lista das tags existentes
- git show 'tag' ---> mostra dados sobre a tag
- git tag -d 'tag' ---> deleta a tag especificada
- git tag -a 'texto' ---> cria uma tag com o texto e será aberto o gerenciador de commits padrão para adicionar um texto de anotações da tag (usar mais esse)
- git tag 'nomeTag' -m 'mensagemTag' ---> 
- git tag -a 'nomeTag' 'commitId' ---> adiciona uma tag em um commit específico
- git tag -a 'nomeTag' -f 'commitId' ---> coloca a etiqueta existente em um novo commit
- git push origin 'tag' ---> atualiza o github apenas com a tag (se o commit da tag n estive la, ele será subido tbm)
- git push origin master --tags ---> atualiza todas as tags
- git push origin :'nomeTag' ---> deleta a tag remota
</details>

<details>
<summary>

### GitHub
</summary>

- **git clone 'Url do repositório'** --->
- **git pull** ---> busca as alterações na branch principal remota(é uma mistura de git fetch e git merge juntos. Ele atualiza cópia da branch remota q temos no nosso computador e mergea com a branch atual)
- **git push origin(a abreviação dada ao repositório remoto escolhido) master(local or remote? branch)** ---> caso não seja especificado ele assume o que foi feito a primeira vez
- **git remote add 'origin' 'URL'** ---> Adiciona uma URL junto a uma abreviação para ela (geralmente usada como origin) para quando for utilizar ela. utilizar a URL no lugar de origin em outros comandos também funciona mas é ineficiente
- git fetch ---> busca todas as alterações remotas incluindo outras branchs
- git fetch origin 'branch' ---> busca uma branch específica
origin é o nome do repositório remoto, pode ser qualquer nome
</details>

## Utilitários GitHub


### Forks

### issues

## Commits
`:emoji:<Tipo>[Resumo] Descrição`
Tipos:
- FIX: Resolvendo bug ou consertando algo. 
- REVERT
- CHORE:
- 

## Fluxo de trabalho

## Referências
[GitHubOfficial](https://github.com/)
[GitOfficial](https://git-scm.com/)  
[Git Iuri](https://github.com/iuricode/padroes-de-commits)  
[Conventional Commits](https://www.conventionalcommits.org/pt-br/v1.0.0/)  
[Udemy Course](https://www.udemy.com/course/git-complete/)
[Git comandos](https://git-scm.com/docs)


