<p>
  <a href="https://blog.bytebytego.com/?utm_source=site"><img src="../images/banner.jpg" /> </a>
</p>

<p align="center">
  【
  <a href="https://www.youtube.com/channel/UCZgt6AzoyjslHTC9dz0UoTw">
    👨🏻‍💻 YouTube
  </a> | 
  <a href="https://blog.bytebytego.com/?utm_source=site">
    📮 Newsletter
  </a> 】
</p>

<a href="https://trendshift.io/repositories/3709" target="_blank"><img src="https://trendshift.io/api/badge/repositories/3709" alt="ByteByteGoHq%2Fsystem-design-101 | Trendshift" style="width: 250px; height: 55px;" width="250" height="55"/></a>

# System Design 101

Explicando sistemas complexos com visuais e termos simples.

Seja que você esteja se preparando para uma Entrevista de Design de Sistemas ou simplesmente deseja entender como sistemas funcionam por baixo do capô, esperamos que este repositório possa te ajudar.

# Tabela de Conteúdos

<!-- TOC toc.levels=2 -->

- [System Design 101](#system-design-101)
- [Tabela de Conteúdos](#tabela-de-conteúdos)
  - [Protocólos de Comunicação](#protocólos-de-comunicação)
    - [REST API vs. GraphQL](#rest-api-vs-graphql)
    - [Como o gRPC funciona?](#como-o-grpc-funciona)
    - [O que é um webhook?](#o-que-é-um-webhook)
    - [Como melhorar a performance de uma API?](#como-melhorar-a-performance-de-uma-api)
    - [HTTP 1.0 -\> HTTP 1.1 -\> HTTP 2.0 -\> HTTP 3.0 (QUIC)](#http-10---http-11---http-20---http-30-quic)
    - [SOAP vs REST vs GraphQL vs RPC](#soap-vs-rest-vs-graphql-vs-rpc)
    - [Code First vs. API First](#code-first-vs-api-first)
    - [Códigos de status HTTP](#códigos-de-status-http)
    - [O que faz um API gatway?](#o-que-faz-um-api-gatway)
    - [Como projetar APIs seguras e efetivas?](#como-projetar-apis-seguras-e-efetivas)
    - [Encapsulação TCP/IP](#encapsulação-tcpip)
    - [Por que o Nginx é chamado de uma proxy "reversa"?](#por-que-o-nginx-é-chamado-de-uma-proxy-reversa)
    - [Quais são os algoritmos de distribuição de carga comuns?](#quais-são-os-algoritmos-de-distribuição-de-carga-comuns)
    - [URL, URI, URN - Você sabe a diferênça?](#url-uri-urn---você-sabe-a-diferênça)
  - [CI/CD](#cicd)
    - [Pipeline CI/CD Explicado em Termos Simples](#pipeline-cicd-explicado-em-termos-simples)
    - [Netflix Stack Tecnológico (Pipeline de CI/CD)](#netflix-stack-tecnológico-pipeline-de-cicd)
  - [Padões de Arquitetura](#padões-de-arquitetura)
    - [MVC, MVP, MVVM, MVVM-C, e VIPER](#mvc-mvp-mvvm-mvvm-c-e-viper)
    - [18 Padrões de Design Essenciais Que Todo Desenvolvedor Deve Conhecer](#18-padrões-de-design-essenciais-que-todo-desenvolvedor-deve-conhecer)
  - [Bancos de Dados](#bancos-de-dados)
    - [Um guia prático de diferentes bancos de dados em serviços de nuvem](#um-guia-prático-de-diferentes-bancos-de-dados-em-serviços-de-nuvem)
    - [8 Estruturas de Dados que Impulsionam seus Bancos de Dados](#8-estruturas-de-dados-que-impulsionam-seus-bancos-de-dados)
    - [Como um comando SQL é executado no Banco de Dados?](#como-um-comando-sql-é-executado-no-banco-de-dados)
    - [Teorema CAP](#teorema-cap)
    - [Tipos de Memória e Armazenamento](#tipos-de-memória-e-armazenamento)
    - [Visualizando uma consulta SQL](#visualizando-uma-consulta-sql)
    - [Linguagem SQL](#linguagem-sql)
  - [Cache](#cache)
    - [Dados são cachados em toda parte](#dados-são-cachados-em-toda-parte)
    - [Por que o Redis é tão rápido?](#por-que-o-redis-é-tão-rápido)
    - [Como o Redis pode ser utilizado?](#como-o-redis-pode-ser-utilizado)
    - [Principais Estratégias de Cache](#principais-estratégias-de-cache)
  - [Arquiteturas de Microsserviços](#arquiteturas-de-microsserviços)
    - [Como é uma arquitetura típica de microsserviços?](#como-é-uma-arquitetura-típica-de-microsserviços)
    - [Melhores Práticas em Microsserviços](#melhores-práticas-em-microsserviços)
    - [Qual pilha tecnológica é comumente utilizada para microsserviços?](#qual-pilha-tecnológica-é-comumente-utilizada-para-microsserviços)
    - [Por quê Kafka é tão rápido](#por-quê-kafka-é-tão-rápido)
  - [Sistemas de Pagamento](#sistemas-de-pagamento)
    - [Como aprender sistemas de pagamento?](#como-aprender-sistemas-de-pagamento)
    - [Por que o cartão de crédito é chamado de "o produto mais lucrativo para os bancos"? Como que a VISA/Mastercard ganham dinheiro?](#por-que-o-cartão-de-crédito-é-chamado-de-o-produto-mais-lucrativo-para-os-bancos-como-que-a-visamastercard-ganham-dinheiro)
    - [Como a VISA funciona quando nós passamos o cartão de crédito em uma loja?](#como-a-visa-funciona-quando-nós-passamos-o-cartão-de-crédito-em-uma-loja)
    - [Série de Sistemas de Pagamento ao Redor do Mundo (Parte 1): Interface Unificada de Pagamentos (UPI, _Unified Payments Interface_) na Índia](#série-de-sistemas-de-pagamento-ao-redor-do-mundo-parte-1-interface-unificada-de-pagamentos-upi-unified-payments-interface-na-índia)
  - [DevOps](#devops)
    - [DevOps vs. SRE vs. Platform Engineering. Qual a diferença?](#devops-vs-sre-vs-platform-engineering-qual-a-diferença)
    - [O que é k8s (Kubernetes)?](#o-que-é-k8s-kubernetes)
    - [Docker vs. Kubernetes. Qual eu deveria usar?](#docker-vs-kubernetes-qual-eu-deveria-usar)
    - [Como o Docker funciona?](#como-o-docker-funciona)
  - [GIT](#git)
    - [Como Comandos do Git funcionam](#como-comandos-do-git-funcionam)
    - [Como o Git funciona?](#como-o-git-funciona)
    - [Git merge vs. Git rebase](#git-merge-vs-git-rebase)
  - [Serviços Cloud](#serviços-cloud)
    - [Um guia prático útil de diferentes serviços em nuvem (edição 2023).](#um-guia-prático-útil-de-diferentes-serviços-em-nuvem-edição-2023)
    - [O que é cloud native?](#o-que-é-cloud-native)
  - [Ferramentas de produtividade para desenvolvedores](#ferramentas-de-produtividade-para-desenvolvedores)
    - [Visualizar arquivos JSON](#visualizar-arquivos-json)
    - [Transformar código em diagramas de arquitetura de forma automática](#transformar-código-em-diagramas-de-arquitetura-de-forma-automática)
  - [Linux](#linux)
    - [Sistema de Arquivos do Linux explicado](#sistema-de-arquivos-do-linux-explicado)
    - [18 Comandos Linux Mais Utilizados que Você Deve Conhecer](#18-comandos-linux-mais-utilizados-que-você-deve-conhecer)
  - [Segurança](#segurança)
    - [Como o HTTPS funciona?](#como-o-https-funciona)
    - [Oauth 2.0 Explicado com Termos Simples.](#oauth-20-explicado-com-termos-simples)
    - [Principais 4 Formas de Mecanismos de Autenticação](#principais-4-formas-de-mecanismos-de-autenticação)
    - [Sessão, cookie, JWT, token, SSO, e OAuth 2.0 - o que são?](#sessão-cookie-jwt-token-sso-e-oauth-20---o-que-são)
    - [Como armazenar senhas de forma segura em bancos de dados e como validá-las?](#como-armazenar-senhas-de-forma-segura-em-bancos-de-dados-e-como-validá-las)
    - [Explicando JSON Web Token (JWT) para uma criança de 10 anos de idade](#explicando-json-web-token-jwt-para-uma-criança-de-10-anos-de-idade)
    - [Como o Autenticador do Google (ou outros tipos de autenticadores de 2-fatores) funciona?](#como-o-autenticador-do-google-ou-outros-tipos-de-autenticadores-de-2-fatores-funciona)
  - [Real World Case Studies](#real-world-case-studies)
    - [Netflix's Tech Stack](#netflixs-tech-stack)
    - [Twitter Architecture 2022](#twitter-architecture-2022)
    - [Evolution of Airbnb’s microservice architecture over the past 15 years](#evolution-of-airbnbs-microservice-architecture-over-the-past-15-years)
    - [Monorepo vs. Microrepo.](#monorepo-vs-microrepo)
    - [How will you design the Stack Overflow website?](#how-will-you-design-the-stack-overflow-website)
    - [Why did Amazon Prime Video monitoring move from serverless to monolithic? How can it save 90% cost?](#why-did-amazon-prime-video-monitoring-move-from-serverless-to-monolithic-how-can-it-save-90-cost)
    - [How does Disney Hotstar capture 5 Billion Emojis during a tournament?](#how-does-disney-hotstar-capture-5-billion-emojis-during-a-tournament)
    - [How Discord Stores Trillions Of Messages](#how-discord-stores-trillions-of-messages)
    - [How do video live streamings work on YouTube, TikTok live, or Twitch?](#how-do-video-live-streamings-work-on-youtube-tiktok-live-or-twitch)
  - [License](#license)

<!-- /TOC -->

## Protocólos de Comunicação

Estilos de arquiteturas definem como os diferentes componentes de uma interface de programação de aplicações (API, _Application Programming Interface_) interagem entre si. Como resultado, eles garantem eficiência, confiabilidade e facilidade de integração com outros sistemas, proporcionando uma abordagem padrão para projetar e construir APIs. Aqui estão os estilos mais utilizados:

<p>
  <img src="../images/api-architecture-styles.png" style="width: 640px">
</p>

- SOAP:

  Amadurecido, abrangente, baseado em XML

  Ideal para aplicações empresariais

- RESTful:

  Popular, fácil implementação, métodos HTTP

  Ideal para serviços web

- GraphQL:

  Linguagem de Consulta, requisita dados específicos

  Reduz sobrecarga de rede, respostas mais rápidas

- gRPC:

  Moderno, alta performance, Protocol Buffers

  Adequado para arquiteturas de microsserviços

- WebSocket:

  Tempo-real, bidirecional, conexões persistentes

  Perfeito para troca de dados de baixa latência

- Webhook:

  Orientado a eventos, chamadas de retorno HTTP, assíncrono

  Notifica o sistema sobre a ocorrência de um evento

### REST API vs. GraphQL

Quando se trata de design de APIs, REST e GraphQL tem suas forças e fraquezas.

O diagrama abaixo mostra uma rápida comparação entre REST e GraphQL.

<p>
  <img src="../images/graphQL.jpg">
</p>

REST

- Utiliza métodos HTTP padrões como GET, POST, PUT, DELETE para operações CRUD.
- Funciona bem quando você precisa de uma interface simples e uniforme entre serviços/aplicações separadas.
- Estratégias de cache são de simples implementação.
- O lado negativo é que pode levar diversas viagens de ida-e-volta para montar os dados relacionados de endpoints separados.

GraphQL

- Fornece um único ponto para clientes realizarem consultas em qualquer dado que precisem.
- Os clientes especificam os campos exatos necessários em consultas aninhadas, e o servidor retorna cargas otimizadas contendo apenas esses campos.
- Suporta Mutations para modificar dados e Subscriptions para notificações em tempo real.
- Ótima para agregar dados de diversas fontes e se adapta bem com requeritos requisitos de frontend que evoluem rapidamente.
- No entanto, isso transfere a complexidade para o lado do cliente e pode permitir consultas abusivas se não forem devidamente protegidas.
- Estratégias de Caching podem ser mais complexas que REST.

A melhor escolha entre REST e GraphQL depende nos requisitos específicos da aplicação e time de desenvolvimento. GraphQL é uma boa opção para necessidades frontend complexas ou que mudam frequentemente, enquanto REST é adequado para aplicações onde contratos simples e consistentes são preferidos.

Nenhuma abordagem dessas APIs é uma solução milagrosa. Avaliar cuidadosamente os requisitos e as compensações é importante para escolher o estilo certo. Tanto REST quanto GraphQL são opções válidas para expor dados e impulsionar aplicações modernas.

### Como o gRPC funciona?

RCP (Chamada de Procedimento Remota, _Remote Procedure Call_) é chamada de "**remota**" pois habilita comunicação entre serviços quando estes são implantados em servidores sob a arquitetura de microsserviços. Do ponto de vista do usuário, ele age como uma chamada de função local.

O diagrama abaixo ilustra o fluxo geral de dados para o **gRPC**.

<p>
  <img src="../images/grpc.jpg">
</p>

Passo 1: Uma chamada REST parte do cliente. O corpo da requisição é geralmetne em formato JSON.

Passo 2 - 4: O Serviço de Pedidos (_Order Service_, que é o cliente gRPC) recebe a chamada REST, a transforma e realiza uma chamada RPC para o Serviço de Pagamentos (_Payment Service_). O gRPC codifica o stub do cliente em um formato binário e o envia para a camada de transporte de baixo nível.

Passp 5: O gRPC envia os pacotes pela rede via HTTP2. Por conta da codificação binária e otimizações de rede, o gRPC é dito ser 5x mais rápido que JSON.

Passo 6 - 8: O Serviço de Pagamentos (_Payment Service_, servidor gRPC) recebe os pacotes da rede, os decodifica e invoca a aplicação do servidor.

Passos 9 - 11: O resultado é retornado pela aplicação do servidor, codificado e enviado para a camada de transporte.

Passos 12 - 14: O Serviço de Pedidos (_Order Service_, cliente gRPC) recebe os pacotes, os decodifica e envia o resultado para a aplicação cliente.

### O que é um webhook?

O diagrama abaixo mostra uma comparação entre Polling e Webhook.

<p>
  <img src="../images/webhook.jpeg" style="width: 680px" />
</p>

Assuma que estamos rodando um website de eCommerce. Os clientes enviam ordens para o Serviço de Ordems pelo API gateway, que aciona o Serviço de Pagamento para transações de pagament. O Serviço de Pagamento fala com um provedor de serviços de pagamento (PSP) para completar as transações.

Há duas forms de lidar comcomunicações com um PSP.

**1. Polling Curto (Short Polling)**

Depois de enviar um pedido de pagamento para o PSP, o serviço de pagamento fica perguntando ao PSP sobre o status do pagamento. Depois de alguns rounds, o PSP finalmente retorna o status.

Polling curto possui duas desvantagens:

- Relizar polling constante a respeito do status consome recursos do Serviço de Pagamento.
- O Serviço Externo se comuica diretamente com o Serviço de Pagamento, criando vulnerabilidades.

**2. Webhook**

Nós podemos registrar um webhook com o Serviço Externo. Isso é: Me avise neste URL quando você tiver alguma atualização da requisição. Quando o PSP completaqr o processamento, ele irá invocar uma requisição HTTP para atualizar o status do pagamento.

Desta forma, o paradigma da programação mudou, quando o Serviço de Pagamento não precisa mais desperdiçar recursos fazendo polling no status de pagamento.

Mas e se o PSP não nos retorna? Podemos fazer uma tarefa/serviço de limpeza para checar o status de pagamento a cada hora.

Webhooks são geralmente referidos como APIs reversos ou push APIs, já que o servidor envia requisições HTTP para o cliente. Nós precisamos prestar atenção a 3 pontos quando utilizamos webhooks:

1. Precisamos projetar uma API adequada para ser chamada pelo serviço externo.
2. Precisamos configurar regras adequadas para o API gateway por razões de segurança.
3. Precisamos registrar a URL correta no Serviço Externo.

### Como melhorar a performance de uma API?

O diagrama abaixo mostra 5 truques comuns para melhorar a performance de uma API.

<p>
  <img src="../images/api-performance.jpg">
</p>

Paginação

Esta é uma otimização comun quando o tamanho do resultado é muito grande. Os resultados são transmitidos de volta para o cliete para melhorar a reponsividade do serviço.

Logging Assíncrono

O log síncrono lida com o disco a cada chamada e pode diminuir a velocidade do sistema. O log assíncrono envia os logs primeiro para um buffer sem bloqueio e retorna imediatamente. Os logs serão periodicamente gravados no disco. Isso reduz significativamente a sobrecarga de E/S (Entrada/Saída).

Caching

Nós podemos armazenar dados frequentemente acessados num cache. O cliente pode realizar uma consulta no cache primeiramente, ao invés de ir direto ao banco de dados. Se ocorrer um cache miss, o cliente deve realizar a consulta ao banco. Caches como Redis armazenam dados em memória, deixando o acesso aos dados muito mais rápido que em um banco de dados.

Compressão da Carga Útil

As slicitações e respostas podem ser comprimidas utilizando gzip etc para que os dados transmitidos tenham um tamanho menor. Isso acelera o upload e download.

Pool de Conexões

Ao acessar recursos, nós precisamos carregar dados do banco de dados. Abrir e fechar conexões com o baco adiciona uma sobrecarga significativa. Portanto podemos nos conectar por um pool de conexões abertas. O pool de conexões é responsável por gerenciar o ciclo de vida da conexão.

### HTTP 1.0 -> HTTP 1.1 -> HTTP 2.0 -> HTTP 3.0 (QUIC)

Quais problemas são resolvidos por cada geração de HTTP?

O diagrama abaixo ilustra as principais características.

<p>
  <img src="../images/http3.jpg" />
</p>

- HTTP 1.0 foi finalizado e totalmente documentado em 1996. Cada solicitação ao mesmo servidor requer uma conexão TCP separada.

- HTTP 1.1 foi publicado em 1997. Uma conexão TCP pode ser deixada aberta para reutilização (conexão persistente), mas não resolve o problema do bloqueio HOL (head-of-line).

  Bloqueio HOL - quando o número de solicitações paralelas permitidas no navegador é esgotado, solicitações subsequentes precisam aguardar as anteriores serem concluídas.

- HTTP 2.0 foi publicado em 2015. Ele aborda o problema HOL por meio do multiplexamento de solicitações, o que elimina o bloqueio HOL na camada de aplicação, mas HOL ainda existe na camada de transporte (TCP).

  Como você pode ver no diagrama, o HTTP 2.0 introduziu o conceito de "streams" HTTP: uma abstração que permite multiplexar diferentes trocas de HTTP na mesma conexão TCP. Cada stream não precisa ser enviado em ordem.

- HTTP 3.0 teve seu rascunho publicado em 2020. Ele é o sucessor proposto do HTTP 2.0. Utiliza o QUIC em vez do TCP como protocolo de transporte subjacente, removendo assim o bloqueio HOL na camada de transporte.

  O QUIC é baseado no UDP. Ele introduz streams como cidadãos de primeira classe na camada de transporte. Os streams QUIC compartilham a mesma conexão QUIC, portanto, não são necessários handshake adicionais e inícios lentos para criar novas conexões, mas os streams QUIC são entregues independentemente, de modo que, na maioria dos casos, a perda de pacotes que afeta uma stream não afeta as outras.

### SOAP vs REST vs GraphQL vs RPC

O diagrama abaixo ilustra a linha do tempo da API e a comparação de estilos de API.

Ao longo do tempo, diferentes estilos arquiteturais de API são lançados. Cada um deles tem suas próprias técnicas para padronizar a troca de dados.

Você pode conferir os casos de uso de cada estilo no diagrama.

<p>
  <img src="../images/SOAP vs REST vs GraphQL vs RPC.jpeg" />
</p>

### Code First vs. API First

O diagrama abaixo mostra as diferenças entre o desenvolvimento Code First e o desenvolvimento API First. Por que queremos considerar o design API First?

<p>
  <img src="../images/api_first.jpg" style="width: 680px" />
</p>

- Microsserviços aumentar a complexidade do sistema e precisamos separar serviços para servir funções diferentes no sistema. Embora esse tipo de arquitetura facilite o desacoplamento e a segregação de responsabilidades, é necessário lidar com as diversas comunicações entre os serviços.

É melhor analisar a complexidade do sistema antes de escrever o código e definir cuidadosamente os limites dos serviços.

- Equipes funcionais separadas precisam falar a mesma linguagem, e as equipes funcionais dedicadas são responsáveis apenas por seus próprios componentes e serviços. Recomenda-se que a organização fale a mesma linguagem por meio do design de API.

Podemos simular solicitações e respostas para validar o design da API antes de escrever o código.

- Melhora a qualidade do software e a produtividade do desenvolvedor. Como resolvemos a maioria das incertezas no início do projeto, o processo de desenvolvimento é mais suave, e a qualidade do software é significativamente aprimorada.

Os desenvolvedores ficam satisfeitos com o processo, pois podem se concentrar no desenvolvimento funcional em vez de lidar com mudanças repentinas.

A possibilidade de surpresas no final do ciclo de vida do projeto é reduzida.

Como projetamos a API primeiro, os testes podem ser planejados enquanto o código está sendo desenvolvido. De certa forma, também temos o TDD (Design Orientado a Testes) ao usar o desenvolvimento API first.

### Códigos de status HTTP

<p>
  <img src="../images/http-status-code.jpg" style="width: 540px" />
</p>

Os códigos de resposta para o HTTP são divididos em cinco categorias:

Informativos (100-199)
Sucesso (200-299)
Redirecionamento (300-399)
Erro do Cliente (400-499)
Erro do Servidor (500-599)

### O que faz um API gatway?

O diagrama abaixo ilustra as principais características.

<p>
  <img src="../images/api_gateway.jpg" style="width: 520px" />
</p>

Passo 1 - O cliente enviar uma requisição HTTP para o API gateway.

Passo 2 - O API gateway analisa e valida os atributos na solicitação HTTP.

Passo 3 - O API gateway verifica a lista de permissões/negações.

Passo 4 - O API gateway se comunica com um provedor de identidade para autenticação e autorização.

Passo 5 - As regras de limitação de taxa são aplicadas à solicitação. Se estiver acima do limite, a solicitação é rejeitada.

Passos 6 e 7 - Agora que a solicitação passou pelas verificações básicas, o API gateway encontra o serviço relevante para rotear por meio de correspondência de caminho.

Passo 8 - O API gateway transforma a requisição no protocolo apropriado e o envia aos microsserviços do backend.

Passos 9-12: O API agteway pode lidar adequadamente com erros e tratar falhas se o erro levar mais tempo para se recuperar (circuit break). Também pode usar a pilha ELK (Elastic-Logstash-Kibana) para registro e monitoramento. Às vezes, são armazenados dados em cache no gateway de API.

### Como projetar APIs seguras e efetivas?

O diagrama abaixo ilustra os designs típicos de API com um exemplo de carrinho de compras.

<p>
  <img src="../images/safe-apis.jpg" />
</p>

Observe que o design da API não se resume apenas ao design do caminho do URL. Na maioria das vezes, precisamos escolher nomes apropriados para os recursos, identificadores e padrões de caminho. É igualmente importante projetar campos de cabeçalho HTTP adequados ou criar regras eficazes de limitação de taxa dentro do API gateway.

### Encapsulação TCP/IP

Como os dados são enviados pela rede? Por que nós precisamos de tantas camadas no modelo OSI?

O diagrama abaixo mostra como dados são encapsulados e desencapsulados ao trasmitidos pela rede.

<p>
  <img src="../images/osi model.jpeg" />
</p>

Passo 1: Quando o Dispositivo A envia dados para o Dispositivo B pela rede via protocolo HTTP, é primeiro adicionado um cabeçalho HTTP na camada de aplicação.

Passo 2: Em seguida, é adicionado um cabeçalho TCP ou UDP aos dados. Eles são encapsulados em segmentos TCP na camada de transporte. O cabeçalho contém a porta de origem, a porta de destino e o número de sequência.

Passo 3: Os segmentos são então encapsulados com um cabeçalho IP na camada de rede. O cabeçalho IP contém os endereços IP de origem/destino.

Passo 4: O datagrama IP é adicionado a um cabeçalho MAC na camada de enlace de dados, com endereços MAC de origem/destino.

Passo 5: Os quadros encapsulados são enviados para a camada física e transmitidos pela rede em bits binários.

Passos 6-10: Quando o Dispositivo B recebe os bits da rede, ele realiza o processo de desencapsulamento, que é um processo reverso do processo de encapsulamento. Os cabeçalhos são removidos camada por camada e, eventualmente, o Dispositivo B pode ler os dados.

Precisamos de camadas no modelo de rede porque cada camada se concentra em suas próprias responsabilidades. Cada camada pode depender dos cabeçalhos para obter instruções de processamento e não precisa conhecer o significado dos dados da camada anterior.

### Por que o Nginx é chamado de uma proxy "reversa"?

O diagrama abaixo mostra as diferenças entre um proxy de encaminhamento (𝐟𝐨𝐫𝐰𝐚𝐫𝐝 𝐩𝐫𝐨𝐱𝐲) e um proxy de reverso (𝐫𝐞𝐯𝐞𝐫𝐬𝐞 𝐩𝐫𝐨𝐱𝐲).

<p>
  <img src="../images/Forward Proxy v.s. Reverse Proxy2x.jpg" style="width: 720px" />
</p>

Uma proxy de encaminhamento é um servidor que fica entre usuários e dispositivos na internet.

Uma proxy de encaminhamento é comumente utilizada para:

1. Proteger clientes
2. Burlar restrições de navegação
3. Bloquear acesso a conteúdos específicos

Uma proxy reversa é um servidor que aceita uma requisição de um cliente, direciona a requisição aos servidores web e retorna os resultados para o cliete como se o próprio servidor proxy tivesse processado a requisição.

Uma proxy reversa é boa para:

1. Proteger servidores
2. Distribuição de Carga
3. Cachear conteúdo estático
4. Encriptar e decriptar comunicações SSL

### Quais são os algoritmos de distribuição de carga comuns?

O diagrama abaixo mostra 6 algoritmos comuns.

<p>
  <img src="../images/lb-algorithms.jpg" />
</p>

- Algoritmos estáticos

1. Round robin

   As requisições dos clientes são enviadas para diferentes instancias de serviços em uma ordem sequencial. Os serviços são usualmente requeridos a serem stateless.

2. Round-robin pegajoso (_sticky_)

   Este é uma melhoria do algoritmo de orund-robin. De a primeira requisição de Alice vai para o serviço A, então as requisições seguintes também vão para o serviço A.

3. Round-robin ponderado (_weighted_)

   O administrador pode especificar um peso para cada serviço. Os que tiverem um peso maior, lidam com mais requisições que os outros.

4. Hash

   Este algoritmo aplica uma função hash (de disperção) nos IPs ou URLs das requisições. As requisições são roteadas para instâncias relvantes com base no resultado do resultado da função hash.

- Dynamic Algorithms

5. Least connections

   A new request is sent to the service instance with the least concurrent connections.

6. Least response time

   A new request is sent to the service instance with the fastest response time.

### URL, URI, URN - Você sabe a diferênça?

O diagrama abaixo mostra uma comparação de URL, URI e URN.

<p>
  <img src="../images/url-uri-urn.jpg" />
</p>

- URI

URI significa Idetificador Uniforme de Recursos (_Uniform Resource Identifier_). Ele identifica um recurso lógico ou físico na web. URL e URN são subtipos de URI. URL localiza um recurso, enquanto URN nomeia um recurso.

Um URI é composto das seguintes partes:
scheme:[//authority]path[?query][#fragment]

- URL

URL significa Localizador Uniforme de Recurso (_Uniform Resource Locator_), o conceito-chave do HTTP. É o endereço de um recurso único na web. Pode ser usado com outros protocolos, como FTP e JDBC.

- URN

URN significa Nome Uniforme de Recurso (_Uniform Resource Name_). Ele usa o esquema urn. URNs não podem ser usados para localizar um recurso. Um exemplo simples fornecido no diagrama é composto por um namespace e uma string específica do namespace.

Se você deseja obter mais detalhes sobre o assunto, eu recomendaria a [explicação do W3C](https://www.w3.org/TR/uri-clarification/).

## CI/CD

### Pipeline CI/CD Explicado em Termos Simples

<p>
  <img src="../images/ci-cd-pipeline.jpg" style="width: 680px" />
</p>

Seção 1 - SDLC com CI/CD

O ciclo de vida de desenvolvimento de software (SDLC, _Software Development Life Cycle_) consiste em várias etapas-chave: desenvolvimento, teste, implantação e manutenção. CI/CD automatiza e integra essas etapas para possibilitar lançamentos mais rápidos e confiáveis.

Quando o código é enviado para um repositório Git, isso aciona um processo automatizado de compilação e teste. Casos de teste de ponta a ponta (end-to-end ou e2e) são executados para validar o código. Se os testes são bem-sucedidos, o código pode ser implantado automaticamente no ambiente de preparo/produção. Se problemas são identificados, o código é enviado de volta para o desenvolvimento para correção de bugs. Essa automação proporciona um feedback rápido aos desenvolvedores e reduz o risco de erros em produção.

Seção 2 - Diferença entre CI e CD

Integração Continua (CI, Continous Integrations) automatiza o processo de compilação, teste e o processo de implantação. Roda testes quando código é comitado para detecção de problemas de integração precocemente. Isso encoraja commits frequentes e feedback rápido.

Entrega Contínua (CD, Continuous Delivery) automatiza processos de lançamento como mudanças de infraestrutura e implantação. Garante que o software possa ser lançado de maneira confiável a qualquer momento por meio de fluxos de trabalho automatizados. A CD também pode automatizar etapas de teste manual e aprovação necessárias antes da implantação em produção.

Seção 3 - Pipeline de CI/CD

Um pipeline típico de CI/CD tem alguns estágios conectados:

- O desenvolvedor comita mudanças de código para o controle de versão
- O servidor de CI detecta as mudanças e dá início à compilação
- Code é compilado e testado (unitário e de integração)
- Os resultados são reportados ao desenvolvedor
- No sucesso, artefatos são lançados para o ambiente de preparo (staging)
- Testes adicionais podem ser realizados no ambiente de preparo antes do lançamento
- O sistema de CD lança mudanças aprovadas para produção

### Netflix Stack Tecnológico (Pipeline de CI/CD)

<p>
  <img src="../images/netflix-ci-cd.jpg" style="width: 720px" />
</p>

Planejamento: A Engenharia da Netflix utiliza o JIRA para planejamento e o Confluence para documentação.

Codificação: Java é a linguagem de programação principal para o serviço backend, enquanto outras linguagens são utilizadas para diferentes casos de uso.

Compilação: Gradle é principalmente utilizado para compilação, e plugins do Gradle são construídos para suportar vários casos de uso.

Empacotamento: O pacote e suas dependências são empacotados em uma Imagem de Máquina Amazon (AMI, _Amazon Machine Image_) para lançamento.

Testes: Os testes enfatizam o foco da cultura de produção na construção de ferramentas de caos.

Implantação: A Netflix utiliza sua própria ferramenta Spinnaker para implantação de rollout de canário.

Monitoramento: As métricas de monitoramento são centralizadas no Atlas, e o Kayenta é utilizado para detectar anomalias.

Relatório de Incidentes: Incidentes são despachados de acordo com a prioridade, e o PagerDuty é utilizado para o tratamento de incidentes.

## Padões de Arquitetura

### MVC, MVP, MVVM, MVVM-C, e VIPER

Esses padrões de arquitetura estão entre os mais comumente utilizados no desenvolvimento de aplicativos, seja nas plataformas iOS ou Android. Os desenvolvedores os introduziram para superar as limitações de padrões anteriores. Então, como eles diferem?

<p>
  <img src="../images/client arch patterns.png" style="width: 720px" />
</p>

- MVC (Modelo-Visão-Controle, _Model View Controller_), o padrão mais antigo, de quase 50 anos
- Cada padrão possui uma "visão", _view_ (V) responsável por exibir conteúdo e receber entrada do usuário
- A maioria dos padrões incluem um "modelo", _model_ (M) para manusear dados de negócio
- "Controller", "presenter" e "view-model" são tradutores que atuam como mediadores entre a "view" e o "model" (ou "entity" no padrão VIPER).

### 18 Padrões de Design Essenciais Que Todo Desenvolvedor Deve Conhecer

Padrões são soluções reutilizáveis para problemas comuns de design, resultando em um processo de desenvolvimento mais linear e eficiente. Eles servem como modelos para construir estruturas de software mais sólidas. Aqui estão alguns dos padrões mais populares:

<p>
  <img src="../images/18-oo-patterns.png" />
</p>

- Fábrica Abstrata (_Abstract Factory_): Criador de Famílias - Cria grupos de itens relacionados.
- Construtor (_Builder_): Mestre Lego - Constrói objetos passo a passo, mantendo a criação e a aparência separadas.
- Protótipo (_Prototype_): Clone Maker - Cria cópias de exemplos totalmente preparados.
- Singleton: Único e Exclusivo - Uma classe especial com apenas uma instâcia.
- Adaptador(_Adapter_): Plugue Universal - Conecta coisas com interfaces diferentes.
- Ponte (_Bridge_): Connectador Funcional - Liga como um objeto funciona ao que ele faz.
- Composito (_Composite_): Constutor de Árvores - Forma uma estruturas semelhantes a árvore com partes simples e complexas.
- Decorador (_Decorator_): Customizador - Adiciona funcionalidade a objetos sem alterar seu núcleo.
- Façada (_Facade_): Tudo em Um - Representa um sistema inteiro com uma única interface simplificada.
- Peso Mosca (_Flyweight_): Economizador de Espaço - Compartilha itens pequenos e reutilizáveis de maneira eficiente.
- Proxy: Ator Substituto - Representa outro objeto, controlando acesso ou ações.
- Cadeia de Responsabilidades (_Chain of Responsibility_): Relé de Requisições - Passa uma requisição por uma cadeia de objetos até que seja tratada.
- Comando (_Command_): Envelopador de Tarefas - Transforma uma solicitação em um objeto, pronto para atuar.
- Iterador (_Iterator_): Exploração de Coleções - Acessa elementos em uma coleção, um a um.
- Mediador (_Mediator_): Central de Comunicações - Simplifica interações entre classes distintas.
- Lembrança (_Memento_): Cápsula do Tempo - Captura e restaura o estado de um objeto.
- Observador (_Observer_): Emissora de Notícias - Notifica classes sobre mudanças em outros objetos.
- Visitante (_Visitor_): Hóspede Habilidoso - Adiciona novas operações a uma classe sem alterá-la.

## Bancos de Dados

### Um guia prático de diferentes bancos de dados em serviços de nuvem

<p>
  <img src="../images/cloud-dbs2.png" />
</p>

Escolher o banco de dados correto para o seu projeto é uma tarefa complexa. Muitas opções de bancos de dados, cada uma adequada a casos de uso distintos, podem rapidamente levar à fadiga de decisões.

Esperamos que este guia prático forneça direcionamento de alto nível para identificar o serviço correto que esteja alinhado com as necessidades do seu projeto e evite possíveis ciladas.

Nota: O Google limitou a documentação para os casos de uso de seus banco de dados. Mesmo que tenhamos feito o nosso melhor para examinar o que estava disponível e chegar à melhor opção, algumas das entradas podem precisar de maior precisão.

### 8 Estruturas de Dados que Impulsionam seus Bancos de Dados

A resposta irá variar dependendo do seu caso de uso. Dados podem ser indexados em memória ou em disco. Similarmente, os formatos dos dados variam, como números, strings, coordenadas geográficas etc. O sistema pode ser intensivo em escrita (write-heavy) ou intensivo em leitura (read-heavy). Todos esses fatores afetam a escolha do formato de índice do banco de dados.

<p>
  <img src="../images/8-ds-db.jpg" />
</p>

A seguir estão algumas das estruturas de dados mais populares usadas para indexar dados:

- Skiplist: um tipo comum de índice em memória. Usado no Redis
- Índice de hash: uma implementação muito comum da estrutura de dados "Mapa" (ou "Coleção")
- SSTable: implementação em disco e imutável do "Mapa"
- Árvore LSM: Skiplist + SSTable. Alta taxa de gravação
- B-tree: solução baseada em disco. Desempenho de leitura/gravação consistente
- Índice invertido: usado para indexação de documentos. Usado no Lucene
- Árvore de sufixos: para pesquisa de padrões em strings
- R-tree: pesquisa multidimensional, como encontrar o vizinho mais próximo

### Como um comando SQL é executado no Banco de Dados?

O diagrama abaixo demonstra o processo. Note que a arquitetura de diferentes bancos são diferentes, o diagrama apresenta alguns designs comuns.

<p>
  <img src="../images/sql execution order in db.jpeg" style="width: 580px" />
</p>

Passo 1 - Uma instrução SQL é enviada para o banco de dados por meio de um protocolo de camada de transporte (por exemplo, TCP).

Passo 2 - A instrução SQL é enviada ao analisador (_parser_) de comandos, onde passa por análise sintática e semântica, e em seguida, uma árvore de consulta é gerada.

Passo 3 - A árvore de consulta é enviada ao otimizador. O otimizador cria um plano de execução.

Passo 4 - O plano de execução é enviado ao executor. O executor recupera os dados da execução.

Passo 5 - Métodos de acesso fornecem a lógica de recuperação de dados necessária para a execução, recuperando dados do mecanismo de armazenamento (_storage engine_).

Passo 6 - Os métodos de acesso decidem se a instrução SQL é somente leitura. Se a consulta for somente leitura (instrução SELECT), ela é enviada para o gerenciador de buffer para processamento adicional. O gerenciador de buffer procura os dados no cache ou nos arquivos de dados.

Passo 7 - Se a instrução for um UPDATE ou INSERT, ela é enviada para o gerenciador de transações para processamento adicional.

Passo 8 - Durante uma transação, os dados estão em modo de bloqueio. Isso é garantido pelo gerenciador de bloqueio. Ele também assegura as propriedades ACID da transação.

### Teorema CAP

O Teorema CAP é um dos termos mais famosos na ciência da computação, mas aposto que desenvolvedores diferentes tem interpretações diferentes. Vamos examinar o que é e por que pode ser confuso.

<p>
  <img src="../images/cap theorem.jpeg" />
</p>

O teorema CAP afirma que um sistema distribuído não pode fornecer mais do que duas destas três garantias simultaneamente.

**Consistência**: consistência significa que todos os clientes enxergam os mesmos dados ao mesmo tempo, não importando em qual nó eles se conectam.

**Disponibilidade**: disponibilidade significa que qualquer cliente que realizar uma requisição de dados terá uma resposta, mesmo que alguns nós não estejam de pé.

**Tolerância de Partição**: uma partição indica uma quebra na comunicação entre dois nós. Uma tolerância de partição significa que o sistema continua em operação apesar de partições de redes.

A formulação "2 de 3" pode ser útil, **mas essa simplificação pode ser enganosa**.

1. Escolher um banco de dados não é fácil. Justificar sua escolha puramente no teorema CAP não é o suficiente. Por exemplo, companhias não escolhem Cassandra para aplicativos de cat simplesmente por ser um sistema AP. Há uma lista de características que tornam uma opção boa para armazenamento de mensagens de chat. Precisamos cavar mais fundo.

2. "CAP proíbe apenas uma pequena parte do espaço de design: disponibilidade e consistência perfeitas na presença de partições, que são raras". Citado do artigo: CAP Twelve Years Later: How the "Rules" Have Changed.

3. O teorema trata de disponibilidade e consistência de 100%. Uma discussão mais realista envolveria as compensações entre latência e consistência quando não há partição de rede. Consulte o teorema PACELC para obter mais detalhes.

**O teorema CAP é de fato útil?**

Acredito que ainda é útil por abrir nossas mentes para um novo conjunto de discussões sobre compensações, mas é apenas uma parte da história. Precisamos nos aprofundar para esolcher o banco de dados correto.

### Tipos de Memória e Armazenamento

<p>
  <img src="../images/Types_of_Memory_and_Storage.jpeg" style="width: 420px" />
</p>

### Visualizando uma consulta SQL

<p>
  <img src="../images/sql-execution-order.jpg" style="width: 580px" />
</p>

As instruções SQL são executadas pelo sistema do banco de dados em várias etapas, incluindo:

- Analisando a instrução SQL e verificando sua validade
- Transformando o SQL em uma representação interna, como álgebra relacional
- Otimizando a representação interna e criando um plano de execução que utiliza informações de índices
- Executando o plano e retornando os resultados

A execução do SQL é altamente complexa e envolve muitas considerações, tais como:

- O uso de índices e caches
- A ordem de junções de tabelas
- Controle de concorrência
- Gerenciamento de transações

### Linguagem SQL

In 1986, SQL (Structured Query Language) became a standard. Over the next 40 years, it became the dominant language for relational database management systems. Reading the latest standard (ANSI SQL 2016) can be time-consuming. How can I learn it?

Em 1986, SQL (Linguagem de Busca Estruturada, _Structured Query Language_) se tornou um padrão. Ao longo os próximos 40 anos, ela se tornou a linguagem dominante para sistemas de manuseamento de bancos de dados relacionais. Ler o último padrão (ANSI SQL 2016) pode ser demorado. Como posso aprenê-lo?

<p>
  <img src="../images/how-to-learn-sql.jpg" />
</p>

Há 5 componentes da linguagem SQL:

- DDL: linguagem de definição de dados, como CREATE, ALTER, DROP
- DQL: linguagem de consulta de dados, como SELECT
- DML: linguagem de manipulação de dados, como INSERT, UPDATE, DELETE
- DCL: linguagem de controle de dados, como GRANT, REVOKE
- TCL: linguagem de controle de transações, como COMMIT, ROLLBACK

Para um engenheiro de backend, pode ser necessário saber a maior parte deles. Como um analista de dados, é importante ter uma boa noção do DQL. Selecione os tópicos que são mais relevantes para você.

## Cache

### Dados são cachados em toda parte

Este diagrama ilustra onde nós cachamos dados em uma arquitetura típica.

<p>
  <img src="../images/where do we cache data.jpeg" style="width: 720px" />
</p>

Existem múltiplas camadas ao longo do fluxo.

1. Aplicativos cliente: As respostas HTTP podem ser armazenadas em cache pelo navegador. Solicitamos dados pela primeira vez por meio do HTTP, e eles são retornados com uma política de expiração no cabeçalho HTTP; solicitamos os dados novamente, e o aplicativo cliente tenta recuperar os dados primeiro do cache do navegador.

2. CDN: CDN (Rede de distribuição de Conteúdos, _Content Delivery Network_) cacha recursos web estáticos. Os clientes podem recuperar dados de um nó de CDN próximo.
3. Distribuidor de Cargas: O distribuidor de cargas também pode cachar recursos.
4. Infraestrutura de mensagens: Corretores de Mensagens (_Message Brokers_) armazenam mensagens primeiramente no disco, e depois os consumidores as recuperam em seu próprio ritmo. Dependendo da política de retenção, os dados são cachados em clusters Kafka por um curto período de tempo.
5. Serviços: Há múltiplas camadas de cache em um serviço. Se o dado não está cachado no cache da CPU, o serviço irá tentar recuperar o dado da memória. As vezes o serviço tem uma segunda camada de cache para armazenar dados em disco.
6. Cache Distribuído: Cache distribuído como Redis armazena pares chave-valor para múltiplos serviços em memória. Ele provê performance de leitura/escrita muito melhor que em um banco de dados.
7. Pesquisa de Texto Completo (_Full-text Search_): as vezes precisamos realizar pesquisas de texto completas como Elastic Search para buscas em documentos ou logs. Uma cópia dos dados é indexada na ferramenta de busca também.
8. Banco de Dados: Até mesmo nos bancos de dados, temos diferentes níveis de cache.

- WAL (Write-ahead Log): os dados são gravados primeiro no WAL antes de construir o índice B-tree.
- Bufferpool: Uma área de memória alocada para cachar os resultados das consultas
- Visualização Materializada: Pré-calcular os resultados da consulta e armazená-los nas tabelas do banco de dados para melhorar o desempenho das consultas
- Materialized View: Pre-compute query results and store them in the database tables for better query performance
- Log de Transação: registrar todas as transações e atualizações do banco de dados
- Log de Replicação: usado para registrar o estado de replicação em um cluster de banco de dados.

### Por que o Redis é tão rápido?

Há 3 razões principais, como mostrado no diagrama abaixo.

<p>
  <img src="../images/why_redis_fast.jpeg" />
</p>

1. Redis é um armazenamento baseado em memória RAM. O acesso à RAM é pelo menos 1000 vezes mais rápido que um acesso aleatório ao disco.
2. O Redis alavanca multipleximento de IO e um loop single-threaded para eficácia de execução.
3. O Redis utiliza algumas estruturas eficázes de baixo nível.

Pergunta: Outro armazenamento em memória popular é o Memcached. Você sabe as diferenças entre Redis e Memcached?

Você pode ter notado que o estilo deste diagrama é diferente dos posts anteriores. Por favor me avise sobre qual você prefere.

### Como o Redis pode ser utilizado?

<p>
  <img src="../images/top-redis-use-cases.jpg" style="width: 520px" />
</p>

Há mais no redis do que apenas caching.

O Redis pode ser utilizado em uma variedade de cenários, conforme mostrado no diagrama.

- Sessão

  Nós podemos utilizar o Redis para compartilhar a sessão do usuário entre diferentes serviços.

- Cache

  Nós podemos utilizar o Redis para cachar objetos ou páginas, especialmente para dados quentes (acessados com frequência alta, _hotspot data_).

- Trava distribuída

  Podemos usar o tipo de dado String do Redis para adquirir uma trava (_lock_) dentre serviços distribuídos.

- Contador

  Podemos contar quantos likes ou quantas leituras em um artigo.

- Limitador de Taxa

  Podemos aplicar um limitador de taxa para determinados IPs de usuários.

- Gerador de ID Global

  Podemos usar o tipo de dado Int no Redis para gerar IDs globais.

- Carrinho de Compras

  Podemos usar o tipo de dado Hash no Redis para representar pares chave-valor em um carrinho de compras.

- Calcular Retenção de Usuários

  Podemos usar o tipo de dado Bitmap no Redis para representar os logins diários dos usuários e calcular a retenção de usuários.

- Fila de Mensagens

  Podemos usar o tipo de dado Lista no Redis para uma fila de mensagens.

- Ranking

  Podemos usar o tipo de dado ZSet (conjunto ordenado) no Redis para classificar os artigos.

### Principais Estratégias de Cache

Projetar sistemas de larga escala geralmente requer consideração cuidadosa de caching. Abaixo são cinco estratégias de caching frequentemente utilizadas.

<p>
  <img src="../images/top_caching_strategy.jpeg" style="width: 680px" />
</p>

## Arquiteturas de Microsserviços

### Como é uma arquitetura típica de microsserviços?

O diagrama abaixo mostra uma arquitetura típica de microsservissos.

<p>
  <img src="../images/typical-microservice-arch.jpg" style="width: 520px" />
</p>

- Distribuidor de Cargas: Isso distribui tráfego de entrada para multiplos serviços de backend.
- CDN (Rede de Distribuição de Serviços, _Content Delivery Network_): CDN é um grupo de servidores distribuídos geograficamente que armazenam conteúdos estáticos para entrega mais rápida. O cliente procura por conteúdo primeiro no CDN, e apenas depois para os serviços de backend.
- API Gateway: Isso lida com as solicitações recebidas e as direciona para os serviços relevantes. Ele se comunica com o provedor de identidade e descoberta de serviços.
- Provedor de identidade (_Identity Provider_): Isso lida com autenticação e autorização para os usuários.
- Registro e Descoberta de Serviços: O registro e a descoberta de microsserviços ocorrem neste componente, e o API Gateway procura por serviços relevantes neste componente para se comunicar.
- Gerenciamento: Este componente é responsável por monitorar os serviços.
- Microsserviços: Microsserviços são desenhados e implantados em diversos domínios.
- Microservices: Microsserviços são projetados e implantados em diferentes domínios. Cada domínio tem seu próprio banco de dados. O API Gateway se comunica com os microsserviços por meio de API REST ou outros protocolos, e os microsserviços dentro do mesmo domínio se comunicam entre si usando RPC (Chamada de Procedimento Remoto).

Benefícios de microsserviços:

- Podem ser projetados e implantados e escalados horizontalmente rapidamente.
- Cada domínio pode ser mantido independentemente por uma equipe dedicada.
- Os requisitos de negócios podem ser personalizados em cada domínio e, como resultado, melhor suportados.

### Melhores Práticas em Microsserviços

Uma imagem vale por mil palavras: 9 melhores práticas para desenvolver microsserviços.

<p>
  <img src="../images/microservice-best-practices.jpeg" />
</p>

Quando desenvolvemos microsserviços, nós precisamos seguir as seguintes melhores práticas:

1. Utilize armazenamento de dados separado para cada microsserviço
2. Mantenha o código em um nível semelhante de maturidade
3. Faça compilação separada para cada microsserviço
4. Atribua a cada microsserviço uma única responsabilidade
5. Implante em containers
6. Projete serviços sem estado
7. Adote o design orientado por domínio
8. Projete micro frontends
9. Orquestre os microsserviços

### Qual pilha tecnológica é comumente utilizada para microsserviços?

Abaixo você irá encontrar um diagrama mostrando a pilha tecnológica de microsserviços, tanto para fase de desenvolvimento como para produção.

<p>
  <img src="../images/microservice-tech.jpeg" />
</p>

▶️ 𝐏𝐫𝐞-𝐏𝐫𝐨𝐝𝐮𝐜𝐭𝐢𝐨𝐧

- Definir a API - Isso estabelece o contrato entre frontend e backend. Nós podemos utilizar Postman ou OpenAPI pra isso.
- Desenvolvimento - Node.js ou react são populares para desenvolvimento frontend, e java/python/go para desenvolvimento backend. Além disso, nós precisamos mudar as configurações no API Gateway de acordo com as definições da API.
- Integração Contínua - Junit e Jenkins para testes automatizados. O código é empacotado em uma imagem Docker e implantado como microsserviços.

▶️ 𝐏𝐫𝐨𝐝𝐮𝐜𝐭𝐢𝐨𝐧

- NGinx é uma escolha comum para distribuidor de carga. A Cloudflare providencia um CDN (Content Delivery Network).
- API Gateway - Nós podemos utilizar o spring boot para o gateway, e usar o Eureka/Zookeeper para descobrimento de serviços.
- Os microsserviços são implantados em clouds. Nós temos opções como AWS, Microsoft Azure ou Google GCP.
- Cache and Busca
- The microservices are deployed on clouds. We have options among AWS, Microsoft Azure, or Google GCP.
- Cache e Busca de Texto Completo - Redis é uma escolha comum para armazenamento em cache de pares chave-valor. Elasticsearch é utilizado para busca de texto completo.
- Comunicações - Para serviços se comunicarem um com o outro, podemos utilizar infraestrutura de mensagerias, como Kafka ou RPC (Chamada de Procedimento Remota, _Remote Procedure Call_).
- Persistencia - Podemos utilizar MySQL ou PostgreSQL para banco de dados relactionais e Amazon S3 para armazenamento de objeto. Também podemos utilizar Cassandra para armazenamento wide-column (coluna-larga) se necessário.
- Gerenciamento & Monitoramento - Para manusear tantos microsserviços, as ferramentas comuns incluem Prometheus, Elastic Stack e Kubernetes.

### Por quê Kafka é tão rápido

Houveram muitas decisões de design que contribuem para a performance do Kafka. Neste post, vamos focar em duas. Acreditamos que estas duas tenham o maior impacto.

<p>
  <img src="../images/why_is_kafka_fast.jpeg" />
</p>

1. A primeira é a dependência do Kafka em E/S (I/O) sequencial.
2. A segunda escolha de design que confere ao Kafka sua vantagem de desempenho é seu foco na eficiência: o princípio de cópia zero.

O diagrama ilustra como o dado transmitido entre produtor e consumidor e o que zero-copy significa.

- Passo 1.1 - 1.3: O Produtos escreve dado no disco
- Passo 2: O Consumidor lê dados sem zero-copy

  2.1 O dado é carregado do disco para o cache do SO

  2.2 O dado é copiado do cache do SO para a aplicação (o próprio Kafka)

  2.3 A aplicação kafka copia o dado para o buffer do socket

  2.4 O dado é copiado do buffer do socket para a placa de rede

  2.5 A placa de rede envia o dado para o consumidor

- Passo 3: Consumidor lê o dado com zero-copy

  3.1 O dado é carregado do disco ao cache do SO
  3.2 Cache do SO diretamente copia o dado da placa de rede com o comando sendfile()
  3.3 A placa de rede envia o dado para o consumidor

Zero-Copy é um atalho para salvar as multiplas copias entre contexto de usuário e contexto de kernel.

## Sistemas de Pagamento

### Como aprender sistemas de pagamento?

<p>
  <img src="../images/learn-payments.jpg" />
</p>

### Por que o cartão de crédito é chamado de "o produto mais lucrativo para os bancos"? Como que a VISA/Mastercard ganham dinheiro?

O diagrama abaixo mostra a economia do fluxo de pagamento com cartão de crédito.

<p>
  <img src="../images/how does visa makes money.jpg" style="width: 640px" />
</p>

1.&nbsp;&nbsp;O titular do cartão paga $100 a um comerciante para comprar um produto.

2.&nbsp;O comerciante se beneficia do uso do cartão de crédito com um volume de vendas mais alto e precisa compensar o emissor e a rede de cartões por fornecer o serviço de pagamento. O banco adquirente estabelece uma taxa com o comerciante, chamada "taxa de desconto do comerciante".

3 - 4. O banco adquirente retém $0,25 como a margem adquirente, e $1,75 é pago ao banco emissor como taxa de intercâmbio. A taxa de desconto do comerciante deve cobrir a taxa de intercâmbio.

A taxa de intercâmbio é estabelecida pela rede de cartões, pois seria menos eficiente para cada banco emissor negociar taxas com cada comerciante individualmente.

5.&nbsp;&nbsp;A rede de cartões estabelece as avaliações e taxas de rede com cada banco, que paga à rede de cartões por seus serviços a cada mês. Por exemplo, a VISA cobra uma avaliação de 0,11%, além de uma taxa de uso de $0,0195, para cada transação.

6.&nbsp;&nbsp;O titular do cartão paga ao banco emissor pelos seus serviços.

Por que o banco emissor precisa ser compensado?

- O emissor paga ao comerciante mesmo se o titular do cartão deixar de pagar ao emissor.
- O emissor paga ao comerciante antes mesmo de o titular do cartão pagar ao emissor.
- O emissor tem outros custos operacionais, incluindo a gestão de contas do cliente, emissão de extratos, detecção de fraudes, gestão de riscos, compensação & liquidação, entre outros.

### Como a VISA funciona quando nós passamos o cartão de crédito em uma loja?

<p>
  <img src="../images/visa_payment.jpeg" />
</p>

VISA, Mastercard e American Express atuam como redes de cartões para a compensação e liquidação de fundos. O banco adquirente e o banco emissor do cartão podem ser - e muitas vezes são - diferentes. Se os bancos fossem liquidar as transações individualmente, sem um intermediário, cada banco teria que liquidar as transações com todos os outros bancos. Isso seria bastante ineficiente.

O diagrama acima mostra o papel da VISA no processo de pagamento com cartão de crédito. Existem dois fluxos envolvidos. O fluxo de autorização ocorre quando o cliente passa o cartão de crédito. O fluxo de captura e liquidação ocorre quando o comerciante deseja receber o dinheiro no final do dia.

- Fluxo de autorização

Passo 0: O banco emissor do cartão emite cartões de crédito para seus clientes.

Passo 1: O titular do cartão deseja comprar um produto e passa o cartão de crédito no terminal de ponto de venda (POS, _Point of Sale_) na loja do comerciante.

Passo 2: O terminal POS envia a transação para o banco adquirente, que forneceu o terminal POS.

Passos 3 e 4: O banco adquirente envia a transação para a rede de cartões, também chamada de esquema de cartão. A rede de cartões envia a transação para o banco emissor para aprovação.

Passos 4.1, 4.2 e 4.3: O banco emissor reserva o dinheiro se a transação for aprovada. A aprovação ou rejeição é enviada de volta para o adquirente, assim como para o terminal POS.

- Fluxo de Captura e Liquidação

Passos 1 e 2: O comerciante deseja receber o dinheiro no final do dia, então eles acionam a "captura" no terminal POS. As transações são enviadas em lote para o adquirente. O adquirente envia o arquivo em lote com as transações para a rede de cartões.

Passo 3: A rede de cartões realiza a compensação para as transações coletadas de diferentes adquirentes e envia os arquivos de compensação para diferentes bancos emissores.

Passo 4: Os bancos emissores confirmam a correção dos arquivos de compensação e transferem dinheiro para os respectivos bancos adquirentes.

Passo 5: O banco adquirente, então, transfere dinheiro para o banco do comerciante.

Passo 4: A rede de cartões liquida as transações de diferentes bancos adquirentes. A liquidação é um processo no qual as transações de compensação mútua são compensadas, reduzindo assim o número total de transações.

No processo, a rede de cartões assume o encargo de falar com cada banco, em troca, recebendo as taxas de serviço.

### Série de Sistemas de Pagamento ao Redor do Mundo (Parte 1): Interface Unificada de Pagamentos (UPI, _Unified Payments Interface_) na Índia

O que é UPI? UPI é um sistema de pagamento instantâneo em tempo real desenvolvido pela National Payments Corporation of India.

Atualmente, representa 60% das transações digitais no varejo na Índia.

UPI = linguagem de marcação de pagamento + padrão para pagamentos interoperáveis

<p>
  <img src="../images/how-does-upi-work.png"  style="width: 600px" />
</p>

## DevOps

### DevOps vs. SRE vs. Platform Engineering. Qual a diferença?

Os conceitos de DevOps, SRE (Engenharia de Confiabilidade do Site, _Site Reliability Engineering_) e Platform Egineering (Engenharia de Plataforma) surgiram em momentos diferentes e foram desenvolvidos por diversos indivíduos e organizações.

<p>
  <img src="../images/devops-sre-platform.jpg" />
</p>

O conceito de DevOps foi introduzido em 2009 por Patrick Debois e Andrew Shafer a conferência Ágil (_Alige_ conference). Eles buscaram reduzir a lacuna entre o desenvolvimento de software e as operações, promovendo uma cultura colaborativa e responsabilidade compartilhada por todo o ciclo de vida do desenvolvimento de software.

O SRE, ou Engenharia de Confiabilidade de Sites, foi pioneirizado pelo Google no início dos anos 2000 para lidar com desafios operacionais no gerenciamento de sistemas complexos em grande escala. O Google desenvolveu práticas e ferramentas de SRE, como o sistema de gerenciamento de clusters Borg e o sistema de monitoramento Monarch, para aprimorar a confiabilidade e eficiência de seus serviços.

A Engenharia de Plataformas é um conceito mais recente, construindo sobre a base da engenharia SRE. As origens precisas da Engenharia de Plataformas são menos claras, mas geralmente é entendida como uma extensão das práticas DevOps e SRE, com foco em fornecer uma plataforma abrangente para o desenvolvimento de produtos que suporta toda a perspectiva do negócio.

Vale ressaltar que, embora esses conceitos tenham surgido em momentos diferentes, todos estão relacionados à tendência mais ampla de aprimorar a colaboração, automação e eficiência no desenvolvimento e operações de software.

### O que é k8s (Kubernetes)?

O K8s é um sistema de orquestração de contêineres. Ele é usado para implantação e gerenciamento de contêineres. Seu design é fortemente influenciado pelo sistema interno do Google chamado Borg.

<p>
  <img src="../images/k8s.jpeg" style="width: 680px" />
</p>

Um cluster K8s consistem em um conjunto de máquinas workers (trabalhadores, secundários) que rodam aplicações containerizadas. Todo cluster tem pelo menos um nó worker.

O(s) nó(s) worker(s) hospedam os Pods que são os componentes da carga de trabalho da aplicação. O plano de controle (_control plane_) gerencia os nós de trabalho e os Pods no cluster. Em ambientes de produção, o plano de controle geralmente é executado em vários computadores, e um cluster geralmente executa vários nós, proporcionando tolerância a falhas e alta disponibilidade.

- Componentem do Plano de Controle

1. Servidor da API

   O servidor da API se comunica com todos os componented do cluster k8s. Todas as operações nos pods são executadas por meio de comunicação com o servidor de API.

2. Escalonador (_Scheduler_)

   O escalonador (_scheduler_) observa cargas de trabalho nas pods e aloca cargas em pods recém-criados.

3. Gerenciador de Controladores

   O gerenciador de controladores executa os controladores, incluindo Node Controller, Job Controller, EndpointSlice Controller e ServiceAccount Controller.

4. Etcd

   etcd é um armazenamento de chave-valor usado como armazenamento principal do Kubernetes para todos os dados do cluster.

- Nós

1. Pods

   Um pod é um grupo de contêineres e é a menor unidade administrada pelo Kubernetes. Os Pods têm um único endereço IP aplicado a cada contêiner dentro do pod.

2. Kubelet

   Um agente que é executado em cada nó no cluster. Ele garante que os contêineres estejam em execução em um Pod.

3. Kube Proxy

   O Kube-proxy é um proxy de rede que é executado em cada nó do seu cluster. Ele direciona o tráfego que entra em um nó proveniente do serviço e encaminha solicitações de trabalho para os contêineres corretos.

### Docker vs. Kubernetes. Qual eu deveria usar?

<p>
  <img src="../images/docker-vs-k8s.jpg" style="width: 680px" />
</p>

O que é Docker ?

O Docker é uma plataforma de código aberto que permite empacotar, distribuir e executar aplicativos em contêineres isolados. Ele se concentra na containerização, fornecendo ambientes leves que encapsulam aplicativos e suas dependências.

O que é Kubernetes ?

O Kubernetes, frequentemente referido como K8s, é uma plataforma de orquestração de contêineres de código aberto. Ele fornece um framework para automatizar a implantação, escalabilidade e gerenciamento de aplicativos em contêineres em um cluster de nós.

Como eles diferem entre si ?

Docker: O Docker opera no nível individual do contêiner em um único sistema operacional hospedeiro.

É necessário gerenciar manualmente cada hospedeiro, e configurar redes, políticas de segurança e armazenamento para vários contêineres relacionados pode ser complexo.

Kubernetes: O Kubernetes opera no nível do cluster. Ele gerencia múltiplos aplicativos em contêineres em vários hospedeiros, proporcionando automação para tarefas como balanceamento de carga, escalabilidade e garantia do estado desejado dos aplicativos.

Em resumo, o Docker foca na containerização e na execução de contêineres em hospedeiros individuais, enquanto o Kubernetes se especializa em gerenciar e orquestrar contêineres em escala, em um cluster de hospedeiros.

### Como o Docker funciona?

O diagrama abaixo mostra a arquitetura do Docker e como ela funciona quando executamos os comandos "docker build", "docker pull" e "docker run".

<p>
  <img src="../images/docker.jpg" style="width: 680px" />
</p>

Há 3 components em uma arquitetura Docker:

- Cliente Docker

  O cliente docker fala com o Docker daemon.

- Hospedeiro Docker (_host_)

  O Docker daemon escuta por requisições de API do Docker e gerencia objetos do Docker, como imagens, contêineres, redes e volumes.

- Registro do Docker (_registry_)

  Um registro do Docker armazena imagens do Docker. O Docker Hub é um registro público que qualquer pessoa pode utilizar.

Vamos tomar o comando "docker run" como exemplo.

1. O Docker puxa a imagem do registro.
2. O Docker cria um novo container.
3. O Docker aloca um sistema de arquivos de leitura-escrita para o container.
4. O Docker cria uma interface de rede e conecta ao container para a rede padrão.
5. O Docker inicializa o container.

## GIT

### Como Comandos do Git funcionam

Para começar, é essencial identificar onde nosso código está armazenado. A suposição comum é que só existem duas localidades - uma em um servidor remoto como Github e a outra em nossa máquina local. No entanto, isso não é totalmente preciso. O Git mantém três armazenamentos locais na nossa máquina, o que significa que nosso código pode estar em quatro lugares:

<p>
  <img src="../images/git-commands.png" style="width: 600px" />
</p>

- Diretório Atual (_Working Directory_): onde editamos arquivos
- Área de Ensaio (_Staging Area_): um local temporário onde arquivos são mantidos para o próximo commit
- Repositório Local: contém o código que foi confirmado (_commitetd_)
- Repositório Remoto (_Remote_): o servidor remoto que armazena o código

A maioria dos comandos Git movimenta arquivos entre essas 4 localidades.

### Como o Git funciona?

O diagrama abaixo mostra o fluxo de trabalho do Git.

<p>
  <img src="../images/git-workflow.jpeg" style="width: 520px" />
</p>

Git é um sistema de controle de versões distribuído.

Todos os desenvolvedores mantém uma copia local do repositório principal e edita e confirma (comita) na cópia logal.

O _commit_ é muito rápido pois a operação não interage com o repositório remoto.

Se o repositorio remoto crasha, os arquivos podem ser recuperados pelas repositórios locais.

### Git merge vs. Git rebase

Quais as diferenças?

Quando nós **mesclamos (merge) alterações** de um branch (ramo) Git para outro, nós podemos usar ‘git merge’ ou ‘git rebase’. O diagrama abaixo mostra como os dois comandos funcionam.

<p>
  <img src="../images/git-merge-git-rebase.jpeg" style="width: 680px" />
</p>

**Git merge**

Isso cria um novo commit G' no branch principal. G' une as histórias tanto do branch principal quanto do branch de recurso (_resource branch_).

O merge do Git é **não destrutivo**. Nem o branch principal nem o branch de recurso são alterados.

**Git rebase**

Git rebase moves the feature branch histories to the head of the main branch. It creates new commits E’, F’, and G’ for each commit in the feature branch.

O rebase do Git move as histórias do feature branch para o topo do branch principal. Ele cria novos commits E', F' e G' para cada commit no branch de recurso.

A vantagem do rebase é que ele resulta em um **histórico de commits** linear.

O rebase pode ser perigoso se "a regra de ouro do git rebase" não for seguida.

**A Regra de Ouro do Git Rebase**

Nunca utilize ele em branches públicos!

## Serviços Cloud

### Um guia prático útil de diferentes serviços em nuvem (edição 2023).

<p>
  <img src="../images/cloud-compare.jpg" />
</p>

### O que é cloud native?

Abaixo é um diagrama mostrando a evoluçã de arquiteturas e processos desde 1980.

<p>
  <img src="../images/cloud-native.jpeg" style="width: 640px" />
</p>

Organizações podem construir e rodar aplicações escaláveis em clouds públicas, privadas e hibridas utilizando tecnologias cloud native.

Isso significa que aplicações são projetadas para aproveitar características da cloud, tornando-as resilientes à cargas fáceis de escalar.

Cloud native inclui 4 aspectos:

1. Processo de Desenvolvimento

   Isso evoluiu do modelo waterfall para o ágil e, posteriormente, para o DevOps.

2. Arquitetura de Aplicação

   A arquitetura foi de monolito para microsserviços. Cada serviço é projetado para ser pequeno, adaptativo para os recursos limitados em containers na cloud.

3. Implantação & Empacotamento

   As aplicações que eram implantados em servidores físicos. Então, por volta do ano 2000, as aplicações que não eram sensitivas à latência foram implantadas em servidores virtuais. Com aplicações cloud native, eles foram empacotados em imagens docker e implantados em containers.

4. Infraestrutura de Aplicação

   As aplicações são implantadas em massa em infraestrutura de nuvem em vez de servidores auto-hospedados.

## Ferramentas de produtividade para desenvolvedores

### Visualizar arquivos JSON

Arquivos JSON aninhados podem ser difíceis de ler.

**JsonCrack** gera diagramas de grafo a partir de arquivos JSON e os torna fáceis de ler.

Além disso, os diagramas gerados podem ser baixados como imagens.

<p>
  <img src="../images/json-cracker.jpeg" />
</p>

### Transformar código em diagramas de arquitetura de forma automática

<p>
  <img src="../images/diagrams_as_code.jpeg" style="width: 640px" />
</p>

O que ele faz?

- Desenha a arquitetura do sistema cloud em código python.
- Diagramas podem ser renderizados diretamente dentro de Jupyter Notebooks.
- Nenhuma ferramenta de design necessária.
- Suporta os seguintes fornecedores: AWS, Azure, GCP, Kubernetes, Alibaba Cloud, Oracle Cloud etc.

[Github repo](https://github.com/mingrammer/diagrams)

## Linux

### Sistema de Arquivos do Linux explicado

<p>
  <img src="../images/linux-file-systems.jpg" style="width: 680px" />
</p>

O sistema de arquivos do Linux costumava se assemelhar a uma cidade desorganizada onde indivíduos construíam suas casas onde queriam. No entando, em 1994, o Padrão de Hierarquia do Sistema de Arquivos (FHS, _Filesystem Hierarchy Standard_) foi introduzido para trazer ordem ao sistem de arquivos Linux.

Ao implementar um padrão como o FHS, o software pode garantir um layout consistente em várias distribuições do Linux. No entando, nem todas as distribuições do Linux aderem estritamente a esse padrão. Elas frequentemente incorporam elementos exclusivos ou atendem a requisitos específicos. Para se tornar proficiente nesse padrão você pode começar explorando. Utilize comandos como "cd" para navegação e "ls" para listar os conteúdos de um diretório. Imagine o sistema de arquivos como uma árvore, começando pela raiz (/). Com o tempo, isso se tornará algo natural para você, transformando-o num administrador Linux habilidoso.

### 18 Comandos Linux Mais Utilizados que Você Deve Conhecer

Comandos Linux são instruções para interagir com o sistema operacional. Eles ajudam a manusear arquivos, diretórios, processos e vários outros aspectos do sistema. Você precisa se tornar familiar com estes comands para navegar e manter um sistema baseado em Linux de forma eficiente e efetiva.

O diagrama abaixo mostra comandos Linux populares:

<p>
  <img src="../images/18 Most-Used Linux Commands You Should Know-01.jpeg" style="width: 680px" />
</p>

- ls - Lista arquivos e diretórios
- cd - Troca o diretório corrente
- mkdir - Cria um novo diretório
- rm - Remove arquivos e ou diretórios
- cp - Copia arquivos e ou diretórios
- mv - Move ou renomeia arquivos e ou diretórios
- chmod - Muda permissoes de arquivos e ou diretórios
- grep - Busca por um padrão em arquivos
- find - Busca por arquivos e diretódios
- tar - Marnipula arquivos tarball comprimidos
- vi - Edita arquivos usando editores de texto
- cat - Imprime o conteúdo de arquivos
- top - Imprime processos e utilização de recursos
- ps - Imprime informações de processos
- kill - Termina um processo por enviar um sinal
- du - Estima a utilização de espaço de arquivos
- ifconfig - Configura interfaces de rede
- ping - Testa conectividade via rede entre hospedeiros (hosts)

## Segurança

### Como o HTTPS funciona?

Protocolo de Transferência de Hipertexto Seguro (HTTPS, _Hypertext Transfer Protocol Secure_) é uma extensão do Protocolo de Transferência de Hipertexto (HTTP). HTTPS transmite dados encriptados utilizando Securança na Camada de de Transporte (TLC, _Transport Layer Security_). Se os dados forem sequestrados online, tudo que o sequestrador recebe é lixo binário.

<p>
  <img src="../images/https.jpg" />
</p>

Como os dados são encriptados e decriptados?

Passo 1 - O cliente (navegador) e o servidor estabelecem uma conexão TCP.

Passo 2 - O cliente envia um "client hello" para o servidor. A mensagem contém um conjunto de algoritmos de criptografia necessários (suites de cifras) e a última versão do TLS que ele pode suportar. O servidor responde com um "server hello" para que o navegador saiba se pode suportar os algoritmos e a versão do TLS.

O servidor então envia o certificado SSL para o cliente. O certificado contém a chave pública, hostname, data de expiração etc. O cliente valida o certificado.

Passo 3 - Após a validação do certificado SSL, o cliente gera a chave de sessão e encripta utilizando a chave pública. O servidor recebe a chave de sessão encriptada e a decripta com a chave privada.

Passo 4 - Agora que tanto o cliente como o servidor possuem a mesma chave de sessão (criptografia simétrica), os dados encriptados são transmitidos em um canal bi-direcional seguro.

Por que HTTPS troca para criptografia simétrica durante a transmissão de dados? Há duas razões principais:

1. Segurança: A criptografia simétrica funciona apenas de um lado. Isso significa que se o servidor tentar enviar dados criptografados de volta para o cliente, qualquer pessoa consegue decriptar os dados utilizando a chave pública.

1. Recursos do Servidor: A criptografia assimétrica adiciona uma carga matemática significativa. Não é adequada para transmissões de dados em sessões longas.

### Oauth 2.0 Explicado com Termos Simples.

OAuth 2.0 é um framework poderoso e seguro que permite diferentes aplicações interagirem uma com as outras de formas seguras em nome dos usuários, sem compartilhar credenciais sensíveis.

<p>
  <img src="../images/oAuth2.jpg" />
</p>

A entidade envolvida com OAuth são: o Usuário, o Servidor e o Provedor de Identidade (IDP, _Identity Provider_).

O que um Token OAuth pode fazer?

Quando você utiliza OAuth, você recebe um OAuth token que representa sua identidade e permissões. Esse token pode fazer algumas coisas importantes:

Single Sign-On (SSO): Com um token OAuth, você pode fazer login em vários serviços ou aplicativos com um único login, tornando a vida mais fácil e segura.

Autorização Entre Sistemas: O token OAuth permite que você compartilhe suas permissões ou direitos de acesso em vários sistemas, evitando que você precise fazer login separadamente em cada lugar.

Acesso ao Perfil do Usuário: Aplicativos com um token OAuth podem acessar partes específicas do seu perfil de usuário que você permite, mas eles não verão tudo.

Lembre-se, o OAuth 2.0 visa manter você e seus dados seguros, tornando suas experiências online contínuas e sem complicações em diferentes aplicativos e serviços.

### Principais 4 Formas de Mecanismos de Autenticação

<p>
  <img src="../images/top4-most-used-auth.jpg" />
</p>

1. Chaves SSH:

   Chaves criptográficas são utilizadas para acesso remoto de sistemas e servidores de forma segura

2. Tokens OAuth:

   Tokens que fornecem acesso limitado aos dados do usuário em aplicativos de terceiros.

3. Certificados SSL:

   Certificados digitais garantem comunicação segura e encriptada entre servidores de clientes

4. Credenciais:

   As informações de autenticação do usuário são utilizadas para verificar e conceder acesso a vários sistemas e serviços.

### Sessão, cookie, JWT, token, SSO, e OAuth 2.0 - o que são?

Esses termos estão todos relacionados à gestão da identidade do usuário. Quando você faz login em um site, declara quem é (identificação). Sua identidade é verificada (autenticação) e são concedidas as permissões necessárias (autorização). Muitas soluções foram propostas no passado, e a lista continua crescendo.

<p>
  <img src="../images/session.jpeg" />
</p>

De simples até complexo, aqui está a minha compreensão sobre a gestão de identidade do usuário:

- WWW-Authenticate é o método mais básico. O navegador solicita o nome de usuário e a senha. Devido à incapacidade de controlar o ciclo de vida do login, raramente é usado hoje em dia.

- Um controle mais refinado sobre o ciclo de vida do login é feito com session-cookie (cookie da sessão). O servidor mantém o armazenamento de sessão, e o navegador mantém o ID da sessão. Um cookie geralmente funciona apenas com navegadores e não é amigável para aplicativos móveis.

- Para lidar com o problema de compatibilidade, o token pode ser usado. O cliente envia o token para o servidor, e o servidor valida o token. A desvantagem é que o token precisa ser criptografado e descriptografado, o que pode ser demorado.

- JWT é uma maneira padrão de representar tokens. Essas informações podem ser verificadas e confiáveis porque são digitalmente assinadas. Como o JWT contém a assinatura, não é necessário salvar informações de sessão no lado do servidor.

- Ao usar SSO (entrada única, _single sign-on_), você pode fazer login apenas uma vez e acessar vários sites. Ele utiliza o CAS (serviço de autenticação central, _central authentication service_) para manter informações entre sites.

- Ao usar OAuth 2.0, você pode autorizar um site a acessar suas informações em outro site.

### Como armazenar senhas de forma segura em bancos de dados e como validá-las?

<p>
  <img src="../images/salt.jpg" style="width: 720px" />
</p>

**O que NÃO fazer**

- Armazenar senhas em texto puro não é uma boa ideia pois qualquer pessoa com acesso interno consegue vê-las.

- Armazenar diretamente os hashes de senhas não é suficiente, pois está sujeito a ataques de pré-computação, como tabelas arco-íris (_rainbow tables_).

- Para miticar ataques pré-computados, precisamos saltear as senhas.

**O que é sal**

De acordo com as diretrizes da OWASP, "um _salt_ (sal) é uma string única e gerada aleatoriamente que é adicionada a cada senha como parte do processo de hash".

**Como armazenar uma senha e sal?**

1. O resultado do hash é único para cada senha.
2. A senha pode ser armazenada no banco de dados usando o seguinte formato: hash(senha + salt).

**Como validar uma senha?**

Para validar uma senha, ela pode passar pelo seguinte processo:

1. Um cliente insere a senha.
2. O sistema recupera o salt correspondente do banco de dados.
3. O sistema concatena o salt à senha e realiza o hash. Vamos chamar o valor hash resultante de H1.
4. O sistema compara H1 e H2, onde H2 é o hash armazenado no banco de dados. Se forem iguais, a senha é válida.

### Explicando JSON Web Token (JWT) para uma criança de 10 anos de idade

<p>
  <img src="../images/jwt.jpg" />
</p>

Imagine que você tem uma caixa especial chamada JWT. Dentro dessa caixa, existem três partes: um cabeçalho, uma carga útil e uma assinatura.

O cabeçalho é como a etiqueta do lado de fora da caixa. Ele nos diz que tipo de caixa é e como ela está protegida. Geralmente, é escrito em um formato chamado JSON, que é apenas uma maneira de organizar informações usando chaves { } e dois-pontos : .

A carga útil é como a mensagem ou a informação real que você deseja enviar. Pode ser seu nome, idade ou qualquer outro dado que você queira compartilhar. Também é escrito no formato JSON, tornando-o fácil de entender e utilizar.

Agora, a assinatura é o que torna o JWT seguro. É como um selo especial que apenas o remetente sabe como criar. A assinatura é criada usando um código secreto, algo semelhante a uma senha. Essa assinatura garante que ninguém pode adulterar o conteúdo do JWT sem que o remetente saiba sobre a alteração.

Quando você deseja enviar o JWT para um servidor, coloca o cabeçalho, a carga útil e a assinatura dentro da caixa. Em seguida, você envia para o servidor. O servidor pode ler facilmente o cabeçalho e a carga útil para entender quem você é e o que deseja fazer.

### Como o Autenticador do Google (ou outros tipos de autenticadores de 2-fatores) funciona?

O Autenticador do Google é comumente utilizado para fazer login em contas quando autenticação de dois-fatores está habilitada. Como ele garante segurança?

O Autenticador doGoogle é um autenticador baseado em software que implementa um serviço de verificação de dois-fatores. O diagrama abaixo detalha.

<p>
  <img src="../images/google_authenticate.jpeg" />
</p>

Existem duas etapas envolvidas:

- Etapa 1 - O usuário habilita a verificação de duas etapas do Google.
- Etapa 2 - O usuário utiliza o autenticador para fazer login etc.

Vamos analisar essas etapas.

**Etapa 1**

Passo 1 and 2: Bob abre a página da web para habilitar a verificação em duas etapas. A interface solicita uma chave secreta. O serviço de autenticação gera a chave secreta para Bob e a armazena no banco de dados.

Passp 3: O serviço de autenticação retorna uma URI para a interface. A URI é composta por um emissor de chave, nome de usuário e chave secreta. A URI é exibida na forma de um código QR na página da web.

Passo 4: Bob então usa o Google Authenticator para escanear o código QR gerado. A chave secreta é armazenada no autenticador.

**Etapa 2**

Passos 1 e 2: Bob deseja fazer login em um site com a verificação em duas etapas do Google. Para isso, ele precisa da senha. A cada 30 segundos, o Google Authenticator gera uma senha de 6 dígitos usando o algoritmo TOTP (Senha de Uso Único Baseada em Tempo, _Time-based One Time Password_). Bob usa a senha para acessar o site.

Passos 3 e 4: A interface envia a senha que Bob insere para o backend para autenticação. O serviço de autenticação lê a chave secreta do banco de dados e gera uma senha de 6 dígitos usando o mesmo algoritmo TOTP que o cliente.

Passo 5: O serviço de autenticação compara as duas senhas geradas pelo cliente e pelo servidor, e retorna o resultado da comparação para a interface. Bob pode prosseguir com o processo de login apenas se as duas senhas coincidirem.

O mecanismo de autenticação é seguro?

- A chave secreta pode ser obtida por outras pessoas?

  Nós precisamos garantir que a chave secreta é transmitida via HTTPS. O cliente do autenticador e o banco de dados armazenam a chave secreta, e precisamos garantir que as chaves secretas sejam criptografadas.

- Os hackers podem adivinhar a senha de 6 dígitos?

  Não. A senha possui 6 dígitos, o que resulta em 1 milhão de combinações potenciais. Além disso, a senha muda a cada 30 segundos. Se os hackers quiserem adivinhar a senha em 30 segundos, precisariam inserir 30.000 combinações por segundo.

## Real World Case Studies

### Netflix's Tech Stack

This post is based on research from many Netflix engineering blogs and open-source projects. If you come across any inaccuracies, please feel free to inform us.

<p>
  <img src="../images/netflix tech stack.png" style="width: 680px" />
</p>

**Mobile and web**: Netflix has adopted Swift and Kotlin to build native mobile apps. For its web application, it uses React.

**Frontend/server communication**: Netflix uses GraphQL.

**Backend services**: Netflix relies on ZUUL, Eureka, the Spring Boot framework, and other technologies.

**Databases**: Netflix utilizes EV cache, Cassandra, CockroachDB, and other databases.

**Messaging/streaming**: Netflix employs Apache Kafka and Fink for messaging and streaming purposes.

**Video storage**: Netflix uses S3 and Open Connect for video storage.

**Data processing**: Netflix utilizes Flink and Spark for data processing, which is then visualized using Tableau. Redshift is used for processing structured data warehouse information.

**CI/CD**: Netflix employs various tools such as JIRA, Confluence, PagerDuty, Jenkins, Gradle, Chaos Monkey, Spinnaker, Atlas, and more for CI/CD processes.

### Twitter Architecture 2022

Yes, this is the real Twitter architecture. It is posted by Elon Musk and redrawn by us for better readability.

<p>
  <img src="../images/twitter-arch.jpeg" />
</p>

### Evolution of Airbnb’s microservice architecture over the past 15 years

Airbnb’s microservice architecture went through 3 main stages.

<p>
  <img src="../images/airbnb_arch.jpeg" />
</p>

Monolith (2008 - 2017)

Airbnb began as a simple marketplace for hosts and guests. This is built in a Ruby on Rails application - the monolith.

What’s the challenge?

- Confusing team ownership + unowned code
- Slow deployment

Microservices (2017 - 2020)

Microservice aims to solve those challenges. In the microservice architecture, key services include:

- Data fetching service
- Business logic data service
- Write workflow service
- UI aggregation service
- Each service had one owning team

What’s the challenge?

Hundreds of services and dependencies were difficult for humans to manage.

Micro + macroservices (2020 - present)

This is what Airbnb is working on now. The micro and macroservice hybrid model focuses on the unification of APIs.

### Monorepo vs. Microrepo.

Which is the best? Why do different companies choose different options?

<p>
  <img src="../images/monorepo-microrepo.jpg" />
</p>

Monorepo isn't new; Linux and Windows were both created using Monorepo. To improve scalability and build speed, Google developed its internal dedicated toolchain to scale it faster and strict coding quality standards to keep it consistent.

Amazon and Netflix are major ambassadors of the Microservice philosophy. This approach naturally separates the service code into separate repositories. It scales faster but can lead to governance pain points later on.

Within Monorepo, each service is a folder, and every folder has a BUILD config and OWNERS permission control. Every service member is responsible for their own folder.

On the other hand, in Microrepo, each service is responsible for its repository, with the build config and permissions typically set for the entire repository.

In Monorepo, dependencies are shared across the entire codebase regardless of your business, so when there's a version upgrade, every codebase upgrades their version.

In Microrepo, dependencies are controlled within each repository. Businesses choose when to upgrade their versions based on their own schedules.

Monorepo has a standard for check-ins. Google's code review process is famously known for setting a high bar, ensuring a coherent quality standard for Monorepo, regardless of the business.

Microrepo can either set its own standard or adopt a shared standard by incorporating the best practices. It can scale faster for business, but the code quality might be a bit different.
Google engineers built Bazel, and Meta built Buck. There are other open-source tools available, including Nx, Lerna, and others.

Over the years, Microrepo has had more supported tools, including Maven and Gradle for Java, NPM for NodeJS, and CMake for C/C++, among others.

### How will you design the Stack Overflow website?

If your answer is on-premise servers and monolith (on the bottom of the following image), you would likely fail the interview, but that's how it is built in reality!

<p>
  <img src="../images/stackoverflow.jpg" />
</p>

**What people think it should look like**

The interviewer is probably expecting something like the top portion of the picture.

- Microservice is used to decompose the system into small components.
- Each service has its own database. Use cache heavily.
- The service is sharded.
- The services talk to each other asynchronously through message queues.
- The service is implemented using Event Sourcing with CQRS.
- Showing off knowledge in distributed systems such as eventual consistency, CAP theorem, etc.

**What it actually is**

Stack Overflow serves all the traffic with only 9 on-premise web servers, and it’s on monolith! It has its own servers and does not run on the cloud.

This is contrary to all our popular beliefs these days.

### Why did Amazon Prime Video monitoring move from serverless to monolithic? How can it save 90% cost?

The diagram below shows the architecture comparison before and after the migration.

<p>
  <img src="../images/serverless-to-monolithic.jpeg" />
</p>

What is Amazon Prime Video Monitoring Service?

Prime Video service needs to monitor the quality of thousands of live streams. The monitoring tool automatically analyzes the streams in real time and identifies quality issues like block corruption, video freeze, and sync problems. This is an important process for customer satisfaction.

There are 3 steps: media converter, defect detector, and real-time notification.

- What is the problem with the old architecture?

  The old architecture was based on Amazon Lambda, which was good for building services quickly. However, it was not cost-effective when running the architecture at a high scale. The two most expensive operations are:

1. The orchestration workflow - AWS step functions charge users by state transitions and the orchestration performs multiple state transitions every second.

2. Data passing between distributed components - the intermediate data is stored in Amazon S3 so that the next stage can download. The download can be costly when the volume is high.

- Monolithic architecture saves 90% cost

  A monolithic architecture is designed to address the cost issues. There are still 3 components, but the media converter and defect detector are deployed in the same process, saving the cost of passing data over the network. Surprisingly, this approach to deployment architecture change led to 90% cost savings!

This is an interesting and unique case study because microservices have become a go-to and fashionable choice in the tech industry. It's good to see that we are having more discussions about evolving the architecture and having more honest discussions about its pros and cons. Decomposing components into distributed microservices comes with a cost.

- What did Amazon leaders say about this?

  Amazon CTO Werner Vogels: “Building **evolvable software systems** is a strategy, not a religion. And revisiting your architecture with an open mind is a must.”

Ex Amazon VP Sustainability Adrian Cockcroft: “The Prime Video team had followed a path I call **Serverless First**…I don’t advocate **Serverless Only**”.

### How does Disney Hotstar capture 5 Billion Emojis during a tournament?

<p>
  <img src="../images/hotstar_emojis.jpeg" style="width: 720px" />
</p>

1. Clients send emojis through standard HTTP requests. You can think of Golang Service as a typical Web Server. Golang is chosen because it supports concurrency well. Threads in Golang are lightweight.

2. Since the write volume is very high, Kafka (message queue) is used as a buffer.

3. Emoji data are aggregated by a streaming processing service called Spark. It aggregates data every 2 seconds, which is configurable. There is a trade-off to be made based on the interval. A shorter interval means emojis are delivered to other clients faster but it also means more computing resources are needed.

4. Aggregated data is written to another Kafka.

5. The PubSub consumers pull aggregated emoji data from Kafka.

6. Emojis are delivered to other clients in real-time through the PubSub infrastructure. The PubSub infrastructure is interesting. Hotstar considered the following protocols: Socketio, NATS, MQTT, and gRPC, and settled with MQTT.

A similar design is adopted by LinkedIn which streams a million likes/sec.

### How Discord Stores Trillions Of Messages

The diagram below shows the evolution of message storage at Discord:

<p>
  <img src="../images/discord-store-messages.jpg" />
</p>

MongoDB ➡️ Cassandra ➡️ ScyllaDB

In 2015, the first version of Discord was built on top of a single MongoDB replica. Around Nov 2015, MongoDB stored 100 million messages and the RAM couldn’t hold the data and index any longer. The latency became unpredictable. Message storage needs to be moved to another database. Cassandra was chosen.

In 2017, Discord had 12 Cassandra nodes and stored billions of messages.

At the beginning of 2022, it had 177 nodes with trillions of messages. At this point, latency was unpredictable, and maintenance operations became too expensive to run.

There are several reasons for the issue:

- Cassandra uses the LSM tree for the internal data structure. The reads are more expensive than the writes. There can be many concurrent reads on a server with hundreds of users, resulting in hotspots.
- Maintaining clusters, such as compacting SSTables, impacts performance.
- Garbage collection pauses would cause significant latency spikes

ScyllaDB is Cassandra compatible database written in C++. Discord redesigned its architecture to have a monolithic API, a data service written in Rust, and ScyllaDB-based storage.

The p99 read latency in ScyllaDB is 15ms compared to 40-125ms in Cassandra. The p99 write latency is 5ms compared to 5-70ms in Cassandra.

### How do video live streamings work on YouTube, TikTok live, or Twitch?

Live streaming differs from regular streaming because the video content is sent via the internet in real-time, usually with a latency of just a few seconds.

The diagram below explains what happens behind the scenes to make this possible.

<p>
  <img src="../images/live_streaming_updated.jpg" style="width: 640px" />
</p>

Step 1: The raw video data is captured by a microphone and camera. The data is sent to the server side.

Step 2: The video data is compressed and encoded. For example, the compressing algorithm separates the background and other video elements. After compression, the video is encoded to standards such as H.264. The size of the video data is much smaller after this step.

Step 3: The encoded data is divided into smaller segments, usually seconds in length, so it takes much less time to download or stream.

Step 4: The segmented data is sent to the streaming server. The streaming server needs to support different devices and network conditions. This is called ‘Adaptive Bitrate Streaming.’ This means we need to produce multiple files at different bitrates in steps 2 and 3.

Step 5: The live streaming data is pushed to edge servers supported by CDN (Content Delivery Network.) Millions of viewers can watch the video from an edge server nearby. CDN significantly lowers data transmission latency.

Step 6: The viewers’ devices decode and decompress the video data and play the video in a video player.

Steps 7 and 8: If the video needs to be stored for replay, the encoded data is sent to a storage server, and viewers can request a replay from it later.

Standard protocols for live streaming include:

- RTMP (Real-Time Messaging Protocol): This was originally developed by Macromedia to transmit data between a Flash player and a server. Now it is used for streaming video data over the internet. Note that video conferencing applications like Skype use RTC (Real-Time Communication) protocol for lower latency.
- HLS (HTTP Live Streaming): It requires the H.264 or H.265 encoding. Apple devices accept only HLS format.
- DASH (Dynamic Adaptive Streaming over HTTP): DASH does not support Apple devices.
- Both HLS and DASH support adaptive bitrate streaming.

## License

<p xmlns:cc="http://creativecommons.org/ns#" >This work is licensed under <a href="http://creativecommons.org/licenses/by-nc-nd/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">CC BY-NC-ND 4.0<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/nc.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/nd.svg?ref=chooser-v1"></a></p>