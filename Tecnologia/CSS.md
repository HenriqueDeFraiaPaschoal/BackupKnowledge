# CSS
## O que é CSS?
O [CSS](https://pt.wikipedia.org/wiki/Cascading_Style_Sheets), cascading style sheet ou folha de estilo em cascata, é um mecanismo para adicionar estilos à uma página html.
- **Cascading**: Cascata, pois processa vários css's e resolve os conflitos "cascatando" entre os arquivos .css
- **Style**: Estilo, pois adiciona estilos aos elementos selecionados com os atributos especificados
- **Sheet**: Folha, pois é um arquivo/folha com as especifícações documentadas

Como um elemnto HTML possui vários documentos de estilo, do autor do site, dos padrões do navegador, das preferências do usuário, conflitos ocorrem, estilos se sobrepõem e o método cascata foi a solução encontrada.
O navegador passa pelos arquivos de estilo criando um único arquivo final com as características e atributos calculados levando em consideração suas prioridades.Este arquivo final é o CSSOM, CSS Object Model.

Apesar de estilo poder ser feito no próprio html adicionando o atributo style="position: relative; color='red'; etc" não é considerado boa prática. O correto é separar o style em um arquivo.css separado e linkado ao html/componente por uma tag link:css.

A sintaxe do CSS segue da seguinte maneira:
selecionador {
  chave: valor;
  chave: valor;
}

Onde um selecionador pode possuir vários atributos/regras(chave: valor)
**/* Comentários no css ficam entre barra asterisco */**

## Seletores
tagHTML
Os seletores são lidos da direita para esquerda:  
Ex. ul li -> ele busca todos li primeiro e depois vê quais são filhos de ul (ver otimização em css)(isso: ul * é mais pesado do que *)
* : universal

.class: seletor por classe
  - Adicionando o atributo e valor no html como class="valor1 valor2 outro-valor"

#id: seletor por id
  - Adicionando o atributo e valor no html como id="nomeId"

tag: seletor por tag
  - buscando vários elementos ou um elemento que segue uma estrutura específica na "árvore"
  Ex1. li -> busca elementos com tag li
  Ex2. ul li -> busca li descendentes diretos ou indiretos de ul

Grouping selectors
*.class
p#class
.classe1, #id1 -> para ambos
ul p -> p descendentes de uma ul
ul > p -> p deve ser um filho direto de ul
p + li -> irmão diretamente seguinte de p, 
p ~ li -> qualquer irmão seguinte de p, não apenas o seguinte
li:nth-child(Xn + b) -> onde x é o intervalo dos grupos e b qual número do grupo será aplicado
  - (2n+1) ou (odd): ímpar
  - (2n+2) ou (even): par
ul li:nth-of-type(odd) -> busca os filhos de um tipo específico

:visited
:active
:focus
:hover
:not(): section:not(#id)
::first-letter
:is(ul, ol) li -> todos li descendentes de ul e ol

com atributos
seletor[atributo] -> qualquer que tenha o atributo
seletor[atributo=valor] -> atributo com exatamente este valor
seletor[atributo~=valor] -> atributo que possui o valor

[Resolvendo conflitos da cascata](https://drafts.csswg.org/css-cascade-4/#cascading)
1. Importância
  1.Important user agent declarations
  2.Important author declarations Ex. color: white !important;
  3.Normal author declarations
  4.Normal user agent declarations

2. specif
  id 100
  class 010
  tag 001

3. Ordem de chamada
  Ganha o ultimo lido

@import 
@layer
@import x layer y

## Render
Para o render há as coordenadas da tela, do conteúdo, do conteúdo dentro do conteúdo, etc.
1px em css = 1/96 inch

como é chegado no valor final:
declared values - > cascading
cascaded value -> defaulting(initial/inheritance)
specified value -> resolving
computed value -> calculating
used value -> final layout adjustments
actual value

### box model
content: onde estara o conteudo
padding: space bettwen the content and the border
border: 
margin: space betwen it and other boxes, they can overlap other margins

## Mathematical expressions
calc(800px - 2rem) -> calcula o valor dado a expressão entre parenteses
min(700px, 80%, 30rem) -> pega o menor dos valores separados por virgula
max(700px, 80%, 30rem) -> pega o maior dos valores separados por virgula
clamp(700px, 90%, 900px) -> clamp(min, valor, max)

## Position
Todo elemento inicialmente possui seu positon: static.

position: relative -> o elemento é tratado como se estivesse me sua posição original, mas pode ser offset/tirado da posição não afetando os outros elementos(relative to its origin)
offset com top: ou left: ou bottom: ou right:

position: absolute -> É posicionado relativamente ao ancestral mais próximo que possua posição não static, se não houver um, será relativo ao bloco da tag html. Ele também não afeta a formatação dos outros elementos. é considerado como se ele não existisse
position: absolute;

position: fixed -> É posicionado relativamente à tela. Ele não afeta a formatação dos outros elementos.

position: sticky -> É posicionado relativamente ao acestral mais próximo com scroll ao passar o scroll, se não houver, será da tela. Ele gruda na tela quando iria sair dela. Ele afeta a formatação dos outros elementos.

right: 0;
top: 0;

## Flex Box
Flex já é baseado na direção de leitura. Logo, possui suporte para variação de direção para cada língua.
display: flex;
justify-content
align-items

flex-direction: row / column / row-reverse / column-reverse

order:
flexwrap
overflow
flexgrow
flexshrink
flex: 1 0 auto;
align-self:
display: inline-flex

## Grid
display:grid;
grid-template-columns: 1fr 1fr 1fr 1fr;//ou repeat(4, 1fr) // Poderia ser px ou outra unidade, pode dar nome as linhas com min-max(100px, 1fr)[start-linha fim-linha]
grid-template-rows: 1fr 1fr;
grid-template: repeat(2, 1fr) / repeat(4, 1fr); // seria rows e columns em sequência
row-gap ou column-gap ou grid-gap: 10px // Dá um espaçamento entre as linhas
grid-auto-rows: 150px // Define o tamanho das linhas criadas automaticamente se necessárias
grid-auto-flow: column // Se precisar criar mais areas, criara mais colunas, por padrão é row

ou separar por áreas
grid-template-areas:"a1 a2 a3" "b1 b2 b3";//Criando uma grid com 2 linhas e 3 colunas


grid-row-start: 1
grid-row-end: 1
grid-row: start / end (ou 1 / span 2)// pode definir que vai ocupar quantos espaços
grid-column-start: 1
grid-column-end: 2
grid-column: start / end
grid-area: gridrowstart / rowend / columnstart / columnend // Ou colocar o nome da área se for utilizado o grid-template-areas

align-items
justify-items
align-content
justify-content



## Performance
inpect, performance, record button refresh stop -> mostra o tempo de cada processo

## Painting
visibility: hidden -> não é "pintado" mas é considerado na formatação dos outros elementos
z-index -> quando maior for o número, maior a chance de ser pintado depois/por cima.
Ex. um elemento z-index:4 sobrepõe um elemento de z-index:3

Caso o z-index for igual, fica por cima o ultimo elemento na árvore do DOM

isolation: isolate -> pesquisar

display: none; -> não é renderizado e o elemento não afeta outros elementos

dúvidas? procure por stacking context html

## Thinking Multlingual
inline direction e block direction podem mudar de língua para língua, utilizando o atributo writing-mode: e direction: e text-orientation:

usar atributos que levam em consideração inline e block directions
Exemplos:
padding-inline: 2rem; -> padding left e right
padding-block: 2rem; -> padding top e bottom
inset-line-start -> top
margin-inline left right
margin-inline-start
margin-inline-end
margin-block
width = inline-size
height = block-size

## Content
text-align:
display: flex;
display: grid;

## Padrão CSS
/*
Aqui ficará o padrão de css utilizado pelo autor para a produção de seus projetos pessoais.
Lembrar de usar um minifier para criar um CSS de uma linha, diminuindo o arquivo e facilitando o download
on root because custom properties are inherited and all css can use it, if declared inside other statement, it can't be acessed by no-children
margin-inline left right
margin-inline-start
margin-inline-end
margin-block
width = inline-size
height = block-size
*/
:root {
  --white: #ffffff;
}

body {
  margin-inline: 0;
  margin-block: 0;
}

* {
  box-sizing: border-box;
}

body {
  margin: 0;
  padding: 0;
  font-size: 100%;
  font: inherit;
}

## Pesquisar por
vh vw dvh dvw svh svw

var (--variável, default)

configurações de css para impressão

[imagens](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images)

overflow:
vertical-align:
text-align:

Herança -> elementos podem herdar algumas caracteristicas dos pais
flow-root -> pode ajudar a consertar problemas com float, em caso de legados

background-image
background-size

transition:

@media screen and (max-width: 800px)

animation
@keyframe
from
to

SVG
color:
fill:

Atributo media no link css ex. media="print" ou "screen" "all"
ou @import "file.css" print; //omitido é all
ou @media print { css rules }

## Links
### Estudados

### Estudar
[CSS Spec](https://www.w3.org/Style/CSS/)
[Google Chrome Style Guide](https://google.github.io/styleguide/htmlcssguide.html)
[chromium blink standard CSS](https://chromium.googlesource.com/chromium/blink/+/72fef91ac1ef679207f51def8133b336a6f6588f/Source/core/css/html.css?autodive=0%2F%2F%2F)
[Verificar funções implementadas por navegador](https://caniuse.com/)
[mozzila developer network](https://developer.mozilla.org/pt-BR/)
[W3C Draft](https://drafts.csswg.org/)
[phd thesis](https://www.wiumlie.no/2006/phd/)
[animate.css](https://animate.style/)
[CSS Validator](https://validator.w3.org/)