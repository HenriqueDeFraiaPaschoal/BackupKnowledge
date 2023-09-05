# Java
[Eclipse](https://www.eclipse.org/downloads/) é o padrão de mercado?
precisa-se instalar o JDK(Java Development Kit) para poder utilizar acessível no [link](https://www.oracle.com/br/java/technologies/downloads/)
instala java e o javac(compilador de java)
O jdk compila os arquivos .java em arquivos.class que são binários e podem ser interpretados pelo computador
javac file.java
java file.class

JAR (Java ARchive) é o arquivo executável criado.
precisa do arquivo manifest.mf(contendo o texto Main-Class: arquivoComMain (enter para ter uma quebra de linha)) para saber onde está a função main
jar -cvfm myProgramName.jar manifest.mf *.class (Create Verbose File, Manifest, *.class pega tudo abaixo)
java -jar arquivo.jar (executa o programa, pode ser executado tbm dando dois cliques no arquivo.jar)
jar -tvf arquivo.jar (table of contents, verbose, file) 
jar -xvf arquivo.jar (extract verbose file)


Tipagem

? extends ClassName // ? pode ser um tipo qualquer, utilizado quando o tipo da variável não importa

void (Apenas para funções, usado para funções que não retornam nada)

byte (1byte max +-127)
short (2bytes máximo de +-32767)
int (4bytes 32bits 2³², um bit é separado para o sinal variando então 2³¹ de -2147483647 à +2147483647)
long number = 9875321L (o L no final é para especificar que é long)
 
float (4bytes)
double (8bytes com decimais)

boolean (true | false)

char (um caracter 'x')
String

int [] nome = new int[n de elementos] // todos elementos não atribuidos começam com valor 0 ou null

ou String[] nomes = new String[] {"henrique", "Pedro", "Joao"}
nome[0 a 99] = 1035;
*String não é um tipo primitivo
.length() --> retorna o tamanho do texto
.substring(n) --> retorna o restante da string contanto o indice n para frente
.substring(n,m) --> pega a string contanto de n (incluida) até m (excluida)
.equals(string2) --> maneira correta de se comparar strings
.equalsIgnoreCase(string2) ---> compara sem caseSensitive
.charAt(n) ---> mostra o caracter no indice n
.indexOf(string, n) --> retorna o primeiro indice onde encontrar o início da ocorrência da string, começando a busca em n (caso omitido começa no indice 0)
.lastIndexOf(string,n) --> mesma coisa mas a última ocorrência e começando pelo último indice

Esses são os tipos primitivos, pode-se criar seus própios tipos. Classes também podem ser a tipagem de uma variável

Condicionais
if (Statement) {
  codeblock
} else if (Statement) {
  codeblock
} else {
  codeblock
}

while(condição) {
  codeblock
}
// break pode ser utilizado para quebrar o loop prematuramente

switch (variable){
  case x: codeblock;
  break;
  case y: codeblock;
  break;
  default: codeblock; // Se nenhum caso for atendido, será executado o default
  break;
}

Funções
System.out.println(String); (sysout)

Construtores da classe é uma função dentro da classe com o mesmo nome da classe:
public class Human {
  public Human(){
    
  }
}


for (int i = 0; i < x.lenght(); i++) {
  code block
}

Interface
Interface é um contrato que uma classe ira ter as funções implementadas de uma outra classe, uma classe pode ter várias interfaces
public interface flyable {
  public void fly();
}

public class sparrow extends bird implements flyable {
  public void fly();
}

Herdar
Uma classe pode herdar apenas uma outra
public class Bird extends Animal {
  public Bird(args de animal) {
    super(preenchimento dos args) // é uma função de construção que compatibiliza a construção da classe com a classe herdada
  }
}
a classe bird herda as funções de animal tbm


Abstrato
uma classe que possui métodos abstratos só pode ser abstrata, e classes abstratas só podem ser extendidas e nunca instanciadas
é como se você deixa-se funções que são necessárias mas que devem ser implementadas na extensão pois pode mudar dependendo do filho
A função abstrata não possui o corpo de código {}

public abstract move();

Modificador de acesso:
Se não específicado, fica visível apenas dentro do mesmo pacote
public - Acessível de qualquer local, inclusive outros pacotes
private - Acessível apenas dentro do primeiro escopo em que se encontra(classe ou arquivo.java)

static - pode ser acessível pela classe padrão, quando não é static só pode ser acessível por uma instância da classe.
Se está como static, não pode/deve ser utilizado por uma instância

pode-se declarar duas funções de mesmo nome porém com tipos de parâmetros diferentes, ex psv print(int x){} ou psv print(String x){}
dependendo do valor usado como argumento, será escolhido o método certo

shift + F6 ---> executa o código no da aba no netbeans  
F6 ---> executa o código principal
\n ---> quebra de linha  
\t ---> tabular(identar)  
`\\` ---> mostra uma \ no texto  
// ----> comentário
System.out.print("texto") ---> imprimi no console sem quebra de linha após  
System.out.println("texto") ---> imprimi no console com quebra de linha após  
System.out.printf(%s%n%s... "texto","texto") ---> imprimi de força mais simplicada vários textos.

import java.util.Scanner; ---> importa as funções de "input" pro java

final = const

incremento i ++ ou i += n

public String toString() {
  return "texto";
}
// método utilizado para imprimir algo expecifico ao tentar imprimir o objeto


import java.util.Scanner;
Scanner inputInstance = new Scanner(System.in);
String variable = input.nextLine(); // Atribui à variável o valor escrito na linha pelo usuário
input.close();


import java.io.*;
try(File fileName = new File("myfile.txt);
  Scanner input = new Scanner(file);){
  while(input.hasNextLine()) {
    String line = input.nextLine();
    System.out.println(line);
  }
  input.close();
} catch (FileNotFoundException e) {
  System.out.println("File not found");
} finally {

}


public int subtract10 (int number) throws Exception {
  if (number < 10) {
    throw new Exception("O número passado era menor que 10");
  }
  return number -10;
}


Creating own exception
public class FooRuntimeException extends Exception {
  public FooRuntimeException(String message) {
    super(message);
  }
}
throw new FooRuntimeException("mensagem");


Generics
List ("pai" dos tipos das listas abaixo) - usar essa 
ArrayList
LinkedList

HashSet(Não aceita valores repetidos e a ordem de entrada não é mantida)
LinkedHashSet(Não aceita valores repetidos e a ordem de entrada é mantida)
TreeSet(é guardado os valores em ordem(numerica, alfabetica,etc.))

List<type> li = new ArrayList<type>(hashSet); criar uma lista com conteudo de um hashset

import java.util.ArrayList;
import java.util.LinkedList;

type não pode ser primitivo
capacity inicia com 10 caso omitida
ArrayList<type> variable = new ArrayList<type>(capacity); // guarda tudo dentro como um objeto e usa o tipo de array(cria um array de 10, se passar cria um de 20 com os 10 anteriores, dobrando o tamanho e clonando os elementos a cada etapa) faster to manipulation, slower to retrivel
LinkedList<type> variable2 = new LinkedList<type>(); // mesma coisa mas com estrutura de nodo, vai adicionando arrays linkados entre si slower to manipulation, faster to retrivel
type pode ser String, Integer, Float, 
variable.add("Heelo");
variable.get(0);
variable.remove(n); remove o primeiro ou o elemento n
variable.size();
variable.addAll(arrayListVariable);
variable.removeAll(arrayListVariable);
variable.clear(); Apaga tudo
variable.contains(x); retorna um booleano se tem ou não o valor passado
variable.isEmpty(); retorna booleano se a lista está vazia
variable.retainAll(arrayListVariable); apaga tudo que não está nos valores
Collections.sort(variableList); ordena a lista

ArrayList<Vehicles> vehicles = new ArrayList<Vehicle>();
Vehicle vehicle2 = new Vehicle("Toyota", "Camery", 12000, false);

vehicles.add(vehicle2);
vehicles.add(new Vehicle("Honda", "accord", 12000, false));

for each
for(String value: variable) { // coloca o tipo das variáveis do array e cada valor dela será passado para value
  sysout(value);
}

// o ultimo tipo pode ser omitido, ele será igual ao o tipo da variável
HashMap<KeyType, ValueType> dictionary = new HashMap<KeyType, Value,Type>();
LinkedHashMap<KeyType, ValueType> dictionary = new LinkedHashMap<KeyType, Value,Type>();
TreeMap<KeyType, ValueType> dictionary = new TreeMap<KeyType, Value,Type>(); (guarda os itens em ordem alfabetica, numericas, etc)
dictionary.put(key, value);
for (KeyType x: dictionary.keySet()) {sysout(x)}
for (KeyType x: dictionary.keySet()) {sysout(dictionary.get(word))}
for (Map.Entry<KeyType, ValueType> x: dictionary.entrySet()) {
  sysout(x.getKey());
  sysout(x.getValue());
}


implements Comparable<Employee>

public int compareTo(Employee o) {
  if(this.salary < o.salary) {
    return -1; // menor
  } else if (this.salary > o.salary) {
    return 1; // maior
  }
  return 0; // igual
}


## Generics


## multthread
can't start a thread more than once in the same instance

Thread.currentThread().setName(); // pega o nome da thread
Thread.currentThread().getName(); // pega o nome da thread

try{
Thread.sleep(10); //para por 10 milisegundos
} catch (InterruptedException e) {
  sysout(e)
}

psvm () {
  Task taskRunner = new Task();
  taskRunner.start();
  sysout("Hello");
}


class Task extends Thread {
  public void run() {
    for(int i=0; i < 1000; i++) {
      sysout("Number", i)
    }
  }
}


synchronized { codeBlock }
synchronized (this) { codeBlock } // para instâncias de objetos
ou adicionar na classe
publick synchronized int getNext() {
  code block
}


boas práticas
criar toString
criar o construtor
criar o equals e hash
criar compareTo