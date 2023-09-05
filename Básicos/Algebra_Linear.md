# Algebra Linear

## Matrizes
A mxn = [aij]mxn
Onde m representa a quantidade de linhas
Onde n representa a quantidade de colunas
Onde mxn representa a ordem dela, onde:
- 1 <= i <= m
- 1 <= j <= n

Matriz Linha: m = 1
Matriz Coluna: n = 1
Matriz quadrada: m = n
Matriz retângular: m != n
Matriz nula: todos seus elementos são zero
Prop. de diagonal principal: elementos aij onde i = j
Prop. de diagonal secundária: i + j = n + 1
Matriz identidade: sua diagonal principal possui valores 1 e os restantes 0 (apenas matrizes quadradas)
Ex.
| 1 0 |
| 0 1 | 
Matriz triângular superior: analisando a diagonal principal, todos os elementos abaixo dela devem ser 0(apenas matrizes quadradas)
Matriz triângular inferior: analisando a diagonal principal, todos os elementos acima dela devem ser 0(apenas matrizes quadradas)

Lei de formação é representado pela regra que determina os elementos, podendo essa regra ser uma função
Matrizes iguais: a ordem precisa ser a mesma e os valores da matriz devem ser iguais junto a suas colocações

### Soma e subtração de matrizes
A ordem permanece a mesma e são somados/subtraidos os elementos de mesmo i e mesmo j entre as matrizes: A12 + B12 = C12, A12 - B12 = C12 

### Produto de matriz
Por um valor escalar, (um valor qualquer) é multiplicado todos os elementos por este valor.

Amxw * Btxy = Cmxy e obrigatóriamente w = x
Já em um produto entre matrizes é multiplicado a linha da primeira pela coluna da segunda

Ex.
	| 5 2 |
	| 3 2 |
	
| 8 9 | | (5.8+9.3) (8.2+9.2) |
| 3 4 | | (3.5+4.3) (3.2+4.2) |

### Matriz transposta
Inverte, as linhas viram colunas e as colunas linhas. Invertendo os índices ex. a posição de A4x5 será na transposta A5x4

### Matriz inversa
A matriz inversa de uma matriz é uma matriz a qual multiplicada pela matriz original resulta na matriz identidade.

Ex.
				|     |
				| 3 2 |
	
| 1 2 | | 1 0 |
| 0 4 | | 0 1 |

Em casos onde não se sabe a matriz original ou a inversa, cairá em um sistema de equações onde pode-se utilizar soluções com 


Determinante teorema de laplace
Primeiro passo é escolher uma linha ou coluna.
Conseguir o cofator de cada elemento da linha/coluna escolhida.

cofator: Cof. aij = (-1)^(i+j).Dij
Onde Dij é o determinante da matriz que sobra retirando a linha e coluna de aij

É feito o somatório do resultado dos cofatores do elemento multiplicado pelo elemento
Somatório = aij . C aij + ...