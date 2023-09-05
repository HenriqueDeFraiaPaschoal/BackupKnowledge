# C
(C)[https://pt.wikipedia.org/wiki/C_(linguagem_de_programa%C3%A7%C3%A3o)] é uma linguagem de programação criada por Dennis Ritchie, de:

- Médio nível de abstração
- Tipada
- Compilada (criando um arquivo .exe)
- Extensão para salvamento .c

Ide usada (Code::Blocks)[https://www.codeblocks.org/]?

## Sintaxe
| Tipagem |        |                    |                  |       |        |
| :--: | :-------: | :----------------: | :--------------: | :---: | :----: |
| char | short int | unsigned short int | int(ou long int) | float* | double* |
|8bits | 16bits(-32768 32767|16bits(0 a 65535)| 32bits(-2147483648 a 2147483647)|32bits(0 a 4294967295)| 32bits 6 digitos de precisão|64bits 10 digitos de precisão|
*A separação das partes fracionárias se da pelo ponto . e não pela vírgula , como no português

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

### Variáveis e Constantes
Recomendável declarar no início de cada (módulo)[#Funções/Módulos]

Variáveis:
int dia, mes, ano;
char sexo;
float salario;

Constantes:
const int pi = 3.141592;
const char sexo;

### Comentários
Um texto de comentário é ignorado pelo compilador. Este pode ser escrito após duas barras ou barra estrela estrela barra.
// Texto de comentário  
/* Bloco de texto
de comentário */


### Funções/Módulos
Possuem *tipo de retorno*, *nome*(primeira letra de Aa a Zz, as demais são alfanuméricos, não sendo uma palavra reservada), *lista de parâmetros tipados*, *bloco de comandos { }*.
É necessário o uso de ponto e vírgula ; no final de cada comando.  
Uma função pode não ter parâmetros *()* e nem retorno *void*.  


Os nomes não podem utilizar palavras reservadas, algumas delas: break, case, char, const, default, do, double, else, enum, float, for, if, int, long, return, short, sizeof, struct, switch, typedef, union, unsigned, void, while, etc.

### Importando módulos 
`#include <nomeDoArquivoQueSeráImportado`

#### Módulo Printf/Scanf
| Identificadores |        |                    |                  |       |        |    |     |
| :------: | :-----------------------: | :-------: | :----------------: | :--------------: | :---: | :----: | :----: |
| caracter | Inteiro decimal com sinal | Inteiro decimal com sinal | número com decimal | número com decimal double | texto | Inteiro decimal sem sinal | Escreve o símbolo % |
| %c | %d | %i | %f | %lf | %s | %u | %% |

Utilizado para imprimir algo na tela
`#include <stdio.h>`
int dia, mes;
printf("oi");
scanf("%d", &dia);
scanf("%d", &mes);
printf("Você tem %d dias e %d meses para realizar o pagamento", dia, mes);


#### Módulo Getch
Utilizado para ler uma única tecla
`#include <conio.h>`
getch();
*a função acima aguardará o pressionamento de qualquer tecla, comumente usada para dar uma pausa*