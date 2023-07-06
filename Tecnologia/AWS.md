# AWS

[AWS](https://aws.amazon.com/pt/) ou Amazon Web Service é um conjunto de serviços computacionais online, altamente escalável e incremental. Onde é possível "alugar" esses serviços conforme a demanda, pagando apenas pelo necessário/utilizado.  
Suas principais características:
- Flexível
- Adaptável
- Escalável
- Seguro
- On demand delivery (entrega por demanda)
- Pay-as-you-go (pague o que usar)
- Acesso global com menor delay
- go global easily (liberdade global fácil)
- Integração entre funcionalidades AWS

Com isso uma empresa, a qual o foco não é criar e gerenciar um sistema computacional, pode tercerizar esse serviço para uma empresa confiável e responsável.  
Permitindo que a empresa foque no que ela realmente precisa e que seu publico demanda.
O custo de criação, reparação e ampliação computacional, também será reduzido devido à especialização da AWS na área e a diluição de custos fixos entre os milhares ou até milhões de clientes.  

## Como AWS funciona e quais são as outras opções?

Em uma visão simplificada, AWS é: vários computadores/componentes ligados e integrados entre si, que podem ser "alugados" pelo tempo/valor definido pelo cliente.  
Precisa de RAM e processamento para manipular dados? É só pedir!  
Precisa de armazenamento e que seja acessível globalmente? É só pedir!  
Tudo isso fornecido por uma empresa 100% dedicada à essa funcionalidade.

As outras opções são:
Servidor dedicado
- Servidor físico utilizado por apenas um cliente
- Precisa "chutar" a capacidade necessário futura
- Equipamento não utilizado foi/está sendo pago
- Escalomanento possui custo e tempo elevados
- Substituir o servidor é extremamente complicado
- Possui segurança e privacidade elevada

VMs (Virtual Machines) Ex. Hypervisor
- Vários servidores em um mesmo sistema
- Um servidor físico distribuido para vários clientes
- Paga por uma fração do servidor
- Paga mesmo sem utilizar o servidor
- Limitado pela capacidade máxima da empresa do servidor
- É possível ter várias aplicações atendidas
- Fácil importação e exportação

Containers Ex. Docker Deamon
- Mais flexível
- Vários aplicações funcionando na mesma VM
- 

Funções
- 
- 

Não entendeu? Veja o exemplo abaixo:
### Exemplo
<detail>
  Para facilitar a visualização, vamos tentar torna esse processo digital em uma situação física.  
  Vamos ver a história de dois empreendedores. Jorginho dono de uma lan-house e dona Maria, dona de um Cyber-café.

  O sonho de dona Maria era ter uma cafeteria, e ela alugou um comércio em frente um cartório. Todo dia dona Maria via seus clientes correndo do estabelecimento indo atrás de uma copiadora ou lan-house para copiar documentos ou iimprimir boletos. Com isso dona Maria comprou 4 computadores para atender essa demanda.

  Já Jorginho, possui 20 computadores para atender as jogatinas dos alunos da faculdade ao lado.

  Ambos estabelecimentos estão à uma casa de distância um do outro.

  Porém, os computadores de Jorginho e Maria são caros, cerca de R$2.000,00 cada.
  A lan-house tem sua ocupação ideal durante a noite, quando os alunos chegam e saem da faculdade. Já a cafeteria tem seu funcionamento de manhã e a tarde.
  Durante o dia os computadores da lan-house ficam criando poeira, sem uso. E durante a noite os computadores da cafeteria fazem o mesmo.  
  Além de que a manutenção dessas máquinas é trabalhosa para dona Maria e para Jorginho, que gostariam mais de focar em seus negócios que é criar eventos/competições e servir café e rosquinhas.

  É ai que AWS entra!
  Imagine que naquela casa entre os dois o mercadinho de AWS se instalou. E que ao invés de terem comprado seus computadores de R$2.000,00 cada, dona Maria e Jorginho alugam eles da AWS. Primeiro que não seriam necessários 25 computadores, apenas 20 atenderiam a demanda pois durante o funcionamento da cafeteria a lan-house não possui muitos clientes.  
  No comércio de AWS eles possuem profissionais especializados em fazer a manutenção das máquinas e atualiza-las, deixando os computadores prontos e melhor preparados para o dia-a-dia.
  Com isso, Jorginho pode focar mais nos eventos da lan-house e promoções e dona Maria em seu café e rosquinhas.  

  Isso causa um melhor aproveitamento do equipamento que será utilizado o dia inteiro, além de diluir o custo de manutenção e compra entre todos os clientes do AWS. Tornando a "posse" do poder computacional mais barato e acessível.

  Além desse problema, AWS também está para solucionar outro problema. Outras 5 empresas próximas dali alugam computadores também, com isso o mercadinho do AWS possui agora 50 computadores.  
  Ao mesmo tempo, Jorginho decide fazer um mega-evento, uma competição de LoL e Fortnite. Com isso ele espera chega à 50 jogadores em uma única noite!
  A situação inicial Jorginho teria que comprar mais 30 computadores desembolsando R$60.000,00! Se o evento não "bombar" como ele espera, esses computadores ficariam parados sem trazer lucro algum!

  Agora, com o aluguel do AWS, Jorginho pode pedir o aluguel de 30 máquinas para os dias específicos dos eventos e pagar apenas pelo que usar! Caso o evento não "bombe" Jorginho terá gasto apenas a "diária" das máquinas, e caso "bombe" mais do que esperava, o mercadinho do AWS possui mais máquinas prontas para a demanda!

  Isso diminui o custo de novas implantações e os riscos de mudanças.

  Voltand´o a realidade e saindo dessa situação ficticia, o AWS faz os mesmo papel mas online.
  Graças ao AWS as empresas não precisam ter e gerênciar servidores e computadores, elas podem focar no que realmente importa que é seu produto final(evento, café e rosquinhas :smile:)
</detail>

## Responsabilidades
AWS cuida da estrutura de hardware e segurança **da** rede.  
O cliente cuida da segurança **na** rede.  
Ex. AWS cuida da manutenção dos hardwares, softwares e ferramentas necessárias para manter o servidor/rede funcionando em perfeito estado. Já o cliente cuida da segurança na rede no seu lado de acesso, atualizando sistemas da AWS, de segurança e ferramentas que utiliza conforme o plano selecionado.

Com isso, há mudanças na responsabilidade dos funcionários internos da compania, por exemplo, a infraestrutura que era de responsabilidade do System Administrator, passa a ser da AWS, e este funcionário pode ser designado à uma função que trará inovações ou desenvolvimento da empresa, e não manutenção de um bem apenas necessário para empresa.

## Papéis em um sistema de tecnologia

IT Solutions Architect - responsável por criar soluções de alto nível para aplicações, sistemas, portifólios ou para toda empresa. Desenvolve soluções e gerência comunicação, segurança e armazenamento de dados.

System Administrator - Responsável pelo sistema físico. Hardware, backups, upgrade de hardware. Mantem o sistema operacional e atualizado para os objetivos da empresa.

Network Administrator - Responsável pela segurança, configurações de acesso interna, configurações e VPNs.

Desktop Administrator - Instala e da manutenção nos softwares dos computadores internos, usando a rede de trabalho.

Applications Administrator - Trabalha com o system e Network administrator. Gerencia aplicativos hospedados no servidor para uso.

Database Administrator - Trabalho com o System e Network, para gerenciar database e acesso aos dados.

## Papéis do AWS na empresa:
Cloud Architect - Desenvolve e gerencia o melhor plano e o implantação na nuvem/cloud AWS
Competências: Entender como os serviços são conectados, a integração deles, Amazon CloudWatch e login, AWS Identity e Acess Management(IAM) e segurança.
- Entendedor da empresa e sua necessidade
- Entendedor das funcionalidades que AWS pode trazer

System Administrator - Responsável pela performace do sistema da nuvem. Faz as melhores configurações para que o sistema tenha a melhor compatibilidade e velocidade, ajudando os outros papéis na configuração com a nuvem.
Competências: Proficiente em executar as tarefas de configurações, requisições e tradução para implantação.
- Especialista em AWS
- Gerenciamento de configurações e mudanças

Security Administrator - Responsável pela segurança **na** nuvem. Define as regras de segurança baseado nas normas e regulamentações sobre os dados, desde acesso à confidencialidade dos dados.
- Não especialista em AWS
- Entende as regulamentações sobre privacidade de dados
- Especialista na segunça
- Determina as normas de segurança conforme contratos e passa instruções para os funcionários
 
DevOps Administrator - Gerencia as releases/lançamentos e a escalabilidade nas ampliações/funções do sistema da empresa. Responsável por voltar releases problemáticas e 
Competências: bom com scripts de programação, operações e gerências dos desenvolvedores, Q.A(quality Assurance), testing
resumo: Gerencia os estágios de produção -> lançamento
- gerencia os devs

## Planos
Cloud-based Deployment - tudo é migrado para a nuvem. Softwares, ferramentas, dados, etc. Tudo é feito na nuvem
On-Premises deployment - Tudo é feito no local da empresa. Aumenta o custo.
Hybrid Deployment - Parte é migrado para nuvem e parte é deixado local. Usado em situações onde certas informações devem ficar em local por regulamentações ou quando a gerência de certos dados são melhor tratados ou necessários localmente.


### Siglas
Infrastructure as a Service (IaaS): Oferece serviços de estrutura, como computação, armazenamento, rede e virtualização, tudo pela nuvem,Amazon Elastic Compute Cloud (EC2),Google Compute Engine, etc.
Platform as a Service (PaaS): Oferece plataformas de trabalho onde pode ser utilizado hardwares e softwares para desenvolvimento de aplicações, Azure WebApps, AWS Elastic Beanstalk, etc.
Software as a Service (SaaS): Oferece serviços de software que podem ser acessados online, zoom, discord, google apps, etc.


Amazon EC2: Amazon Elastic Compute Cloud
Amazon S3: Amazon Simple Storage Service

Compute Services:
- Amazon EC2: Resizable comput capacity
- Amazon EC2 Auto Scaling: Increase or decrease number of instances
- Elastic Load Balancing: Distribute incoming traffic
- Amazon Elastic Container Service: Run applications on a managed Cluster
- Amazon Elastic Kubernetes Service: Run kubernetes applications on AWS and on-premises
- AWS Lambda: Run code in response to events, serverless

Store Services:
- Amazon Elastic Block Store: Persistent block-level storage
- Amazon S3: Durable, scalable object storage
> Standard: Active data
> Standard Infrequent Acess: Infrequent acess
> One Zone-Infrequent Acess: Rarely used
> Glacier storage Classes: Archived data
- Amazon S3 Glacier: Data archiving and backup
- AWS Storage Gateway: Integrate Cloud storage with on-site workloads
- Amazon Elastic File System: File storage for Amazon EC2 Instances
- Amazon FSx: File storage for widely-used file systems

Data Base Services:
Data base em EC2 ou Data Base Services?
Em database services você tem backup automatico, criação e manutenção rápida, escalamento.
Em EC2 se tem mais controle e mais flexibilidade e necessita de aplicações espefíficas
- Amazon RDS: cost-efficient and resizable capacity
- Amazon DynamoDB: Fast and predictable performance
- Amazon ElastiCache: Fast, managed information retrieval

Networking Services
- Amazon VPC(Virtual Private Cloud): build a virtual network in the cloud
- Security Groups: Control access to instances
- Network Access Control Lists(NACL): Control access to subnets
- Amazon Route 53: Route end users to internet applications

Tópicos de Serviços de Segurança:
- Data Protection
- Detection
- Identity & access management (IAM)
- Infrastructure Protection
- Incident Response
- Compliance




AWS management interfaces
AWS users can create and manage resources on the platform in three ways. All three options are built on a common, REST-like application programming interface (API) that serves as the foundation of AWS. 

The AWS Management Console provides a rich graphical interface to a majority of the features offered by AWS. It facilitates cloud management for all aspects of a customer’s AWS account, including monitoring their monthly spending by service, managing security credentials, or even setting up new IAM users.

The AWS Command Line Interface (AWS CLI) provides a suite of utilities that can be launched from a command program in Linux, Mac, or Windows. The CLI is an open source tool that provides commands for interacting with AWS services.

AWS Software Development Kits (SDKs) are packages that give access to AWS in a variety of popular programming languages. AWS manages infrastructure as code by using the SDKs and the APIs that underlie them. These language-specific SDKs contain APIs with which customers can incorporate the wide range of AWS Cloud services into their code without writing the functions themselves.

AWS service breadth and depth
AWS offers a broad set of cloud-based products and services, including compute, storage, databases, analytics, networking, mobile, developer tools, management tools, Internet of Things (IoT), security, and enterprise applications. These services help organizations move faster, lower IT costs, and scale. AWS is trusted by large enterprises and start-ups to power a wide variety of workloads including web and mobile applications, game development, data processing and warehousing, storage, archives, and many others.

One of the many differences between an on-premises environment and AWS is that on AWS, customers pay only for what they use. Cost optimization is also making sure customers only pay for what they need, running the exact amount of resources required to get their business done. AWS has identified four key best practices of cost optimization:

Rightsizing instances
Rightsizing is the process of reviewing deployed resources and seeking opportunities to downsize when possible. For example, if an application instance is consistently underutilizing its RAM and CPU, switching that to a smaller instance can offer significant savings while maintaining the same performance.
Increasing application elasticity
An example is using auto scaling to ensure that the correct number of instances are available to handle the workload of an application. Scale out during high demand and scale in during low demand.
Choosing the right pricing model
An example is using Reserved Instances for workloads that need to run most or all the time, such as production environments. This can have a significant impact on savings compared to on-demand; in some cases, up to 75 percent.
Optimizing storage
An example is the S3 Intelligent-Tiering storage class, which is designed to optimize costs by automatically moving data to the most cost-effective storage tier.

The Seven R's
Rehost
Replatform
Relocate
Refactor
Retire
Retain
Repurchase

Regions
Are geographic locations that host 2 or more avaibility zones.
Locais geográficos que possuem zonas de disponibilidade para atender melhor o cliente. Eles não necessáriamente são espelhados para outras regiões.
São isolados dos outros locais geográficos em quesitos de energia, água e localidade.
Os custos podem variar por região. Mas na conta vem como pagamento para região de US-EAST1
O que se preocupar em regiões:
- Quais regulamentações aquela região se comporta?
- Qual o custo dos serviços de AWS naquela região?
- Quais serviços estão disponíveis naquela região?
- Qual a distância ou latência para meus usuários finais?


avaiability zones (AZ)
É uma coleção de data-centers em uma region.
São espelhados entre si, conectados, porém não ficam no mesmo prédio mas proximos entre si, mantendo uma latência baixa. Caso um tenha algum problema, os outros atendem a demanda. É recomendado que os serviços específicos de subnets sejam separados entre elas dentro das AZ para caso tenha um problema com uma sub-net, o sistema todo não será comprometido.

edge location
host a cotent delivery network to delivery content to the costumers

## Usefull Links
[Notion About AWS Practitioner](https://wrf.notion.site/wrf/AWS-Cloud-Practitioner-1f6d122e45d84658ab6621a168035127)