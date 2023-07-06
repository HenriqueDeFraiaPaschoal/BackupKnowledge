# Markdown

Markdown é uma linguagem de marcação de texto leve e simples criada em 2004 por [John Gruber](https://daringfireball.net/projects/markdown/ "Site do criador do Markdown").`<br>`
Os arquivos com extensão .md ou .markdown podem ser lidos em quase qualquer sistema podendo sua versão variar pouco entre sistemas.`<br>`
Devido sua compatibilidade e simplicidade, muitos textos de produtos, listas e documentos são estruturados com essa sintaxe.

<details>
  <summary>
    Adendo
  </summary>

  Este é um documento de anotação de [Henrique Paschoal](https://www.linkedin.com/in/henrique-de-fraia-paschoal-113b4111a/ "Linkedin Henrique Paschoal") com intuito de facilitar uma revisão e agrupar referências para o autor e visitantes.`<br>`
  Sendo assim, o material é variável à visão do autor e sucinto.`<br>`
  É aconselhável buscar em referências cursos ou sites caso busque por instruções ou descrições detalhados.

</details>

## MARKDOWN ADICIONADO DE HTML

O principal uso do autor se da na plataforma GitHub, logo, considerando a compatibilidade do GitHub com marcações HTML, além de ser comparado as sintaxes, será adicionado marcações HTML úteis na criação de README's e documentos de texto no GitHub.

!! Lembrete: Nem todos sistemas aceitam HTML com markdown e markdown aninhados ou em linhas adjacentes à tags HTML pode não funcionar. Pular linha entre tags HTML e markdown.

> `<h1>Titulo<h1><br>``<br>## Subtitulo`

<details>
  <summary>

### TÍTULOS

</summary>

  Sempre deixar o espaço de uma linha separando titulos.`<br>`
  Titulos possuem níveis de 1 a 6 sendo 1 o maior e mais importante diminuindo em tamanho e importância nos ## `<h2>f`,### `<h3>`,...

  Os ID's nos títulos não funcionam 100% no github (utilizar h1,h2,h3... com id="" e linkar normalmente com markdown `[texto](#nomeID)`)

|                  Markdown                  |         HTML         |     Representação     |
| :----------------------------------------: | :------------------: | :----------------------: |
| # Título`<br><br>`Título`<br>`===== | `<h1>Título</h1>` | `<h1>`Título`</h1>` |
| ## Título`<br><br>`Título`<br>`----- | `<h2>Título</h2>` | `<h2>`Título`</h2>` |
|                ### Título                | `<h3>Título</h3>` | `<h3>`Título`</h3>` |
|                #### Título                | `<h4>Título</h4>` | `<h4>`Título`</h4>` |
|              ##### Título´              | `<h5>Título</h5>` | `<h5>`Título`</h5>` |
|               ###### Título               | `<h6>Título</h6>` | `<h6>`Título`</h6>` |

</details>

<details>
  <summary>

### PARÁGRAFOS E QUEBRA DE LINHA

</summary>

  Parágrafos podem ser separados por linhas em branco.`<br>`
  Não identar parágrafos que não estejam em uma lista.

| Markdown | HTML | Representação |
| :---: | :------: | :----------: |
| Ficou alguma dǘvida?`<br><br>`Olhe as referências! | `<p>Ficou com alguma dúvida?</p><br>``<br><p>Olhe as referências!</p>` | `<p>`Ficou com alguma dúvida?`</p><br>``<p>`Olhe as referências!`</p>` |

  Quebras de linhas podem ser feitas deixando 2 ou mais espaços em branco no final da linha ou com a tag HTML `<br>`.`<br>`
  Recomendo usar a tag quando possível devido a facilidade de visualização no código e há diferença de espaçamento entre as duas opções.

</details>

<details>
  <summary>

### ITÁLICO, NEGRITO, TACHADA, SUBLINHADO, SOBRE/SUBSCRITO

</summary>

  Lembrando que as tags `<strong>` e `<em>` podem possuir os efeitos que negrito e itálico mas possuem semântica diferente das tags `<b>` e `<i>`.`<br>`
  Sendo palavras em negrito entre dois asteriscos/sublinhados e itálico entre um asterisco/sublinhado.`<br>`
  Negrito e itálico são três.

  !! O uso do sublinhado não é recomendado devido imcompatibilidades.

| Markdown                                         | HTML                                                          | Representação                                             |
| :----------------------------------------------- | :------------------------------------------------------------ | :---------------------------------------------------------- |
| Este `**texto**` está em negrito              | Este `<b>`texto `</b>` está em negrito                   | Este`<b>`texto`</b>` está em negrito                   |
| Este `*texto*` está em itálico               | Este `<i>`texto `</i>` está em itálico                  | Este`<i>`texto`</i>` está em itálico                  |
| Este `***texto***` está em negrito e itálico | Este `<b><i>`texto `</i></b>` está em negrito e itálico | Este`<b><i>`texto`</i></b>` está em negrito e itálico |
| `Este ~~texto~~ está tachado`                 | `Este <s>texto</s> está tachado`                           | Este`<s>`texto`</s>` está tachado                      |
| Não encontrado                                  | Este `<ins>texto</ins>` está sublinhado                    | Este`<ins>`texto`</ins>` está sublinhado               |
| x `^2^`                                        | x `<sup>2</sup>`                                            | x`<sup>`2`</sup>`                                       |
| H `~2~`O                                       | H `<sub>2</sub>`O                                           | H`<sub>`2`</sub>`O                                      |

</details>

<details>
  <summary>

### CITAÇÕES EM BLOCO

</summary>

  Pode ser utilizado o sinal de >

  `> Mantenha o sinal durante a quebra de linha para manter a citação<br>`
  `><br>`
  `> Como neste exemplo.<br>`
  `>> Pode haver uma citação dentro de outra!<br>`
  `>> Ou outros elementos como:<br>`
  `>> - Listas<br>`
  `>> - *Palavras em itálico e **negrito**`

> Mantenha o sinal durante a quebra de linha para manter a citação
>
> Como neste exemplo.
>
>> Pode haver uma citação dentro de outra!
>> Ou outros elementos como:
>>
>> - Listas
>> - `<i>`Palavras em itálico e `<b>`negrito`</b></i>`
>>

</details>

<details>
  <summary>

### LISTAS

</summary>

  Aninhados é adicionado identação.

#### Ordenada

  Marcado por número e ponto final nas ordenadas. 1.`<br>`
  Pode ser utilizado ( ) mas não é recomendado. 1)`<br>`
  A lista deve começar com 1 mas o restante dos números não faz diferença.

#### Não ordenada

  Marcado por - ou * ou + nas não ordenadas. - Olá`<br>`
  Se começar com número e . é adicionado uma barra invertida.

  `- 1995\. O autor nasceu! `

| Markdown                                                                                                                                                                                                   | HTML                                                                                                                                                                                                                                                                                                                                                                                                | Representação                                                                                                                                                                                                                                                                |
| :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `<pre>`1. Primeiro`<br>`2. Segundo`<br>`8. Terceiro`<br>` 1. Identado`<br>`4. Quarto`<br>`- E não ordenada`<br>`  + Assim identado`<br>`+ Assim não identado`<br>`* Ou assim`</pre>` | `<pre><ol>``<br>  <li>Primeiro</li>``<br>  <li>Segundo</li>``<br>  <li>Terceiro</li>``<br>  <ol>``<br>    <li>Identado</li>``<br>  </ol>``<br>  <li>Quarto</li>``<br></ol>``<br><ul>``<br>  <li>E não ordenada</li>``<br>  <ul>``<br>    <li>Assim identado</li>``<br>  </ul>``<br>  <li>Assim não identado</li>``<br>  <li>Ou assim</li>``<br></ul>``</pre>` | `<ol><li>`Primeiro`</li><li>`Segundo`</li><li>`Terceiro`</li><ol>``<li>`Identado`</li></ol>``<li>`Quarto`</li></ol>``<ul><li>`E não ordenada`</li><ul>``<li>`Assim identado`</li></ul>``<li>`Assim não identado`</li><li>`Ou assim`</li></ul>` |

</details>

<details>
  <summary>

### LINKS E IMAGENS

</summary>

  Links e imagens seguem um padrão bem parecido.
  Pode ser feito imagens com links no MD.

  Sendo para links:

  `[texto como link](link 'descrição')<br>`
  `<a href="link" title="descrição">texto como link</a><br>`
  `<link>`

  Ex. [Henrique Paschoal](https://www.linkedin.com/in/henrique-de-fraia-paschoal-113b4111a/ "Linkedin Henrique Paschoal")

  Para imagens segue o mesmo exemplo adicionando ! na frente

  `![texto alternativo](link para a imagem 'Descrição')<br>`
  `<img href="link para imagem" alt="texto alternativo">`

  ![Henrique](./Fotos/Henrique.jpg "Foto de Henrique Paschoal")

  Para arquivos:
  `[texto como link](diretório ex: ./readme.md)`

</details>

<details>
  <summary>

### LINHA HORIZONTAL E TABELAS

</summary>

  Podem ser feitas com uma sequência de três -, * ou _
  Deixar quebras de linhas entre ela

---

  Barra gradiente?

>>>>>> `
>>>>>>
>>>>>
>>>>
>>>
>>

  `>>>>>>`\`

  Tabelas são separadas horizontalmente por | e quebra de linha e os alinhamentos definidos entre o titulo da coluna e a coluna.`<br>`
  As tabelas aceitam apenas texto, links, negrito e italico. Outros tipos não funcionam.

  `| Alinhado Esquerda | Alinhado Meio | Alinhado direita |<br>`
  `| :--- | :---: | ---: |<br>`
  `| dado1 | dado2 | dado3 |<br>`

| Alinhado Esquerda | Alinhado Meio | Alinhado direita |
| :---------------- | :-----------: | ---------------: |
| dado1             |     dado2     |            dado3 |

</details>

<details>
  <summary>

### TEXTO DE CÓDIGO E NOTAS DE RODAPÉ

</summary>

  Para criar um texto que deve ser interpretado/apresentado como texto, coloque entre crases.

  \`## Titulo - o sustenido não apareceria\`

  \` `<h2>Subtitulo - a tag h2 não apareceria</h2>` \`

  Para salvar a identação pode-se utilizar a tag: `<pre></pre>`

`[^qualquer-texto]: Exemplo do rodapé.`

Para criar uma nota apenas coloque o texto dentro de colchetes `[^qualquer-texto]` e no rodapé crie o link desejado.
  Notas de rodapé dentro de `<details>` tem sua referência jogada para o final do documento.

`[^qualquer-texto]: Exemplo do rodapé.`

  Dúvidas? Olhe a referência[^1]!

  Para criar um código com botão de cópia(testado no readme.md no github) use ``` ou ~~~ na linha anterior e posterior do código

```
  Isto é um código
```

  `~~~`
  Ìsto é um código
  `~~~`

</details>

<details>
  <summary>

### LISTA DE TAREFAS E EMOJIS

</summary>

  Para lista de tarefas é usado `- [ ]` e para emojis é usado `:palavraDoEmoji:` a lista de emoji pode ser encontrada nos links abaixo.

  `- [x] Lavar a louça<br>`

- [X] Lavar a louça`<br>`
  `- [ ] Enxugar a louça<br>`
- [ ] Enxugar a louça

  `:smile:<br>`
  😄

  Links com boas listas de emojis:`<br>`
  [Emoji Cheat Sheet GitHub](https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md)
  [Emojipedia](https://emojipedia.org/)

</details>

<details>
  <summary >

### DICAS GERAIS

</summary>

  Estas dicas podem ou não funcionar no sistema que está utilizando mas foram utilizadas neste documento.

  Criar uma separação de conteúdo minimizado

  `<details><br>`
  `<summary>`

  `### DICAS GERAIS`
  `</summary>`

  `Texto, links e o que quiser minimizado. Pode ser adicionado open <details open> caso deseje que comece maximizado`
  `</details>`

</details>

## Extensões
Office Viewer(Markdown Editor)

## Referências

[MARKDOWN GUIDE](https://www.markdownguide.org/ "Site guia sobre markdown")
Uma ótima referência para aprender MarkDown e possui um CheatSheet excelente!

[JOHN GRUBER](https://daringfireball.net/projects/markdown/ "Site do criador do Markdown") Visualmente não muito atrativo, mas ainda, uma ótima referência para se aprofundar sobre sua origem e licenças.

[READMES GITHUB](https://docs.github.com/pt/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/quickstart-for-writing-on-github) Para verificar a documentação do que é suportado etc.

[Readmes para inspiração](https://github.com/abhisheknaiidu/awesome-github-profile-readme)

[Gerador de README](https://readme.so/pt/editor)

[Gerador de Profile para GitHub](https://profile-readme-generator.com/)

[^1]: ]:[MARKDOWN GUIDE](https://www.markdownguide.org/ "Site guia sobre markdown")

