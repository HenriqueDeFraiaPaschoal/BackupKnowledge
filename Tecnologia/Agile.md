# Metodologia Ágil

É uma metodologia interativa e incremental. Focada em manter a qualidade e se adaptar às mudanças.

- *Adaptável*
- *Planejado em sub-produtos*
- *Sempre em contato com usuários e cliente*
- *Feedback rápido*

| Preferências da metodologia: | |
| ------ | ----- |
| **Essencial, preferível** | **Não preferível, mas não descartável** |
|indivíduos e insterações | processos e ferramentas |
| software funcionando | documentação compreensiva |
| colaboração do cliente | negociação por contrato |
| responder à mudança | seguir o plano |

Principais pontos implementados:
- Reuniões cara a cara
- entregas constantes
- suporte e confiança ao time - maior moral do time
- aceitar mudanças
- satisfazer o cliente
- colaborar com o cliente dia a dia
- mensurar progresso a cada produto funcional
- manter um ritmo de produção constante, entrega rápida
- manter excelência
- simplifique
- time auto-gerênciável
- melhoria constante
- visibilidade de projeto
- alinhamento entre colaboradores

Base levando como conceito Triangulo de Ferro:

- escopo é maleável
- custo e tempo é fixo

## Metódo cascata - método anteriormente utilizado

Um processo seguido de outro, apenas com uma entrega final.

O cliente passava os requerimentos, era analisado tudo, feito tudo, validado tudo, entregue tudo, para só então o cliente ver o produto e decidir, mudar algo, ou implementar o produto.

Base levando como conceito Triangulo de Ferro:

- escopo é fixo
- custo e tempo é maleável


## Scrum
É uma estrutura de trabalho que se enquadra em metodologia ágil.
Não há hierarquia no time, logo tudo é decidido pelo grupo e em grupo. Há muitas votações.
Seu processo segue um encadeamento de *sprints* (ciclos de produção), que possuem um objetivo e são seguidos até que o produto final seja entregue.
Sendo mudanças no produto feitas entre sprints e nunca durante sprints.

### Scrum Team:
Time multidisciplinar, sem hierárquia e auto gerenciável, preferêncialmente menos de 10 integrantes
Pode ter mais de um time, com mesmo Backlog e mesmo P.O.
- **Product Owner (P.O.)** - "Representante" do cliente, conhecedor do tema do produto, maximizador do valor do sub-produto entregue ao final e palavra final no Backlog
- **Scrum Master (S.M.)** - Especialista focado em manter e facilitar o trabalho ágil. Responsável por:  
  - Garantir que as reuniões serão feitas e serão eficazes
  - Manter o time focado e auto-organizado
  - Remover obstáculos e evitar contratempos
- **Developers (Devs)** - Membros do time que se planejam/adptam desenvolvendo o produto (não necessáriamente apenas desenvolvedores de software)
- **Stacke Holders** - São as partes interessadas(usuários, clientes, investidores,etc)

### Eventos
- **Sprint Planning** - Reunião de todo o time para definir os objetivos para a sprint (Sprint Backlog)  
  - Definem um Backlog da sprint, estima o tempo de cada user story, e os devs decidem o que será feito.
  - *Por quê* a sprint é importante? (User Stories)  
    *O que* somos capazes de fazer durante a sprint? (Estimativa de tempo/produção)  
    *Como* o trabalho será feito (To Do lists)?
- **daily** - Reunião cara a cara dos devs em qualquer lugar e rápida, menos de 15 minutos, discutir progresso, impedimentos e andamentos. *O que fiz ontem? O que farei hoje? Há algum obstáculo?*
- **Sprint Review** - Momento de apresentação do sub-produto da sprint recebendo feedbacks dos stakeholders/cliente que participam ativamente
- **Sprint Retrospective** - Reunião descontraida para discutir sobre o fluxo de trabalho  
  *O que deu certo?*  
  *O que deu errado?*  
  *O que pode ser melhorado?*

### Tarefas

- **Product Backlog** - Lista de objetivos ordenados por prioridade, <em>gerenciado pelo P.O</em>.
- **User Story** - O objetivo/funcionalidade do produto. Parte do que será implementado
  Ex. As a [user/role], i want [functionality/action], so that [goals/benefits]  
  Ex. Given [precondition], when [trigger event], then [expected results]
- **Sprint** - Ciclo de um mês ou menos, duração do ciclo de um sub-produto
- **Planning Poker** - Estimar coletivamente o esforço necessário para cada objetivo da sprint, onde cada dev vota com um valor a cada user story  
  Ex. 0, 1/2, 1, 2, 3, 5, 8, 13, 20, 40, 100, infinito (muito esforço), ? (user story não claro)  
  Se os valores variam muito, é perguntado e re-analisado o user story, senão é dado o valor votado  
  No final da sprint é analisado os pontos da sprint e quantos foram concluídos para definir a "potência" do time 
- **Story Point** - Unidade de medida para estimar o esforço necessário para um objetivo/sub-produto
- **Kanban** - Um outro método/ferramenta utilizada para visualizar e facilitar a implementação de metodologias ágeis
- **Burn Down Chart** - gráfico de trabalho necessário VS tempo para finalizar uma sprint 

