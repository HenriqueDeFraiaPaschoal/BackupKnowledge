# JavaScript

[JavaScript](https://en.wikipedia.org/wiki/JavaScript) ou JS é uma linguagem de programação interpretada estruturada, de script em alto nível com tipagem dinâmica(o tipo das variáveis pode mudar) fraca e multiparadigma, muito dissiminada e utilizada.
Interpretadores dessa linguagem podem ser encontrados em todos os navegadores como: FireFox com SpiderMonkey e Chrome com V8.
Em 2009 o V8 do Chrome foi integrado em um programa em C++ o qual é chamado de [Node](https://nodejs.org/en), permitindo "rodar" códigos JS fora do navegador, permitindo a criação de backend também em JavaScript.
ECMAScript são especificações/padrões que o JavaScript segue para seu desenvolvimento.

Padrões
Comentários no código é utilizado barra dupla //
Separado um arquivo chamado index.js, linkado via `<script src="./index.js"></script>`

block scope
function scope
global scope

## Instalação do NODE

Pq instalar o node?
Várias bibliotecas que podem ser utilizados futuramente para o desenvolvimento, podem necessitar do node instalado para sua execução.
npm -> Node Package Manager

Basics
Variáveis
É case-sensitive
Utiliza camelCase
O nome dela não pode começar com um número e não pode utilizar as palavras reservadas(if, else, let, ...)
var - não utilizado mais devido a vazamento de escopo entre outros problemas(seu escopo é de função, no navegador quando declarada globalmente, ela é anexada ao objetov window)
let - para variáveis que podem ter seu valor reatribuido(seu escopo é de bloco)
let/const name = value;(seu escopo é de bloco)
const - para variáveis com valor fixo
let name; // Variável iniciada com valor undefined
let idade = 27;
const name = 'henrique', lastName = 'Paschoal'; // Não muito utilizado, normalmente 1 declaração de variável por linha
const deve ser a declaração padrão, usar let apenas se for reatribuir valores

primitives types of values
are copied by their value
quando referenciados, o valor deles é acessado e copiado ex. x=1 y=x x=2 (no final x=2 e y=1)
[string](link string junto com os contra barra simbolo para uso ex. \')
boolean
number
symbol
undefined // O valor de undefined é de tipo undefined
null // Usado em situação que queremos limpar o valor de uma variável, o valor null possui tipo object

reference types
are copied by their reference
quando referenciados, o valor deles é apontado e guardado, ex. x={n:1} y= x x={n:4} (no final x={n:4} e y={n:4} pois possuem a mesma referência)
object
function (que também é um objeto)
array (que também é um objeto)

arrays
possui tipagem de objeto. Por isso ele recebe métodos quando é criado, como filter, every, length etc.
O tipo e o tamanho de um array é dinâmico também. Pode receber elementos de tipagens diferentes
let cores = ['amarelo', 'vermelho', 'azul', 'branco'];

objetos
let person = {
  name: 'Henriqeu',
  sobreNome: 'Paschoal',
  idade: 27
}

person.name ou person[name] acessa o valor de name, com colchetes pode adicionar variáveis
person.hobbie = 'games'; // Cria um novo atributo (chave:valor)
delete person.hobbie; // Deleta um atributo
Object.keys(obj); // Retorna um array com as chaves do obj
if ('name' in person) // Verifica se o objeto possui a chave 'name'
Object.assign({}, obj1, obj2...) // Adiciona os atributos de um ou mais objetos à um objeto (podendo ser ou não vazio)
let another = { ...person } //Spread, clonar um objeto
usar === verifica se possuem a mesma referência

funções
Em javascript funções também são objetos. O que fica claro quando você consegue acessar métodos dele através de funcao.metodo
É uma sequência de ordens que ou executam uma tarefa ou/e retornam um valor
function (parametro) {}
function // Traz a função como um "objeto"
function(argumento) // Executa a função

person.name = 'Henrique'; // Escolha padrão para acessar dados de um objeto
person['name'] = 'Henrique'; // Possui seus casos de uso específicos, como usar uma variável no lugar de 'name'

O ideal é deixar o script no final do elemento body. Pois devido a leitura ser de cima para baixo, o sistema terá lido todos elementos antes de iniciar o script, evitando problemas do código tentar pegar elementos que ainda não foram carregados. Alem de carregar a página inicial e não perder muito tempo no código enquanto a tela está em branco para o usuário, dando a impressão de que travou.

Operadores
aritimetricos(+:soma, -:subtração, *:multiplicação, /:divisão, %:resto de divisão, **:exponênciação,
 ++:incrementador, x++ é lido o valor de x e depois incrementado, ++x é incrementado e depois lido o valor de x
 console.log(10++) mostra 10
 console.log(++10) mostra 11 )
 --:drecrementador

atribuição
+=
-=
*=
/=

comparação
relacional

<

> =
> <=
> igualitário?equality
> ==: apenas mesmo valor
> ===: estritamente igual, mesmo tipo e mesmo valor(padrão a ser usado)
> !==:

lógica
&&: e ou and, verifica se ambas expressões são verdadeiras
||: ou ou or, verifica se pelo menos 1 expressão é verdadeira, retorna o primeiro valor truthy
!: not, entrega o oposto do valor

O retorno de uma expressão lógica pode não ser necessáriamente true ou false, ex. false || 'Henrique' || 'Paschoal' retorna 'Henrique'
Short-circuting ou curto-circuito em uma expressão
corEscolhida: 'branco;
corPadrao: 'vermelho';
cor = corEscolhida || corPadrao; // Exemplo de uso
falsy: undefined, null, 0, '', false, NaN

bitwise
no binário, a cada 8 elemento representa 1bit : 1 = 00000001, 2 = 00000010
console.log(1 | 2) // Bitwise OR, verifica os bits e mantem os 1, 00000011
console.log(1 & 2) // Bitwise AND, verifica os bits e se ambos forem 1 retorna 1, 00000000
ex. É possível definir permissões de usuário com apenas 1bit
read permission 00000100, write 00000010, execution 00000001 (R--:4, -W-:2, --E:1)
let readP = 4;
let writeP = 2;
let executeP = 1;

let myPermission = 0;
myPermission = myPermission | writeP;

let message = (myPermission | readP) ? 'yes' : 'no'
retorna No

ternário
verificação ? caso true : caso false

Control Flow

### Arrow Function

let func = () => {}
o parenteses pode ser omitido caso hava apenas um parametro e as chaves também caso haja apenas uma linha de código que será retornada
let print = a => console.log(a);

### if

if(condition) {
    statement
  }
else if (condition){
    statement
  }
...
else statement

### SwitchCase

let role;
switch (role) {
  case 'case1':
  statement;
  break // se não tiver o break ele pula para o próximo case.
  case 'case2':
  statement;
  break
  ...
  default:
  statement;
}

Loops
Lembrar, se existe loops dentro de loops, seria bom quebrar a lógica em 2 funções e chamar uma dentro da outra.
Cada função simples e com um objetivo específico.

### For

for (initialExpression; Condition; IncrementExpression) {
  statement;
}

Ex.
for (i = 0; i < 5; i++) {
  if (i % 2 !== 0) {
    console.log('É impar');
  }
}

### While

Pode ter um break caso queira parar o loop por algum motivo, ou continue caso você queira que ele volte a se repetir parando ali

while (condition) {
  statement
}

Ex.
let i = 0;
while (i < 5) {
  console.log('Olá', i)
  i += 2
}

### DoWhile

A diferença entre o while é que será executado a primeira vez independentemente.
Pode ter um break caso queira parar o loop por algum motivo, ou continue caso você queira que ele volte a se repetir parando ali

do {
  statement
} while (condtion);

### For In

for (let key in object) {
  statement
  console.log(key, object['key'])
}

for (let index in array) {
  statement
  console.log(array[index])
}

### For Of (only arrays and maps)

for (let element of array) {
  statement
  console.log(element)
}

### Factory Functions

Nome da função é camelNotation
function createCircle (radius) {
  return {
    radius, // Cria já uma chave com o nome radius recebendo o valor de radius como valor ou escrever radius: radius
    locationX: 5,
    locationY: 10,
    drawType() {
      console.log('Circle');
    }
  };
}

const circle1 = createCircle(1);
console.log(circle1);
const circle2 = createCircle(2);
console.log(circle2);

### Constructor Functions

Nome da função PascalNotation
function Circle(radius){
  this.radius = radius;
  this.draw = function() {
    console.log('draw');
  }
}

const circle = new Circle(1);

### THIS e NEW

this está relacionado ao objeto que está executando o código
ex. se o this está em um método, ele referência ao objeto que o executa
    se o this está em uma função ele referência globalmente(window em navegadores)

Para mudar o this de uma função
.call({}, arg1, arg2,...) // Chama a função com os argumentos mudando seu this
.apply({}, [arg1, arg2, ...]) // mesma coisa mas diferente
.bind({})() // Muda permanentemente o this de uma função sem chama-la ou chamando-a colocando () no final

OU ARROW FUNCTION
arrow function herdam o this do bloco que estão

new cria um novo objeto vazio para encapsular

### Build-in Objects

Math
.PI()
.random()
.round(arg)
.max(arg)
.min(arg)

Métodos para strings
.length
.includes()
.startsWith()
.endsWith()
.indexOf('a') //mostra o index do primeiro match
.replace(arg1, arg2) // Retorna uma nova string com a primeira palavra/caracter encontrada pela segunda
.toUpperCase
.toLowerCase
.trim ou .trimLeft ou .trimRight // Retira espaços das pontas
.split(arg) // Retorna um array com os pedaços da string os quais foram separados pelo argumento

Métodos para arrays (Podem ser encadeados, mas colocando um em cada linha)
array1 = x
copy = array1 //copia a referencia do array
copy = ...array1 // copia individualmente cada elemento do array para o novo array
.push(arg1, arg2,...) // Adiciona os elementos no final do array
.pop() // remove o ultimo elemento
.shift() // Remove o primeiro elemento
.unshift(arg1, arg2, ...) //Adiciona os elementos no começo do array
.splice(startPosition, deleteQuantity, arg1, arg2, ...) // Adiciona elementos no meio
.splice(startPosition, deleteQuantity) // Deletar elementos no meio
.length
.indexOf(arg, startIndex) // Retorna o index do primeiro match ou -1 se não encontrar
.lastIndexOf(arg) // Retorna o index do ultimo match ou -1
.includes(arg) // Retorna bolleano há arg no array (não funciona com array de objetos)
.find((e)=>{}) // Retorna o elemento ao qual o função passada retorna true

- findIndexOf
  .map
  .reduce
  array = []; // Zera um array mas se tiver outros elementos referenciando-o, é mantido 2 referências ocupando memória
  .length = 0 // Zerar os elementos de um array
  .concat(array) // Retorna um array concatenando-os, pode ser atribuido a uma variavel
  .slice(startIndex, EndIndex) // Retorna o array cortado nos index, caso omitido retorna uma copia
  ...array // Espalha os elementos do array dentro de uma variável
  ex. const combined = [...array1, ...array2]
  .forEach((e,index)=>{},this.arg) // Para cada elemento do array, sendo ele o argmento para a funççao, this.arg pode ser omitido
  .join(',') // Retorna uma string com os elementos juntados com o argumento entre eles
  .sort() //Ordena os elementos de acordo com ASCII
  .sort((a,b) {
  const A = a.key.toLowerCase()
  const B = b.key.toLowerCase()
  if(A < B) return -1
  if(A > B) return 1
  return 0
  }) //Para objetos
  .reverse() //Ordena em ordem decrescente
  .every((e)=>{return true ou false}) // Verifica se todos elemtnos do array condizem com a função especificada
  .some((e)=>{}) // Verifica se pelo menos 1 elemento condiz com a função
  .filter((e)=>{}) //Retorna um array com os elementos que condizem com a função
  .map((e)=>{}) // Jogar o retorna como um novo elemento de um novo array
  .reduce(((acumulador, e)=> {acumulador+e}), ValorInicialAcumulador)
  Caso omitido o valor de acumulador, ele será o primeiro elemento do array

Array.isArray(objeto) // Verifica se o objeto é um array e retorna um boleano

Arrow Function
() => {return}
ou
se tiver apenas um parametro pode omitir () e se tiver apenas uma linha pode omitir o return e as {}

### Template Literal

Usando crase para iniciar e fechar e sifrão e colchetes
Ex. `Este texto é ${color} com idade ${calculaIdade(person.birhDate)}`

### Console

console.log
console.error

### Function Expression

Essas só podem ser chamadas após sua atribuição
Pois o hoisting(mover as funções para a parte de cima do código) só funciona com funções declaradas e não com variáveis
run(); // Não vai chamar a função
const run = function () {};
run();

### Arguments Rest Operator

O restOperator deve ser sempre o último argumento da função
Converge os ultimos elementos extras (alem dos dos parâmetros) em um array
function sum (dicount, ...args) {
  total = args.reduce((a,b) => a + b);
  return total * (1 - discount);
}
console.log(sum(0.1,1,2,3,4,5,6,7));

### Spread Operator

É usado para meio que "abrir" o objeto e espalhar pela função. Como se você retirasse a chaves ou colchetes
ex. array1 = ['henrique', 'igor', 'duda', 'eliane']
array2 = ['victor', 'ael']
array2.push(array1) -> vai empurrar o array inteiro, para mandar cada elemento de 1 individualmente para 2 usa-se o spread
array2.push(...array1)

Pode ser usado em objetos para adicionar o conjunto de chave/valor em um outro objeto ou array

### Destructuring

Desestrutura um elemento e já guarda em outra variável. Parecido com o spread
let array1 = ['a', 'b', 'c', 'd']
let [e1, e2, ...en] = array1; -> cria uma variável e1 com o primeiro valor de array1 e uma variável e2 com o segundo, e cria um array en com os valores restantes

let obj = {
  name: 'henrique',
  age: 28
}

const { name:nomeIndividuo, age } = obj; -> cria constantes pegando os valores com os mesmos nomes da chaves, podendo manter o nome chave ou não
foi criado:
const nomeIndividuo = 'henrique'; e const age = 28;

### Arguments Default Valor

Todos os valores após o primeiro com um valor padrão também devem possuir valor padrão
Caso contrário na hora de passar os argumentos, os com valores padrão devem receber undefined
function interest (arg1, arg = 3,)

### Getters and Setters and Static

Podem ser utilizados para melhorar a segurança e impedir reatribuições erradas, além de adicionar lógicas extras quando for feita uma leitura ou adição/atribuição de algum valor.
const person = {
  firstName: 'Henrique',
  lastName: 'Paschoal',
  get fullName () {
    return `${person.firstName} ${person.lastName}`
  },
  set fullName (value) {
    const parts = value.split(' ');
    this.firstName = parts[0];
    this.lastName = parts[1];
  }
};
person.fullName = 'Henrique Fraia';

static deixa a função livre para ser acessada sem que a classe seja necessáriamente instânciada.
Variáveis e funções estáticas só podem ser acessadas dentro da classe por outros estáticos. Acessando apenas com nomeClasses.propriedade

### Try and Catch

quando há um trow new error o código é parado e dado sequencia ao catch
const person = {
  firstName: 'Henrique',
  lastName: 'Paschoal',
  get fullName () {
    return `${person.firstName} ${person.lastName}`
  },
  set fullName (value) {
    if (typeof value !== 'string')
      throw new Error('Value is not a string');

    const parts = value.split(' ');
    this.firstName = parts[0];
    this.lastName = parts[1];
  }
};

try {
  person.fullName = 'Henrique Fraia';
}
catch (e) {
  alert(e)
}

### OOP

Object-oriented programming, programação orientada à objeto
Com o uso de classes é possível criar plantas/padrões para a construção de objetos.
Criando objetos que possuem um mesmo padrão/função.
O nome inicia maiusculo.

class Department {
  constructor(n) {
    this.name = n;
  }
}

const accounting = new Department('Accounting');
// O new chama o constructor e os valores passados em () vão nos argumentos do constructor

### ESCOPO

typeof

Date Objects
.toISOString()
.toLocaleString('en-US', { month: 'long' })
.toLocaleString('en-US', { day: '2-digit' })
.getFullYear()

nota: '10';
nota2: '5';
+nota + +nota2; // Converte a string para número ?

[ECMA 6 COMPAT](https://kangax.github.io/compat-table/es6/)
[Erros JS Contraintuitivos](https://github.com/denysdovhan/wtfjs)
