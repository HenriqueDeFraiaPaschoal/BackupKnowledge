# Python
Python é uma linguagem de programação de:

- Alto nível de abstração
- Tipagem forte e dinâmica
- Interpretada
- Blocagem por indentação
- Multiparadigma
- Case-sensitive

Vantagens:
- Tratamento de dados (várias bibliotecas)

extensão .py

## Terminal
extensão VSCODE Python para executar programas python
no terminal digitar python3 nomeArquivo ---> executa o arquivo .py
no terminal digitar python3 ---> faz uma execução rápida de python, podendo fazer alguns testes rápidos sem necessidade de criar arquivos
linux--> Python3 --version
windows--> python --version

## Sintaxe
|Matemáticos|      |               |         |                 |               |             |
| :--: | :-------: | :-----------: | :-----: | :-------------: | :-----------: | :---------: |
| soma | subtração | multiplicação | divisão | divisão inteira | resto divisão | potenciação |
|   +  |     -     |       *       |   /     |      //         |     %         |    **       |


|Atribuição|       |           |         |         |
| :-----: | :----: | :-------: | :-----: | :-----: |
| simples | somada | subtraída | produto | divisão |
|   =     |  +=    |    -=     |   *=    |   /=    |

|Comparação|        |           |           |             |             |
| :---: | :-------: | :-------: | :-------: | :---------: | :---------: |
| igual | diferente | maior que | menor que | maior igual | menor igual |
|   ==  |     !=    |     >     |     <     |   >=        |   <=        |

|Lógicos|  |     |
| :-: |:--:| :-: |
| and | or | not |
| and | or | not |

| Tipagem |    |     |            |      |     |       |         |     |
| :--: | :---: | :-: | :--------: | :--: | :-: | :---: | :-----: | :-: |
| list | tuple | set | dictionary | bool | int | float | complex | str |
|x=[1,2]|x=(2,1,4)|x={2,3}|x={'nome': 'Diego, 'n': 2}| True False | 1,2 | 10.3 | 34j | 'oi' "olá"|

Associação?
| in | not in |

### Notation
// -> resultado de expressão
// > texto que será impresso em console.log
// apenas um comentário

### Condicionais
if (condição) {
	bloco de código
}

### funções


def nomeFunção param1,param2,param3,...:
	processo
	return

função:
def nome (parâmetros,...):
	lógica
	return

funções lambda (funções simples de retorno simples)
Ex. S = lambda x,y: x+y

### Comentários
"""  
	Caixa de comentário: mais utilizado para descrever a função
"""  
`# Comentário de linha`

### Strings
capitalize(): Converte 1º caracter para maiúsculo
find(): Retorna o índice da 1ª ocorrência ou -1 se não tiver
index(): retorna uma exceção caso o valor não exista?
len(): Retorna o tamanho da string
split(): Divide em substrings separados pelo valor, retornando uma lista com elas
strip(): Remove espaços em branco do início e fim

### List (Arrays)
- Ordenada
- Mutável
- Permite duplicatas
- Indexação por inteiro
- Delimitada por []
Pode-se acessar os últimos valores por indice negativo: -1(ultimo), -2(ultimo)  
**array[n]**: Acessa o elemento de índice n  
**array.append(item)**: adiciona o item no final do array  
**array.insert(posição, item)**: adiciona o item no indice do array especificado  
**array[n] = item**: substitui o valor da posição n pelo item  
**array.len**: mostra o tamanho do array  
**array.pop()**: remove o ultimo elemento do array  
**array.pop(n)**: remove o elemento de posição n  
**array.remove(item)**: remove o primeiro item com o valor igual a item  
**array[n:m]**: mostra os elementos do array de indice n até o indice m, caso omitidos, o n será 0 e o m será o ultimo  
**reversed(array)**: mostra o array invertido  
**array.sort()**: Ordena alterando o array original  
**array.sort(reverse=True)**  
**sorted(array)**: Retorna o array ordenado sem alterar o array original  
**array.count(n)**: Verifica quantas vezes n repete no array  

- **range(n,m,i)**: gera uma lista com os valores
	- n : valor inicial (omissão n = 0)
	- m : valor final
	- i : intervalo (omissão i = 1)

### Dicionário (Objeto)
- Não ordenada
- Mutável
- Não permite duplicatas
- Indexação por string
- Delimitada por {}

print(f"texto {variável} texto {funcao()}")
<pre>
def busca_sequencial(lista,val):  
  for pos in range(len(lista)):  
    if val == lista[pos]: return pos  
  return -1</pre>

### Bibliotecas
Pi
from math import pi
condicionais:
if condição:
	return
elif condição
	return
else 
	return
	
print("texto",variável,função(),...)


lista.reverse (inverte a lista original
reversed(lista) inverte o output da lista que pode ser atribuido à uma variável


ENTRADA:
nome = input("Escreva seu nome") por padrão o tipo dela é string
n1 = int(input("Digite um número"))

if
elif
else

type(var)