## Kanban
[Kaban](https://pt.wikipedia.org/wiki/Kanban) é uma ferramenta de trabalho que pode auxiliar na visualização e gerênciamento de tarefas.  
Principais características:
- Representação gráfica do desenvolvimento
- Facilidade em medir e gerênciar progresso
- Aberturas para melhorias constantes

O Kanban por ser uma ferramenta auxiliar da produção, pode ser utilizado em várias áreas. Cada área pode possuir separações e classificações de tarefas diferentes, específicas da área. 
O mais comum junto a um exemplo pode ser visto abaixo:  
| Criadas | Em Andamento | Bloqueada | Finalizada |
| ----- | ----- | ----- | ----- |
| Lavar roupa<br><br>Lavar carro<br><br>Passear cachorros | Varrer sala[Henrique] | Lavar louça(acabou detergente) | Passar pano cozinha |

Isso facilita o time a verificar o que está sendo feito, quem precisa de ajuda e qual o andamento total do projeto. Além de que a visualização do andamento do projeto pode ajudar na moral do time.

Algumas das ferramentas mais utilizadas baseadas nesse conceito são:
- [Trello](https://trello.com/pt-BR)
- [Monday](https://monday.com/lang/pt)
- [Jira](https://www.atlassian.com/br/software/jira)

Elas possuem várias outras utilidades como:
- E-mails avisando sobre mudanças
- Pessoas designadas para cada tarefas
- Gráficos e tabelas
- Cores e etiquetas
- Datas e checklists na tarefa
- Entre várias outras

## Scrumban
Na área de tecnologia o mais usual é a combinação de Scrum e Kanban. Separando os pedidos em sprints e seguindo a estruturação do time em Scrum, porém visualizando as tarefas e o progresso com o uso de ferramentas baseadas em Kanban.

## Minha visão

### O que é o Scrum?
É uma abordagem de sub-dividir objetivos grandes em objetivos pequenos e fáceis de conquistar, analisando brevemente o todo a cada conquista e planejando profundamente o próximo sub-objetivo considerando as mudanças necessárias.

### O que é Kanban?
É uma ferramenta muito poderosa para facilitar a visualização e o gerênciamento da produção. 

### Conclusão do autor e dicas
- Reuniões cara-a-cara e em pé podem agilizar e tornar reuniões mais eficazes

O conhecimento dos métodos e ferramentas auxiliam a melhoria e o gerênciamento, porém o foco exagerado neles, sem o aprofundamento no negócio/mercado/empresa, pode ocasionar em organizações caóticas.

<em><strong>O SEGREDO ESTÁ EM ADAPTAR, O QUE CONDIZ E QUANDO CONDIZ, A NECESSIDADE DA EMPRESA</em></strong>


## Exemplo
Desenvolvimento de site de um jogo.

Scrum Team 6 membros
- Gerente do produto
- 1 senior, 1 pleno e 3 juniores(J1, J2 e J3)
- O pleno fará o papel de S.M.

Clientes
- Gerentes
- Usuários
- Patrocinadores
- Sócios

1. Time decide: fazer sprints de 2 semanas e dailys pelo zoom as 13:00 
2. É definido o Product Backlog pelo P.O.  
  - User Story 1: Como um [usuário] eu gostaria de [pesquisar tópicos] para [encontrar as descrições do jogo mais fácil] *5 pontos*
  - User Story 2: Como um [usuário] eu gostaria de [ter uma lista de favoritos] para [marcar posts/novidades do jogo] *10 pontos*
  - User Story 3:Como um [produtor de eventos] eu gostaria de [ter um contato e lista de serviços da empresa] para [que eu possa personalizar ou adicionar produtos únicos pra meus eventos] *20 pontos*  
  - ...
3. É estimado pelo P.O. junto ao time poucos itens do Backlog para referência e suficientes para a sprint

- Início da Sprint 1
4. O P.O. passa os itens da sprint e o time decide se é aceito aqueles itens para aquela sprint: User Story 1, 2 e 3
5. O time cria um plano de trabalho, lista de tarefas com cada tempo (usando um trello)  
  -Criação dos cards 2h  
  -Link com banco de dados de descrição do jogo 1h  
  -Caixa de pesquisa 2h  
  -Criação do formulário de cadastro 2h  
  -Aba de login 1h  
  -Lista de favoritos 2h  
  -Estilização dos componentes 3h  
  -...
6. Na daily 4 o J2 comunicou dificuldades em implantar o sistema de login, o J3 decidiu ajuda-lo após a daily
7. No final da primeira semana é feito um refinamento na Sprint Backlog com o P.O. usando o Planning Poker: User Story 3 *10 pontos* e User Story 2 *5 pontos*
8. E marcado a sprint review e sprint retrospective
9. É apresentado o produto feito na sprint no sprint review, recebendo os feedbacks e fazendo mudanças no Product Backlog. Entregue apenas os User Story 1 e 2´
10. Na sprint retrospective é decidido quais foram os obstáculos, o que poderia ser melhorado para as próximas sprints: ter uma documentação da API de descrição do jogo, a falta de experiência da equipe dificultou o processo mas a experiência adquirida na primeira sprint servirá para as demais sprints

Início Sprint 2:  
...

## Referências

[Agile Manifesto](http://agilemanifesto.org/iso/en/manifesto.html)
