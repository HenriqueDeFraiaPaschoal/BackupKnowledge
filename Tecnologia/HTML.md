# Hyper Text Markup Language HTML

O HTML é uma linguagem de marcação de texto que segue uma estrutura do tipo árvore. a qual utiliza tags/etiquetas para fazer sua marcação. Seus arquivos são documentos de texto como outro qualquer, o que o difere de tantos outros são suas tags, estruturas e funcionalidades.

Exemplo de estrutura de árvore:

                                     ┌────────┐                
                                     │  HTML  │                
                                     └───┬────┘                
                          ┌──────────────┴─────────────┐       
                    ┌─────┴─────┐                 ┌────┴────┐  
                    │   BODY    │                 │  HEAD   │  
                    └─────┬─────┘                 └─────────┘  
               ┌──────────┴────────┐                           
      ┌────────┴─────────┐  ┌──────┴───────┐                   
      │   Container 1    │  │   Element 1  │                   
      └────────┬─────────┘  └──────────────┘                   
        ┌──────┴─────────┐       
  ┌─────┴──────┐    ┌────┴───────┐  
  │ Element1.1 │    │ Element1.2 │  
  └────────────┘    └────────────┘  

Uma estrutura de marcação facilita a distinção ou tratamento de determinados elementos pelo computador/usuário conforme sua marcação.  
Por exemplo o título inicial apenas foi reconhecido como um título e não um texto qualquer devido a marcação colocada no texto. Apesar da estrutura deste documento ser MarkDown, o HTML segue o mesmo conceito.

O objetivo da marcação pode ser resumido em descrever semânticamente ou dar sentido ao texto.

- Hyper Text: texto que referência outro texto que o UserAgent disponibiliza para o usuário acessar
- Markup: Marcação pois utiliza de marcações/tags para dar sentido e facilitar a interpretação do texto.
- Language: Linguagem pois precisa seguir padrões e normas para que seja mutualmente interpretado facilitando a comunicação

## O que são tags?

Resume
Henrique Paschoal

Informação de contato
endereço: Rua x
Numero x

Como podemos mostrar o que cada parte representa?
Henrique Paschoal meu nome
Mas onde meu nome começa e termina?
(meu nome)Henrique Paschoal(meu nome)
Mas quando é o começo de um nome e final? E como identificar se é um texto entre parentes ou uma marcação?
`<nome>Henrique Paschoal</nome>`
podem ter atributos
`<nome nickname=true>Henrique Paschoal</nome>`
Isso é um elemento

Porém seguindo as especificações, cada tag possui um [conteúdo](https://html.spec.whatwg.org/#content-models) esperado dentro dele



User Agent: navegador(fornece dados de forma visual), leitores de telas(fornece dados de maneira lida), googlebot(lê e categoriza sites), software que trabalha para o usuário e tenta interpretar os documentos

## Tags comuns e mais usuais 

### Metadata
lang -> [abreviacoes](https://www.w3schools.com/tags/ref_language_codes.asp)


### Sections
[**detail**]():  
[**preview**]():  
[**article**](): 
caracteriza um elemento onde o seu conteúdo é independente. Seu conteúdo é um elemento que sozinho consegue representar algo sem a necessidade de elementos anteriores/pais.  
[**aside**](https://html.spec.whatwg.org/#the-aside-element): 
um conteúdo tangencialmente relacionado ao principal  
[**section**](https://html.spec.whatwg.org/#the-section-element): 
um container genérico que serve para novos conteúdos, pode ter seu próprio header e footer   
[**h1, h2, h3, h4, h5, h6**](https://html.spec.whatwg.org/#the-h1,-h2,-h3,-h4,-h5,-and-h6-elements): 
Títulos, subtítulos, cabeçalho, do elemento onde está contido. Sendo h1 o maior/principal e o h6 o menor/secundário  
[**footer**](): 
 Um elemento de rodapé do conteúdo de seccionamento que está contido, apenas 1 por conteúdo  
[**adress**](): 
Elemento que contém dados de contato do elemento article ou body mais próximo
[**img**](): 
src="img_girl.jpg" alt="Girl in a jacket" propriedades
### Grouping Content
[**p**](): Um parágrafo, um conjunto de frases que discutem um mesmo tópico  
[**blockquote**](): Uma seção para citação ou referência  
[**ul**](): Uma lista de itens não ordenados, lista de itens que a mudança de ordem não muda o sentido da lista  
[**ol**](): Uma lista ordenada, lista de itens que seguem uma ordem específica
[**li**](): Itens de uma lista  
[**dl**](): Lista de chave/valor, uma lista de itens que possuem um titulo/termo e uma definição/valor
[**dt**](): Termo/chave de um item em uma dl  
[**dd**](): O valor/definição de uma dl  
[table]():
thead
tbody
tfoot
tr
td : colspan="2"
div
img href alt 


Texto
strong
b
em
i
small
span

Anchor tags
a:
-href
-target
-

comments
<!-- -->

Browser
Possui rendering engine, networking, storage e Java Script Engine
Todo navegador possui esses softwares/funcionalidade.
O Chrome possui o [blink](https://www.chromium.org/blink/) como motor de renderização
O mozzilaFirefox usa gekko

A tag `<pre></pre>` mantem todos os espaços e quebras de linhas do texto dentro delas.

You should use htmlspecialchars. It replaces characters as below:

## Simbolos de tag no texto
[Tabela de simbolos](https://html.spec.whatwg.org/#named-character-references)
& (ampersand) becomes &amp;
" (double quote) becomes &quot; when ENT_NOQUOTES is not set.
' (single quote) becomes &#039; only when ENT_QUOTES is set.
< (less than) becomes &lt;
> (greater than) becomes &gt;

Um container é um elemento que possuí outros elementos dentro dele

## Ancoras
id
class
tags

## Forms
get colocar os dados na url e post coloca os dados internamente
label "for" é vinculado ao input "id"

## DOM
Document Object Model - Um documento que representa o HTML, provendo a habilidade de examinar ou alterar o documento.

O dom são objetos gravados na memória do computador que podem ser utilizados de várias maneiras, desde criar uma representação gráfica para visualização do usuário, até a criação dos elementos em developers tools, onde o dom é convertido em uma estrutura similar ao html facilitando a edição e visualização do DOM.
Porém, o DOM pode ser utilizado não apenas para mostrar algo visual, mas também mostrar algo de outra maneira, como leitores de telas que narram/descrevem o site conforme passam pelo DOM.


## Links

### Estudados

### Estudar
[HTML Spec](https://html.spec.whatwg.org/)
[estrutura de árvore](https://github.com/yzhong52/ascii_tree)
[Leitor de tela do Windows](https://www.nvaccess.org/download/)
[Tags e atributos para acessibilidade](https://www.w3.org/TR/html-aria/)

tag script defer o que faz?