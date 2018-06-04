# APIs RESTful – Uma descrição acurada.

E aí, galera. 

Hoje, eu pensei que poderia escrever um post rápido para cobrir APIs RESTful, e o que elas são. A razão para este artigo é que eu tenho, em múltiplas ocasiões, encontrado desenvolvedores (e, na verdade, times inteiros) que entenderam errado mesmo a parte mais básica deste conceito. Isso causa um número de problemas. Primeiramente, se você não fundamentalmente entender RESTful APIs, você provavelmente vai passar por prolemas de integração desde o começo. Segundamente, infelizmente, se você estiver fazendo uma entrevista para um papel e não entendeu o que é uma API RESTful propriamente, você vai travar na entrevista.

### O que uma API RESTful não é (necessariamente)
- Uma palavra-chave para JSON API
- Uma API com funcionalidades obscuras.

### O que uma API RESTful é, e o que ele tem
- REST significa Transferência de Estado Representacional. RESTful é um adjetivo, então uma API RESTful é uma API que compreende os princípios de REST;
- O propósito do REST é garantir que APIs sejam fáceis de se entender em um nível universal;
- APIs RESTful terão endpois que representarão entidades;
- Estes endpoints respeitarão métodos HTTP (também referenciados como verbos) para representar as ações que você desejar responder;

### Okay, então explique para mim os verbos/métodos HTTP
- Requisições GET representam a leitura desta entidade/coleção da fonte de dados;
- Requisições POST representam a criação de uma entidade/coleção da fonte de dados;
- Requisições PUT atualizam (substituindo destrutivamente) a entidade da fonte de dados;
- Requisições PATCH atualizam (parcialmente) a entidade da fonte de dados;
- Requisições DELETE removem a entidade da fonte dedados;

### Como isso funciona na prática?
Vamos utilizar o exemplo de um provedor de pagamentos, você pode ter entidades, como:

- api/customer
- api-payment
- api/payment/paymentId/refund

Você sempre precisará de uma especificação, mas teóricamente você sabe que se você mandar um POST para endpoint/customer, você vai criar um, se você enviar um PATCH, você vai atualizá-lo parcialmente, se você neviar um POST para api/payment você irá criar um pagamento, para o qual você vai receber uma referência (ID), e se você mandar uma requisição POST para api/paymente/id-que-você-receb3u/refund, então você vai criar um retorno do pagamento que você especificou com o ID de pagamento.

### Então qual o objetivo disso?
A principal ideia por detrás de RESTful APIs, a mesma de outros padrões, como PSR-X, é unificar a forma como nós construímos APIs, então se eu fosse dizer, por exemplo, para uma organização com a qual eu vou estar integrando que "nós temos uma API RESTful com quem você pode integrar" eles sabem, com algum nível de certeza, quanto trabalho estará envolvido em trabalhar com ela – eles também não têm que ter um profundo entendimento do meu desenho local, arquitetura e etc, porque desenhos RESTful abstraem qualquer necessidade deste conhecimento.

### Em resumo
APIs RESTful são ótimas, outras APIs que não são RESTful também podem ser ótimas. Eu só queria ajudar a injetar algum entendimento sobre o tópico, embora, com certeza, há um monte de informação na internet sobre essa metodologia em particular. Se uma pessoa lê este artigo e ganha um entendimento real do que RESTful é, então ele já serviu o seu propósito.

### Edição: próximas letituras HATEOAS
[DarkTechnocrat](https://www.reddit.com/user/DarkTechnocrat) levantou um ponto válido no Reddit, para próximas leituras que forem além de um entendimento muito básico de REST, você provavelmente pode ler [HATEOAS](https://spring.io/understanding/HATEOAS) – em uma olhada rápida, este artigo no spring.io parece ser um bom lugar para começar.

