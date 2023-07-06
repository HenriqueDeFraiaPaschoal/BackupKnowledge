# TypeScript
TypeScript é um superSet de JavaScript. A linguagem do javaScript adicionado de outra funções.
Em typeScript a tipagem não é mais dinâmica. Logo não é possível atribuir um valor de tipagem diferente à uma variável que já foi inicializada com outra tipagem.
TS não é executado por navegadores/node, é necessário converter. Esta conversão não é apenas de linguagem do typescript para javascript, também pode ser de typescript moderno para javascript antigo.
A 'funcionalidade' dele é, ajudar durante a complicação/desenvolvimento, encontrar erros de lógica e tipagem no código. Ele não muda nada no 'runtime' do código. 
Extensão .ts
Instalando:
npm install -g typescript

tsc file.ts -> compila o arquivo em javascript
tsc file.ts --watch ou -w -> Deixa um arquivo sendo "observado" e atualizando a compilação sempre que o arquivo é salvo

tsc --init -> transforma o diretório em um diretório observado por typescript
após isso rodar tsc no terminal compila todos arquivos ts
tsc --watch -> observa todo o diretório por salvamentos e compilando novamente

### Tsconfig.json
Muitas das configurações comentadas, apesar de comentadas, já possui valores padrões e estão ativas. O uso delas são em situações específicas.
sourcemap -> Adiciona um arquivo map que fornece um documento de analise para o navegador. Útil para debugar código vendo o processo de leitura do códio pelo navegador em Sources. Muito bom com a extensão do chrome para debugar no vscode.
outdir -> usado para especificar uma pasta à qual será salvo os arquivos.js compilados.
removeComments -> remove os comentários durante a compilação
"noEmitOnError": true -> não cria os arquivos js caso haja erro no ts

Em strict como padrão tudo está true. Define os padrões do que é permitido ou não. Por exemplo se os parâmetros de uma função deve ou não possuir tipagem.

Em aditional checks é bom ligar unUsedLocals, unUsedParam e noImplicitReturns

Algumas configurações extras podem ser adicionadas após o primeiro valor, adicionando uma vírgula no final do objeto e adicionado a chave/valor desejado.
"excluse": "node_modules"    Exclui um arquivo ou pasta da compilação automática via tsc --init e tsc ou tsc -w, por padrão já tem node modules definido
"inclue": "arquivo.ts"       Por padrão já vem com todos arquivos, tendo que especificar todos caso queira especificar um arquivo
"files": "diretório"         Mesma coisa mas com diretórios

Types cores(all lowerCase)
number
string
boolean(no truthy or falsy)
object
array
tuple
Enum
Any

ex.
function (n1: number, n2: number) {
}

// Em objetos e arrays, o ideal é dexar o typescript definir os tipos conforme os elementos são atribuidos
const object: {
  CPF: number;
  nome: string;
  empregado: boolean;
} = {
  CPF: 0000000,
  nome: 'Henrique',
  empregado: true
}

const nomes string[] = ['henrique', 'paschoal'];
const person [string, number | string] = ['henrique', 28];

### Enum
Cria e da um valor iniciando em 0 ou a partir do valor explicito no anterior, para os elementos atribuidos. ADMIN = 0, READ_ONLY = 5, AUTHOR = 6.
enum Role { ADMIN, READ_ONLY = 5, AUTHOR };

### Type Alias
type Combinados = {
  number | string
}

type Dados = {
  name: 'Henrique';
  cpf: number;
}

### Void
É a tipagem dada a uma função que não possui retorno.
Apesar do retorno dela ser definido com undefined...

### Function types
let combine: (a:number, b:number) => number;

### Unknown
Quase a mesma coisa de any, mas ele ainda é verificado. Seria um any mantendo a verificação se o tipo esperado é compatível com o tipo armazenado em uma variável com unknown

### Never
Uma função que retorna nada devido uma pausa/break/error ou que fica em um loop infinito. Uma função pode ter o retorno de tipo never


class Department {
  private name: string;

  public constructor (n: string) {
    this.name = n;
  }
}

class Product {
  title: string;
  price: number;
  private isListed: boolean;
 
  constructor(name: string, pr: number) {
    this.title = name;
    this.price = pr;
    this.isListed = true;
  }
}

const accounting = new Department('Accounting');

extends aproveita uma classe já criada e usa como parte na criação de uma nova mas com adições. É necessário usar o super.
private -> deixa privado sendo acessado apenas pela própria classe
public
protected -> deixa privado mas pode ser acessado tanto pela própria classe como por classes que usem-a como extensão


É preciso instalar node antes para utilizar!
[TypeScript Download](https://www.typescriptlang.org/)


