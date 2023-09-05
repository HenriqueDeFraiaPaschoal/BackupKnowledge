# Linux
[Linux](https://pt.wikipedia.org/wiki/Linux) é um termo usado para referir à sistemas operacionais baseados em Kernel Linux, desenvolvido por [Linus Torvalds](https://pt.wikipedia.org/wiki/Linus_Torvalds), que é um sistema operacional open-source (código aberto).
Este, como outros sistemas, é baseado em [Unix](https://pt.wikipedia.org/wiki/Unix), um sistema operativo. Tudo em Unix são ou processos ou arquivos, e o sistema operacional facilita a comunicação do usuário com esse sistema operativo.

Essa comunicação possui vários componentes/participantes: hardware (peças/equipamentos), [BIOS](https://pt.wikipedia.org/wiki/BIOS) (Sistema básico de entrada e saída), [kernel](https://pt.wikipedia.org/wiki/N%C3%BAcleo_(sistema_operacional)) (gerenciador de recursos, ponte entre aplicativos e o hardware), aplicações/sistemas operacionais e usuários. Com a ajuda deste documento, iremos trabalhar em partes dessa comunicação.

Resumo do [autor](https://br.linkedin.com/in/henrique-de-fraia-paschoal-113b4111a?original_referer=https%3A%2F%2Fwww.google.com%2F):

Hardware é iniciado -> Bios gerência essa inicialização -> kernel do sistema passa a gerenciar quase tudo -> O sistema operacional é iniciado comunicando o usuário com o kernel

## Distros

Sendo open-soucer, o Linux possui várias distros ([distribuições/versões](https://en.wikipedia.org/wiki/Linux_distribution)) criadas a partir de sua base, cada uma com diferentes focos. As mais conhecidas são:
- Ubuntu
- Fedora
- Manjaro
- Mint
- Debian

Os focos podem ser segurança, utilização ou até apenas visual.

Como preferência do [autor](https://br.linkedin.com/in/henrique-de-fraia-paschoal-113b4111a?original_referer=https%3A%2F%2Fwww.google.com%2F) deste documento, a distro utilizada é o Ubuntu, mas muitos dos comandos também podem ser utilizados em outros sistemas operacionais.

## Instalação do sistema operacional


## Terminal

Existem vários tipos de [Shell](https://pt.wikipedia.org/wiki/Shell_(computa%C3%A7%C3%A3o)) (Interface de Usuário) com linha de comando (CLI - Command Line Interface) ou interface gráfica (GUI - Graphical User Interface). Funcionam como um sistema de comunicação entre o sistema operacional, o usuário e o kernel.

Entre os CLI os principais são: SH, BASH, CSH, TCSH e ZSH.

O foco deste documento será no [BASH](https://pt.wikipedia.org/wiki/Bash).

Dentro do UNIX tudo pode ser ser separado em arquivos e processos. Fazer algo é um processo, todo processo possui seu PID(Process Identifier) com proprietário do processo, seção do shell, se está funcionando ou parado.
Tudo mais são arquivos, os arquivos são organizados em [hierarquia de raiz ou árvore](https://pt.wikipedia.org/wiki/%C3%81rvore_(estrutura_de_dados)).

Os comandos abaixo podem ser utilizados no terminal, sendo no Ubuntu o atalho para abri-lo Ctrl+Alt+T, ou abra aplicativos e pesquise por terminal.

### Terminologias
A palavra [diretório](https://pt.wikipedia.org/wiki/Diret%C3%B3rio_(computa%C3%A7%C3%A3o)) pode ser conhecida como pasta.

### Atalhos e opções do terminal:  
Utilizar TAB para completar nomes de arquivos.  
Utilizar Ctrl+C para terminar operações  


### Comandos de ajuda e básicos
Comandos em negrito e itálicos representam os [comandos para windows](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/windows-commands).  
Os comandos apresentados seguem, mas não obrigatóriamente, o padrão/ordem de:

- **Comando** < especificação > [anexo/opção | versão abreviada] {descrição ***windows equivalente***}

Ex:
> **ls** [--all | -a]: {List All Directories, lista todos os diretórios}
  - -a: lista todos os diretórios


#### Ajuda
Qualquer dúvida utilize os comandos de ajuda

- **man** < comando >: {Mostra o manual do comando}
  - *Q* : Sai do manual.
- **whatis** < comando >: {Mostra um resumo breve do que é o comando}
- **apropos** < palavra >: {Busca um comando que tenha a palavra}
- < comando > [ --help ]: {Mostra um documento de ajuda sobre o comando}

#### Básicos

- **clear** : {Limpa o terminal ***cls***}  
- **cd** < diretório >: {Change Directory - Muda de Diretório}  
  */* : é o root  
  *~* : é o home do usuário  
  *.* : é o atual  
  *..* : diretório pai/anterior
- **ls** < opcional > [ -a ]: {List Directory Contents - Lista arquivos no diretório atual ***dir***}  
  *: pode ser utilizado para mostrar os arquivos e subarquivos do diretório  
  *a* : Inclui arquivos ocultos
- **mkdir** < nome > [ -p ]: {Make Directory - Cria um diretório com o nome escolhido}
  -p < direc/direc/.../nome > : cria o caminho de diretórios
- **pwd**: {Print current Working Directory - Mostra o caminho do root até o diretório}
- **touch** < nome.extensão >: {Cria um ou mais arquivos vazios com a extensão especificada}  
  < nome{0..10}.extensão >:
  - Ex1. touch listaCompras.txt
  - Ex2.touch Funcionário{1..10}.txt
- **cp** -[ i ] 'arquivoACopiar' 'nomeDaCopia' ---> (Copy) {Cria uma cópia do arquivo com primeiro nome, nomeando a copia com o segundo nome}
- **cat** 'arquivo' ---> (Concatenate) {Concatena e regista o conteúdo do arquivo no terminal}
  - Apenas cat irá
- **mv** 'nome1' 'nome2' ---> (Move) {Move/Renomeia o arquivo de nome1 para o diretório/nome nome2}
- **rm** ***del*** 'nome' ---> (Remove) {Remove/deleta apenas arquivos arquivo}
- **rmdir** -[ r | f ] 'nome' ---> (Remove Directory) {Remove/deleta o diretório}
  - *r* : Recursivo, deleta os itens internos
  - *f* : Força a remoção
- **less** 'arquivo' ---> {Exibe o conteúdo do arquivo paginado, não fica registrado o conteúdo no terminal}
  - *Spacebar* : Passa a página
  - *Q* : Sai da visualização
  - */'Palavra'* : Pesquisa a palavra no arquivo
    - *N* : Passa de palavra em palavra
    - *Enter* : Finaliza a pesquisa
- **head** -[ 'número' ]'arquivo' ---> {Mostra os 10 primeiros se não especificado ou o 'número' valores/linhas do arquivo}
- **tail** -[ 'número' ] ---> {Mostra os 10 últimos se não especificado ou o 'número' valores/linhas do arquivo}
- **grep** -[ i | v | n | c ] 'Palavra/'frase entre aspas'' 'arquivo' ---> {Busca a palavra/frase no arquivo desejado}
  - *i* : Ignora se está maiusculo ou minusculo
  - *v* : Busca valores que não possuem a palavra/frase
  - *n* : Mostra a linha onde se encontra
  - *c* : Mostra o número de vezes que se encontra a palavra no arquivo
- **wc** 'arquivo' ---> (Word Count) {Mostra a quantidade de linhas, palavras e caracteres do arquivo}~
  - *w* : Mostra só a quantidade de palavras
  - *l* : Mostra só a quantidade de linhas
  - *c* : Mostra só a quantidade de bytes
  - *m* : Mostra só a quantidade de caracteres

### Intermediários e instalações

sudo dpkg -i package_file.deb.

Ou utilize os caracteres coringas

O caracter ? pode substituir por um caracter desconhecido.
>Poderia pesquisar por ?arina.txt caso não lembre se o nome é Carina ou Karina

O caracter asterisco * pode representar todos ou continuação
> wc * contaria todos arquivos<br>
> ls *.txt listaria todos os arquivos com extensão .txt

- **cat** > 'nome' ---> 
  - Escreva o que deseja ser o conteúdo e aperte ctrl+D
- **cat** >> 'nome' ---> Irá adicionar no arquivo o que foi escrito antes do ctrl+D
- **cat** 'arquivo1' 'arquivo2' > 'arquivo3' ---> Cria um arquivo de nome3 com o conteúdo dos arquivos nome1 e nome2

- **sort** < 'arquivo' ---> Mostra o conteúdo em ordem alfabética
- **sort** < 'arquivo1' > 'nome1' ---> cria um arquivo nome1 com o conteúdo do arquivo1 ordenado
- **who** ---> Mostra os usuários logados atualmente
- **find** 'diretório' -[ type | size | name | date ] ''nome'' ---> Procura no diretório arquivos com as especificações
  - type : f são arquivos e d diretórios
  > find /home/trabalhos -type f "*mplos"
- history ---> Mostra o histórico de comandos utilizados no terminal
- **echo** 'mensagem' ---> Utilizado para imprimir textos na tela em scripts, ou pode-se criar arquivos como cat
  > echo 
### Avançados

O caracter pipe | pode ser utilizado para adicionar um comando no output de outro
> who | wc -l mostraria quantos usuários estão online no computador

'comando' > 'arquivo' ---> Direciona a saida do comando e sobrescreve/cria o conteúdo
'comando' >> 'arquivo' ---> Adiciona a saida do comando para o final do arquivo
'comando' < 'arquivo' ---> Direciona o comando para um arquivo sem altera-lo
'comando1' | 'comando2' ---> Direciona a saida do comando1 como entrada para o comando2

## Exercícios

### Básicos

1. **Crie** um diretório chamado `exercicios`
2. **Navegue** até o diretório `exercicios`
3. **Crie** dois arquivos de texto com nome `teste.txt` e `arquivo1.txt`
4. **Crie** dois diretorios com nome `diretorio1` e `diretorio2`
5. **Copie** o arquivo `teste.txt` com o nome `teste_copy.txt`
6. **Renomeie** o arquivo `teste.txt` para `teste_antigo`.txt
7. **Mova** o arquivo `teste_copy.txt` para o `diretório1`
8. **Mova** o arquivo `teste_copy.txt` do diretorio1 para o `diretorio2`
9. **Apague** a pasta `diretorio1`
10. **Renomeie** a pasta diretorio2 para `diretorio1`
11. Veja o **caminho** completo até o `diretório atual`
12. **Liste** todos os arquivos do `diretorio atual`
13. **Apague** o `diretorio1`
14. **Apague** todos arquivos terminados com `.txt`
15. **Limpe** o `terminal`

Resposta:
1. mkdir exercicios
2. cd exercicios
3. touch teste.txt arquivo1.txt
4. mkdir diretorio1 diretorio2
5. cp teste.txt teste_copy.txt
6. mv teste.txt teste_antigo.txt
7. mv teste_copy.txt diretorio1
8. mv diretorio1/teste_copy.txt diretorio2
9. rmdir diretorio1
10. mv diretorio2 diretorio1
11. pwd
12. ls -a
13. rm -rf diretorio1
14. rm *.txt
15. clear

### Intermediário

Após finalizar os exercícios básicos, na mesma pasta, siga:

1. Crie um arquivo filmes.txt com 10 nomes de filme de sua preferência
2. Mostre os 5 primeiros filmes no terminal
3. Mostre os 4 ultimos filmes no terminal
4. Mostre o conteúdo de forma páginada
5. Busque pela palavra GitHub e por uma palavra de algum filme durante a visualização paginada
6. Crie um arquivo nomes.txt com 5 nomes conhecidos
7. Adicione 5 nomes ao arquivo nomes.txt
8. Busque em nomes.txt algum nome
9. Execute a mesma busca anterior mas ignorando maiusculo e minusculo
10. Busque por nomes que não sejam Henrique
11. Busque por nomes que possuem a letra a
12. Acesse o manual do comando wc
13. Conte o número de linhas, palavras e caracteres dos arquivos filmes.txt
14. Conte apenas o número de caracteres do arquivo nomes.txt
15. Crie os arquivos foto.jpg, relatorio.pdf
16. Liste os arquivos que terminem com .txt
17. Liste os arquivos que terminem com .txt e .jpg

Respostas:

1. cat > filmes.txt  
  Rei  
  Leão  
  Narnia  
  Lightyear  
  Red  
  Os Incríveis  
  UP  
  Wall-e  
  Mulan  
  Toy Story  
  Hilda
2. head -5 filmes.txt
3. tail -4 filmes.txt
4. less filmes.txt
5. less filmes.txt /GitHub /Rei
6. cat > nomes.txt  
  Henrique  
  João  
  Vitor  
  Alex  
  Kety
7. cat >> nomes.txt  
  Mayara  
  Livia  
  Miriam  
  Remo  
  Bianca
8. grep 'Henrique' nomes.txt
9. grep -i 'henrique' nomes.txt
10. grep -v 'henrique' nomes.txt
11. grep '*a*' nomes.txt
12. man wc
13. wc filmes.txt
14. wc -m nomes.txt
15. touch foto.jpg relatorio.pdf
16. ls *.txt
17. ls *.txt *.jpg

### Avançados

Após finalizar os exercícios intermediários, na mesma pasta, siga:

1. Crie um arquivo chamado primeiros_nomes.txt com os 5 primeiros nomes de nomes.txt em ordem alfabética
2. Conte os números de linhas que possuem as letras 'an' em nomes.txt
3. Conte o número de linhas que não possuem as letras 'an' em nomes.txt
4. Crie um novo arquivos chamado filmes_e_nomes.txt com os conteúdos de nomes.txt e filmes.txt
5. Ordene o arquivos filmes_e_nomes.txt

## Dicas

echo $0 -> mostra qual shell está sendo utilizado

## Exercicios


## Referências

Uso de [Curl](https://linux.die.net/man/1/curl) em certos comandos

[Repo Git Comandos](https://github.com/trinib/Linux-Bash-Commands/blob/main/README.md#-b)

[git1](https://gist.github.com/riipandi/3097780)

[git2](https://gist.github.com/heobay/8431305)
