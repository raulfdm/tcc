# <a name="topo">SUMÁRIO</a>
1. [CONTEXTUALIZAÇÃO DA EMPRESA](#contextualizacao)
  1. [OBJETIVO GERAL](#obj-geral)
  1. [OBJETIVOS ESPECÍFICOS](#obj-espec)

1. [ANÁLISE DO NEGÓCIO](#analise-de-negocio)
  1. [ESCOPO DO NEGÓCIO](#escopo)
  1. [DIAGRAMA DE _USE CASE_ DE NEGÓCIO](#use-case-negocio)
    1. [Descrição dos Processos de Negócio](#descricao-dos-processos)
  1. [DESCRIÇÃO DOS STAKEHOLDERS](#stakeholders)
  1. [DEFINIÇÃO DO PROBLEMA](#definicao-problema)
  1. [DIAGRAMA DE CAUSA E EFEITO (ESPINHA DE PEIXE)](#ishikawa)
  1. [LISTA DE RESTRIÇÕES](#restricoes)

1. [ANÁLISE DE SISTEMA](#analise-sistema)
  1. [DESCRIÇÃO GERAL DO SISTEMA](#descricao-geral-sistema)
  1. [PROPOSTA DE DESENVOLVIMENTO DO SISTEMA](#proposta)
  1. [FRONTEIRA SISTÊMICA](#fronteira-sistemica)
  1. [_USE CASE_ DE SISTEMA](#use-case-sistema)
    1. [Descrição dos Processos de Sistema](#descricao-dos-processos-sistema)
  1. [DIAGRAMA DE CLASSE](#diagrama-classe)
  1. [DIAGRAMA DE SEQUÊNCIA](#diagrama-sequencia)

1. [MODELAGEM DO BANCO DE DADOS](#modelagem-db)
  1. [MODELO ENTIDADE RELACIONAMENTO (MER)](#modelagem-mer)
    1. [O Banco de dados Firebase Realtime Database](#modelagem-mer-firebase)
    1. [O Modelo Entidade-Relacionamento e o NoSQL](#modelagem-mer-nosql)
  1. [DIAGRAMA ENTIDADE RELACIONAMENTO (DER)](#modelagem-der)

1. [STORY BOARD](#story-board)

1. [CRONOGRAMA PARA O DESENVOLVIMENTO](#cronograma)

1. [REFERÊNCIAS BIBLIOGRÁFICAS](#referencias)


# <a name="contextualizacao">CONTEXTUALIZAÇÃO DA EMPRESA</a>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;A empresa alvo deste projeto possui apenas duas pessoas, uma comerciante autônoma, vendedora de roupas e acessórios que atua no ramo há 25 anos e sua filha que está iniciando no ramo de vendas. Por se tratar de uma microempresa, ambas cuidam de todas as áreas, desde as vendas, contas a pagar, contas a receber e até mesmo as compras de mercadorias. Seus clientes são pessoas físicas que as solicitam uma visita residencial para a apresentação das mercadorias trazidas de outras cidades, como por exemplo São José do Rio Preto/SP, Goiânia/GO, entre outras.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nas viagens de compra de mercadoria, quase todas as negociações são feitas através de cheques pré-datados e todo o controle de datas de pagamentos e valores são feitos através de anotações em cadernos que são trocados anualmente.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;No processo de venda, é feito uma apresentação de mercadorias ao cliente. No ato da venda, a vendedora cria uma ficha cadastral, onde são anotadas informações básicas para contato e identificação do cliente e informações gerais sobre as vendas realizadas, como a quantidade total da compra e as parcelas com suas respectivas datas de pagamento.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Diariamente, três informações são consultadas para iniciar o dia de trabalho. A primeira é identificar quais são os pagamentos a serem efetuados no dia. A segunda é levantar a relação de clientes que estão pendentes de pagamento para que então, seja feito contato e o recebimento. Por último, é analisar quais clientes que estão próximos de quitar suas dívidas e fazer contato para o agendamento de uma nova visita e venda.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Assim, o sistema deverá proporcionar um controle dos pagamentos e recebimentos, bem como exibir ao usuário todas as informações importantes para o início das atividades de forma automatizada, otimizando o tempo gasto nas tarefas manuais.

[menu↑](#topo)

## <a name="obj-geral">OBJETIVO GERAL</a>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;O objetivo deste projeto é criar um sistema de informação para uma empreendedora autônoma no seguimento de venda de roupas e acessórios.

[menu↑](#topo)

## <a name="obj-espec">OBJETIVOS ESPECÍFICOS</a>
Os objetivos específicos são:
* Controlar a compra de mercadorias;
* Manter um cadastro de todas clientes;
* Cadastrar pedidos de vendas;
* Controlar contas a receber;
* Controlar prospecção das vendas;
* Implementar no sistema o acesso por perfis de usuário
* Disparar *e-mail* list e mensagens para smartphones

[menu↑](#topo)

# <a name="analise-de-negocio">ANÁLISE DO NEGÓCIO</a>

##	<a name="escopo">ESCOPO DO NEGÓCIO</a>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;O trabalho é feito por duas pessoas. O (A) comerciante acompanha as tendências da moda através das mídias sociais, televisão, revistas e encartes enviados pelas lojas para obter as atualizações das novidades e potencial comercial para seu público alvo. Com essas referências em mente, o primeiro passo é a compra das mercadorias.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;O (A) vendedor (a) entra em contato com uma agência que realiza viagens para cidades que possuam um centro comercial atacadista e consulta as datas previstas para as viagens por cidades. Cada cidade possui um tipo específico de mercadorias, assim, caso o (a) vendedor (a) não tenha experiência com compras, ele pode consultar o representante da agência, que informará o destino que melhor atenderá suas necessidades e passar informações sobre condições de pagamento dos locais.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;No dia da viagem, o (a) vendedor (a) se dirige ao local onde o ônibus sairá e partem rumo a cidade destino. Chegado ao destino, (o) a vendedor (a) assiste desfiles de modas e consome a divulgação das mercadorias feitas por cada loja, afim de fazer uma breve apresentação de quais mercadorias estão disponíveis para compra. Na loja, a vendedora analisa as mercadorias e efetiva a compra das peças que lhe interessaram, no mínimo 6 (seis) ou mais peças, por se tratar de lojas atacadistas. É combinado com o (a) vendedor (a) da loja, o valor total, o desconto e a forma de pagamento, que podem ser à vista, cartão de crédito parcelado ou cheques pré-datados.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;As viagens têm duração de 1 ou 2 dias, variando conforme a agência e/ou destino escolhidos. No retorno, (o) a vendedor (a) organiza-se para fazer o controle e separação de toda mercadoria adquirida.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;O primeiro passo é a organização das mercadorias para facilitar a marcação de preços, separando as mercadorias em grupos definidos por loja ou por marca. Após a organização física, o (a) vendedor (a) anota peça a peça o tipo da mercadoria, por exemplo, calça, blusa, vestido, seu preço de custo e de venda em um caderno. A anotação do preço acontece tanto no caderno, quanto em sua etiqueta, para facilitar a visualização do mesmo na hora da venda. Após esse processo, as mercadorias são separadas por tamanho (P, M, G, etc.) e guardadas em sacolas.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;No processo seguinte, no mesmo caderno onde foram anotados os valores de cada mercadoria, é feita a somatória do valor total investido e do valor total a ser vendido. Caso as mercadorias tenham sido adquiridas por cheque pré-datado, é anotado o valor do cheque e a data a ser pago. Esses dados servirão de consulta para as contas a pagar por dia.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Terminado o processo de organização e separação das mercadorias, o (a) vendedor (a) entra em contato com a sua carteira de cliente, sempre priorizando os clientes que possuem maior credibilidade no histórico de pagamentos e compras. No contato, é informado que estão disponíveis novas mercadorias e caso o (a) cliente tenha interesse, é agendado a data e o local para que seja feita a apresentação.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Na data e hora combinada, o (a) vendedor (a) vai até o local escolhido pelo (a) cliente, que pode ser desde o local de trabalho ou sua própria casa, e apresenta as mercadorias de acordo com o tamanho do cliente. O (A) cliente assiste à apresentação e escolhe as peças que tem interesse em adquirir e a vendedora opina sobre como fazer combinações entre peças, combinação de cores, combinação do próprio estilo da pessoa com a roupa. O (A) cliente tem a possibilidade de experimentar a peça durante a visita.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;No fim da visita, o cliente informa a vendedora quais as mercadorias que deseja adquirir. Caso seja um cliente novo, a vendedora pega uma pasta com as fichas de todos os clientes e cria uma nova ficha que contém informações básicas para o contato, como o nome completo, telefones para contato, endereço. Caso seja um cliente já antigo, a vendedora procura a ficha deste cliente na pasta para fazer as anotações da compra. Em seguida, a vendedora soma o total e informa o cliente quais as condições disponíveis de pagamento. Essas, podem ser à vista ou à prazo (30/60/90 dias) no cheque ou na caderneta. Após o cliente escolher a forma de pagamento, é anotado em sua ficha as datas e o valor de cada parcela, junto com o valor total da compra.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Uma das condições mais usadas como condição de pagamento é o fiado. Esse método é baseado na confiança, ou seja, a cliente faz a compra, divide o valor total em no máximo 4 meses e informa o dia que poderá pagar a parcela. Na data informada, a vendedora entra em contato com a cliente para fazer o recebimento. O controle é todo feito através da ficha da cliente.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Logo, todos os dias pela manhã a vendedora consulta as fichas de cada cliente para verificar se há recebimentos a serem feitos naquele dia. Caso haja, é feito um contato com a mesma, que diz se a vendedora pode ou não fazer o recebimento. Caso a cliente não tenha dinheiro naquele dia, é agendado para uma nova data, substituindo a data anotada pela data informada pela cliente.

[menu↑](#topo)


## <a name="use-case-negocio">DIAGRAMA DE _USE CASE_ DE NEGÓCIO</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;O diagrama de _Use Case_ de negócio, tem como objetivo fornecer uma visão de como é o processo atual de trabalho. Na figura 1, temos a representação visual destes fluxos e suas interações com os atores.

Figura 1. *Use Case* de Negócio
![Use Case de negócio](https://github.com/raulfdm/tcc/blob/master/Files/img/use-case-negocio.png)
<br><br>Fonte: Autoria Própria

[menu↑](#topo)

### <a name="descricao-dos-processos">Descrição dos processos de negócio</a>

<table>
<caption>Quadro 1 - <i>Use Case</i> de Negócio: Agendar Viagem</caption>
  <tr>
  <td><i>Use Case</i> de Negócio:</td>
    <td>Agendar Viagem</td>
  </tr>
  <tr>
  <td>Ator(es):</td>
    <td>Agente de Viagem e Vendedor(a)</td>
  </tr>
  <tr>
  <td>Descrição:</td>
    <td>Neste processo, é agendado a viagem para compra das mercadorias.</td>
  </tr>
</table>
---
<table>
<caption>Quadro 2 - <i>Use Case</i> de Negócio: Comprar Mercadorias</caption>
  <tr>
  <td><i>Use Case</i> de Negócio:</td>
    <td>Comprar Mercadorias</td>
  </tr>
  <tr>
  <td>Ator(es):</td>
    <td>Fornecedor e Vendedor(a)</td>
  </tr>
  <tr>
  <td>Descrição:</td>
    <td>Neste processo, é feito a escolha e aquisição das mercadorias por lojas atacadistas.</td>
  </tr>
</table>
___
<table>
<caption>Quadro 3 - <i>Use Case</i> de Negócio: Organizar Mercadorias</caption>
  <tr>
  <td><i>Use Case</i> de Negócio:</td>
    <td>Organizar Mercadorias</td>
  </tr>
  <tr>
  <td>Ator(es):</td>
    <td>Vendedor(a)</td>
  </tr>
  <tr>
  <td>Descrição:</td>
    <td>Neste processo, é feita toda a organização das mercadorias adquiridas, as preparando para a venda.</td>
  </tr>
</table>
---
<table>
<caption>Quadro 4 - <i>Use Case</i> de Negócio: Anotar Preços nas Mercadorias</caption>
  <tr>
  <td><i>Use Case</i> de Negócio:</td>
    <td>Anotar Preços nas Mercadorias</td>
  </tr>
  <tr>
  <td>Ator(es):</td>
    <td>Vendedor(a)</td>
  </tr>
  <tr>
  <td>Descrição:</td>
    <td>Neste processo, é calculado e anotado o preço de venda de na etiqueta de cada mercadoria.</td>
  </tr>
</table>
---
<table>
<caption>Quadro 5 - <i>Use Case</i> de Negócio: Consultar Contas a Pagar</caption>
  <tr>
  <td><i>Use Case</i> de Negócio:</td>
    <td>Consultar Contas a Pagar</td>
  </tr>
  <tr>
  <td>Ator(es):</td>
    <td>Vendedor(a)</td>
  </tr>
  <tr>
  <td>Descrição:</td>
    <td>Neste processo, é consultado o caderno com as anotações de todos os pagamentos de cheques ou fornecedores que devem ser realizados.</td>
  </tr>
</table>
---
<table>
<caption>Quadro 6 - <i>Use Case</i> de Negócio: Pagar Contas</caption>
  <tr>
  <td><i>Use Case</i> de Negócio:</td>
    <td>Pagar Contas</td>
  </tr>
  <tr>
  <td>Ator(es):</td>
    <td>Vendedor(a)</td>
  </tr>
  <tr>
  <td>Descrição:</td>
    <td>Neste processo, é feito o pagamento dos cheques ou fornecedores.</td>
  </tr>
</table>
---
<table>
<caption>Quadro 7 - <i>Use Case</i> de Negócio: Consultar Contas a Receber</caption>
  <tr>
  <td><i>Use Case</i> de Negócio:</td>
    <td>Consultar Contas a Receber</td>
  </tr>
  <tr>
  <td>Ator(es):</td>
    <td>Vendedor(a)</td>
  </tr>
  <tr>
  <td>Descrição:</td>
    <td>Neste processo, é consultado o caderno com as fichas das clientes e verificado se há recebimentos a serem feitos no dia.</td>
  </tr>
</table>
---
<table>
<caption>Quadro 8 - <i>Use Case</i> de Negócio: Ligar para o Cliente</caption>
  <tr>
  <td><i>Use Case</i> de Negócio:</td>
    <td>Ligar para o Cliente</td>
  </tr>
  <tr>
  <td>Ator(es):</td>
    <td>Vendedor(a) e Cliente</td>
  </tr>
  <tr>
  <td>Descrição:</td>
    <td>Neste processo, é feito um contato para o agendamento de uma visita ao cliente para fazer o recebimento ou uma exibição/venda das mercadorias.</td>
  </tr>
</table>
---
 <table>
<caption>Quadro 9 - <i>Use Case</i> de Negócio: Ligar para o Cliente</caption>
  <tr>
  <td><i>Use Case</i> de Negócio:</td>
    <td>Ligar para o Cliente</td>
  </tr>
  <tr>
  <td>Ator(es):</td>
    <td>Vendedor(a) e Cliente</td>
  </tr>
  <tr>
  <td>Descrição:</td>
    <td>Neste processo, é feito um contato para o agendamento de uma visita ao cliente para fazer o recebimento ou uma exibição/venda das mercadorias.</td>
  </tr>
</table>
---
 <table>
<caption>Quadro 11 - <i>Use Case</i> de Negócio: Visitar Cliente</caption>
  <tr>
  <td><i>Use Case</i> de Negócio:</td>
    <td>Visitar Cliente</td>
  </tr>
  <tr>
  <td>Ator(es):</td>
    <td>Vendedor(a) e Cliente</td>
  </tr>
  <tr>
  <td>Descrição:</td>
    <td>Neste processo, o (a) vendedor(a) vai até o local escolhido pelo cliente na hora e data marcadas.</td>
  </tr>
</table>
---
<table>
<caption>Quadro 12 - <i>Use Case</i> de Negócio: Fazer Recebimento</caption>
  <tr>
  <td><i>Use Case</i> de Negócio:</td>
    <td>Fazer Recebimento</td>
  </tr>
  <tr>
  <td>Ator(es):</td>
    <td>Vendedor(a) e Cliente</td>
  </tr>
  <tr>
  <td>Descrição:</td>
    <td>Neste processo, o(a) vendedor(a) recolhe o dinheiro do pagamento pendente por parte do cliente e da baixa na ficha.</td>
  </tr>
</table>
---
<table>
<caption>Quadro 13 - <i>Use Case</i> de Negócio: Dar baixa do pagatamento na ficha do cliente</caption>
  <tr>
  <td><i>Use Case</i> de Negócio:</td>
    <td>Dar baixa do pagatamento na ficha do cliente</td>
  </tr>
  <tr>
  <td>Ator(es):</td>
    <td>Vendedor(a) e Cliente</td>
  </tr>
  <tr>
  <td>Descrição:</td>
    <td>Neste processo, o(a) vendedor(a) marca um "ok" ao lado da parcela que o cliente está pagando.</td>
  </tr>
</table>
---
<table>
<caption>Quadro 14 - <i>Use Case</i> de Negócio: Mostrar Mercadorias</caption>
  <tr>
  <td><i>Use Case</i> de Negócio:</td>
    <td>Mostrar Mercadorias</td>
  </tr>
  <tr>
  <td>Ator(es):</td>
    <td>Vendedor(a) e Cliente</td>
  </tr>
  <tr>
  <td>Descrição:</td>
    <td>Neste processo, o(a) vendedor(a) apresenta as mercadorias que sejam compatíveis com o tamanho do cliente, fazendo as cobinções e auxiliando na experimentação das peças.</td>
  </tr>
</table>
---
<table>
<caption>Quadro 15 - <i>Use Case</i> de Negócio: Realizar Venda</caption>
  <tr>
  <td><i>Use Case</i> de Negócio:</td>
    <td>Realizar Venda</td>
  </tr>
  <tr>
  <td>Ator(es):</td>
    <td>Vendedor(a) e Cliente</td>
  </tr>
  <tr>
  <td>Descrição:</td>
    <td>Neste processo, o(a) cliente o(a) vendedor(a) quais as peças que ele vai comprar e o(a) vendedor(a) começa a organizar e guardar as mercadorias de volta na sacola.</td>
  </tr>
</table>
---
<table>
<caption>Quadro 16 - <i>Use Case</i> de Negócio: Anotar Venda na Ficha do Cliente</caption>
  <tr>
  <td><i>Use Case</i> de Negócio:</td>
    <td>Anotar Venda na Ficha do Cliente</td>
  </tr>
  <tr>
  <td>Ator(es):</td>
    <td>Vendedor(a) e Cliente</td>
  </tr>
  <tr>
  <td>Descrição:</td>
    <td>Neste processo, o(a) cliente informa o(a) vendedor(a) qual a condição de pagamento que vai querer e o(a) vendedor(a) anota na ficha do(a) cliente o valor da parcela e as datas para o recebimento.</td>
  </tr>
</table>

[menu↑](#topo)

## <a name="stakeholders">DESCRIÇÃO DOS <i>STAKEHOLDERS</i> </a>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;O termo *Stackholder* se refere a uma pessoa ou grupo de pessoas interessadas  em uma empresa, negócio ou indústria. Assim, o *Stakeholder* da empresa é a própria fundadora. 

[menu↑](#topo)

## <a name="definicao-problema"> DEFINIÇÃO DO PROBLEMA</a>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Baseado no escopo de negócio, pode-se afirmar que o problema é a ineficiência no controle de todas as atividades pertinentes ao trabalho do (a) comerciante, atualmente serem feitas em papéis e caderno. Essa atitude apesar de ter sido adotada há muito tempo, possibilita as chances de alguma falha no processo acontecer, como por exemplo perda de dados de clientes ou de pagamentos a serem feitos, e também diminui de forma significativa a capacidade de analisar precisamente o histórico de venda para tomadas de decisão.


[menu↑](#topo)

## <a name="ishikawa">DIAGRAMA DE CAUSA E EFEITO (ESPINHA DE PEIXE)</a>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;A figura 2, mostra o diagrama de Ishikawa (Causa e Efeito) do negócio. Nele, temos como ponto central a dificuldade no gerenciamento das vendas e os problemas causadores de tal.
O ambiente se trata do meio ambiente do dia-a-dia de trabalho da vendedora. Nela, é possível notar que a mesma trabalha a maior parte do tempo no carro, ou seja, se locomovendo para o local de venda escolhido pela cliente.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;O método mostra as metodologias de trabalho escolhidas pela vendedora no processo atual, onde os cálculos de contas a pagar, receber, dos pedidos de venda, pedidos de compra e todo o fluxo restante do processo, é anotado em papeis e cadernos de forma manual. O que proporciona uma dificuldade na manutenção e organização dos documentos.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;No problema relacionado a maquinário, é exibido ao difícil acesso à tecnologia por parte da vendedora, na qual não possui um tablet nem um computador de mesa nem notebook para fazer seus controles. Associado a esse fator, também temos a pouca familiaridade da mesma com esse tipo de tecnologia.

Figura 2. Diagrama de Causa e Efeito
![Diagrama de causa e efeito (Ishikawa)](https://github.com/raulfdm/tcc/blob/master/Files/img/diagrama-ishikawa.png)
<br>Fonte: Autoria Própria 

[menu↑](#topo)

## <a name="restricoes">LISTA DE RESTRIÇÕES</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;A lista de restrições tem como objetivo fornecer informações sobre os requisitos gerais  para  o  desenvolvimento  do  sistema.  O  quadro  15  tem  como  objetivo  prover essa visão.

Quadro 15 - Lista de Restrições

|   Restrição   | Descrição     | Motivo
| :-----------: |:-------------:|:-------------:| 
| Linguagem de Programação - <i>Front-end</i> | Javascript, HTML5, CSS3, React | O React foi escolhido pela alta performance e capacidade de componentização de elementos. Por ele ser apenas uma biblioteca, é possível usá-lo em várias tecnologias, logo, caso haja mudança na tecnologia futuramente, o código poderá ser reutilizado. JavaScript, HTML5 e CSS3 são linguagens web, as tornando fundamentais para a realização do projeto.| 
| <i>Back-end</i> | Firebase| O Firebase foi escolhido pois ele fornece uma abstração da implementação do servidor, ou seja, ele oferece um SGBD não relacional, autenticação, armazenagem de arquivos através de serviços web e na nuvem. Seu uso reduzirá eliminará a necessidade de desenvolver um serviço na parte do servidor.|
| Servidor Web      |     Hospedagem LocaWeb  | Foi escolhido a Locaweb pela credibilidade da empresa e pelo valor de serviço prestado.|
| SGBD  |  NoSQL (Firebase) | Este é fornecido pelo próprio firebase.|

[menu↑](#topo)

# <a name="analise-sistema">ANÁLISE DE SISTEMA</a>

## <a name="descricao-geral-sistema">DESCRIÇÃO GERAL DO SISTEMA</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;O objetivo do sistema é oferecer ao vendedor e microempresário a possibilidade de ter  um  controle  mais  preciso  de  todo  o  seu  fluxo  de  trabalho  e  também  fornecer informações  que  facilitem  na  tomada  de  decisão.  Em  linhas  gerais,  a  proposta  é extinguir  o  uso  de  anotações  manuais  em  papel,  e  trabalhar com  as  informações inseridas de forma inteligente.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;O  sistema  terá  um  cadastro  de  clientes  e  fornecedores  com  as  informações essenciais de cada um. Também terá um cadastro de pedido de compra, onde será informado o fornecedor, as mercadorias, o preço de custo e a porcentagem na qual será usada para projetar automaticamente o preço de venda. O produto poderá  ser cadastrado  tanto  pela  tela  de  pedido  de  compra,  quanto  pela tela  de  produto, devendo ser inseridas informações inerentes ao mesmo. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Também deverá  possuir  um  cadastro  de  pedidos  de  venda,  onde  será selecionado  a  qual  cliente  a  venda  se  refere,  selecionar a  mercadoria  que  está sendo  vendida,  calculando  automaticamente  o  preço  total,  de  acordo  com  o  valor estabelecido no pedido de compra, possibilitar a seleção da forma de pagamento e com  isso,  definir  as  datas  e  valores  de  pagamentos.  Esses  valores  deverão  ser salvos individualmente para cada cliente em sua carteira. Cada  cliente  deverá  ter  uma  carteira  digital,  onde  poderá  ser  definido  um limite  de  crédito  para  o  cliente,  bem  como  informar  o  histórico  de  compras  e pagamentos efetuados ou pendentes do cliente.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;O sistema fornecerá relatórios que informarão ao vendedor as contas à pagar e à  receber  do  dia.  Também  deverá  possuir  uma  agenda  onde será  possível  ver essas  mesmas  informações,  mas,  em  formato  de  calendário.  Além  disso,  deverá gerar  um  relatório  de  vendas  por  semana,  mês  ou  ano,  dando  a  possibilidade  de comparar os meses e de venda e os mesmos períodos em diferentes anos. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;O  sistema  fará  também  a  emissão  de  relatório  de  inadimplência  e  atrasos, mostrando quais os clientes devedores de forma ranqueada (maior para o menor ou menor  para  o  maior),  bem  como  exibir  o  valor  total  da  receita  pendente  de recebimento.

[menu↑](#topo)

## <a name="proposta">PROPOSTA DE DESENVOLVIMENTO DO SISTEMA</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;A proposta é desenvolver o sistema Web, baseado nas tecnologias React. O React é um framework, desenvolvido pelo time de desenvolvimento do Facebook com o intuito de componentizar aplicações web. Seu desenvolvimento é feito através da linguagem de programação JavaScript (JS), junto com o padrão Web, HTML (Hypertext Markup Language) para marcação e estruturação das informações e CSS (Cascading Style Sheet) para dar estilo aos elementos.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;O sistema será pensado utilizando o conceito de PWA (Progressive Web Apps), ou seja, uma aplicação web, mas feita pensando em dispositivos móveis (smartphones e tablets), na qual gera uma experiência ao usuário de ao abrir o site, ter a sensação de utilizar um app nativo.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;No que se refere à estrutura de servidor e banco de dados, será utilizado o serviço do Google chamado Firebase. A proposta do Firebase é fornecer um back-end como serviço (Back-end as a Service - BaaS), ou seja, eles fornecem um servidor preparado com banco de dados, serviço de armazenamento de arquivos e autenticação, tudo através de API Rest (Representation State Transfer), que, utiliza o protocolo HTTP (Hypertext Transfer Protocol) para fazer operações como obtenção, inserção, alteração e deleção de dados, usando objetos JSON (JavaScript Object Notation).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;O sistema de banco de dados utilizado pelo Firebase é um banco de dados NoSQL (Not Only Structure Query Language), ou seja, não relacional. Bancos de dados não relacionais são baseados apenas em documentos, e com isso, não possuem relacionamento entre os documentos, tão pouco validações de chaves primarias ou estrangeiras. Assim, o foco deste tipo de banco de dados fica em escalabilidade e o armazenamento de grandes massas de dados. Logo, uma vez que esses documentos estão em formato de objetos JavaScript o custo de armazenagem de dados cai consideravelmente. Com esse comportamento, toda a responsabilidade da integridade dos dados para o banco de dados fica por conta da aplicação que o utiliza.

[menu↑](#topo)

## <a name="fronteira-sistemica">FRONTEIRA SISTÊMICA</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Na figura abaixo, é exibido a interação dos atores com o sistema, onde, esse será acessado tanto pelo vendedor (a), quanto pelo seu cliente. Todas as consultas de dados e autenticação serão feitas por um sistema paralelo ao sistema, o Firebase.

Figura 3 - Fronteira Sistêmica
<br>![Fronteira Sistêmica](https://github.com/raulfdm/tcc/blob/master/Files/img/fronteira-sistemica.png)
<br>Fonte: Autoria Própria

[menu↑](#topo)

## <a name="use-case-sistema">_USE CASE_ DE SISTEMA</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;A figura 4 exibe o _Use Case_ (Caso de Uso) de Sistema, no qual estão exibidas a proposta de interação entre os atores e os fluxos das principais operações.

Figura 4 - Use Case de Sistema
![Use Case de Sistema](https://github.com/raulfdm/tcc/blob/master/Files/img/use-case-sistema.png)
<br>Fonte: Autoria Própria

[menu↑](#topo)

### <a name="descricao-dos-processos-sistema">Descrição dos Processos de Sistema</a>

<table>
<caption>Quadro 17 - Use Case de Sistema: Gerar Pedido de Venda</caption>
  <tr>
  <td><i>Use Case</i> de Sistema:</td>
    <td>Cadastrar Venda</td>
  </tr>
  <tr>
  <td>Ator(es):</td>
    <td>Vendedor(a)</td>
  </tr>
  <tr>
  <td>Descrição:</td>
    <td>Nessa tela do sistema, o vendedor(a) poderá cadastrar um pedido de venda, informando a qual cliente que se destina, as mercadorias, quantidades, valores, somatório do total e a forma de pagamento. Caso seja parcelado, o sistema informará quais as datas de pagamento.</td>
  </tr>
</table>
---
<table>
<caption>Quadro 18 - <i>Use Case</i> de Sistema: Gerar Pedido de Compra</caption>
  <tr>
  <td><i>Use Case</i> de Sistema:</td>
    <td>Cadastrar Compra</td>
  </tr>
  <tr>
  <td>Ator(es):</td>
    <td>Vendedor(a)</td>
  </tr>
  <tr>
  <td>Descrição:</td>
    <td>Nesta tela, o vendedor(a) poderá cadastrar um pedido de compra, selecionando de qual fornecedor(loja) aquela compra se fere, a data da compra, o valor, a forma e condições de pagamento, os produtos e a margem de lucro que seja calculada em cima de cada produto.</td>
  </tr>
</table>
---
<table>
<caption>Quadro 19 - <i>Use Case</i> de Sistema: Cadastrar Fornecedor</caption>
  <tr>
  <td><i>Use Case</i> de Sistema:</td>
    <td>Cadastrar Forcedor</td>
  </tr>
  <tr>
  <td>Ator(es):</td>
    <td>Vendedor(a)</td>
  </tr>
  <tr>
  <td>Descrição:</td>
    <td>Nesta tela, o vendedor(a) poderá cadastrar o forcedor, informando todas as informações básicas do mesmo.</td>
  </tr>
</table>
---
<table>
<caption>Quadro 20 - <i>Use Case</i> de Sistema: Cadastrar Cliente</caption>
  <tr>
  <td><i>Use Case</i> de Sistema:</td>
    <td>Cadastrar Cliente</td>
  </tr>
  <tr>
  <td>Ator(es):</td>
    <td>Vendedor(a)</td>
  </tr>
  <tr>
  <td>Descrição:</td>
    <td>Nesta tela, o(a) vendedor(a) poderá cadastrar o cliente com as informações básicas e essências para contato e cobrança.</td>
  </tr>
</table>
---
<table>
<caption>Quadro 21 - <i>Use Case</i> de Sistema: Cadastrar Produto</caption>
  <tr>
  <td><i>Use Case</i> de Sistema:</td>
    <td>Cadastrar Produto</td>
  </tr>
  <tr>
  <td>Ator(es):</td>
    <td>Vendedor(a)</td>
  </tr>
  <tr>
  <td>Descrição:</td>
    <td>Nesta tela, o(a) vendedor(a) poderá cadastrar o produto, informando qual seu fornecedor e as informações que o qualifiquem.</td>
  </tr>
</table>
---
<table>
<caption>Quadro 22 - <i>Use Case</i> de Sistema: Consultar Pedidos de Compra</caption>
  <tr>
  <td><i>Use Case</i> de Sistema:</td>
    <td>Consultar Pedidos de Compra</td>
  </tr>
  <tr>
  <td>Ator(es):</td>
    <td>Vendedor(a)</td>
  </tr>
  <tr>
  <td>Descrição:</td>
    <td>Nesta tela, o(a) vendedor(a) poderá consultar todos os pedidos de compra filtrando por fornecedor ou período.</td>
  </tr>
</table>
---
<table>
<caption>Quadro 23 - <i>Use Case</i> de Sistema: Consultar Pedidos de Venda</caption>
  <tr>
  <td><i>Use Case</i> de Sistema:</td>
    <td>Consultar Pedidos de Venda</td>
  </tr>
  <tr>
  <td>Ator(es):</td>
    <td>Vendedor(a)</td>
  </tr>
  <tr>
  <td>Descrição:</td>
    <td>Nesta tela, o(a) vendedor(a) poderá consultar todos os pedidos de venda, filtrando por cliente ou período.</td>
  </tr>
</table>
---
<table>
<caption>Quadro 24 - <i>Use Case</i> de Sistema: Consultar Relatórios</caption>
  <tr>
  <td><i>Use Case</i> de Sistema:</td>
    <td>Consultar Relatórios</td>
  </tr>
  <tr>
  <td>Ator(es):</td>
    <td>Vendedor(a)</td>
  </tr>
  <tr>
  <td>Descrição:</td>
    <td>Nesta tela, o(a) vendedor(a) poderá retirar os relatórios analíticos e detalhado da sua operação.</td>
  </tr>
</table>
---
<table>
<caption>Quadro 25 - <i>Use Case</i> de Sistema: Consultar Carteira Digital</caption>
  <tr>
  <td><i>Use Case</i> de Sistema:</td>
    <td>Consultar Carteira Digital</td>
  </tr>
  <tr>
  <td>Ator(es):</td>
    <td>Vendedor(a) e Cliente</td>
  </tr>
  <tr>
  <td>Descrição:</td>
    <td>Esta tela, poderá ser acessada tanto pelo(a) vendedor(a), quanto pelo cliente. Nela, será exibida as informações do cliente, como suas informações cadastrais. Também será exibida um histórico de pagamentos e compras, bem como os débitos pendentes.</td>
  </tr>
</table>
---
<table>
<caption>Quadro 26 - <i>Use Case</i> de Sistema: Autenticar no Sistema</caption>
  <tr>
  <td><i>Use Case</i> de Sistema:</td>
    <td>Autenticar no Sistema</td>
  </tr>
  <tr>
  <td>Ator(es):</td>
    <td>Vendedor(a) e Cliente</td>
  </tr>
  <tr>
  <td>Descrição:</td>
    <td>Para ter acesso à todas as informações do sistema, tanto o(a) vendedor(a), quanto o(a) cliente, farão uma autenticação no sistema. Essa, será disparada para o servidor da google e retornará autorizando ou não a entrada do usuário.</td>
  </tr>
</table>

---

[menu↑](#topo)

## <a name="diagrama-classe">DIAGRAMA DE CLASSE</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;O diagrama de classe tem como objetivo fornecer uma visão macro das principais classes do sistema e como elas se relacionam. A figura 5, mostra a estrutura básica das classes do sistema, desenhados especialmente para a linguagem de programação que será utilizada no desenvolvimento do sistema, o JavaScript.

Figura 5 - Diagrama de Classe
![Diagrama de Classe](https://github.com/raulfdm/tcc/blob/master/Files/img/diagrama-classe.png)
<br>Fonte: Autoria Própria

[menu↑](#topo)

## <a name="diagrama-sequencia">DIAGRAMA DE SEQUÊNCIA</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;O diagrama de sequência tem como objetivo, exemplificar o trajeto de ações das principais interações do usuário com o sistema.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Na figura 6, é apresentado o fluxo da tela de consulta de pedidos. Inicialmente o usuário acessará o menu de pedidos e poderá escolher entre Pedidos de Compra e o Pedido de Venda.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Caso ele opte por pedido de Compra, ele selecionará a opção e será aberta uma tela com os pedidos de compra disponíveis dos últimos 15 dias. Ele terá uma opção de filtro de fornecedor, onde exibirá uma lista carregada com todos já cadastrados no sistema e ele poderá selecionar por exibir pedidos apenas de um fornecedor específico. Caso seja filtrado o fornecedor, o sistema fará uma busca no Firebase, que devolverá uma relação de pedidos cadastrados para o fornecedor em questão para os últimos 15 dias.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Caso ele escolha a tela Pedido de Venda, será exibido uma relação dos pedidos dos últimos 15 dias em ordem decrescente de data de todos os clientes e a opção de filtrar pedidos de um cliente em específico. Caso ele opte por realizar o filtro, o sistema fará uma consulta no Firebase e o mesmo retornará uma lista de todos os pedidos do cliente para os últimos 15 dias.

Figura 6 - Diagrama de Sequência: Consultar Pedidos
![Figura 6 - Diagrama de Sequência: Consultar Pedidos](https://github.com/raulfdm/tcc/blob/master/Files/img/diagrama-sequencia/consulta-pedidos.png)
<br>Fonte: Autoria Própria

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Na figura 7, está representado o fluxo da carteira digital, onde, poderá ser acessada tanto pelo cliente dono da carteira, quanto pelo (a) vendedor (a).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;No caso do cliente, não haverá a opção de filtrar clientes, assim, será exibida todas as informações referentes ao seu histórico de compra, de pagamento, seu saldo atual e gráficos de consumo por período.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Quando o usuário do sistema for vendedor (a), ao acessar a tela, o sistema acessará o Firebase e buscará a relação de todos os clientes já cadastrados no sistema e será fornecido um filtro com essa relação. Quando o usuário selecionar o cliente, o sistema buscará no Firebase as informações desse cliente, como informações cadastrais, histórico de compra, histórico de pagamento e exibirá em painéis divididos e gráficos dinâmicos essas informações.

Figura 7 - Diagrama de Sequência: Consultar Carteira
![Figura 7 - Diagrama de Sequência: Consultar Carteira](https://)
<br>Fonte: Autoria Própria

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Na figura 8, é exibido o filtro do fluxo de efetivação de uma conta pendente de pagamento no sistema. O usuário (vendedor (a)) acessará a tela de contas à pagar, onde o sistema fará uma consulta no Firebase e retornará a lista das contas pendentes de pagamento do último mês em ordem crescente de vencimento. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;O usuário poderá filtrar por uma conta específica, e somente essa será exibida no grid. Ao selecionar o menu de administração, o usuário confirmará o valor e o dia que a conta foi paga. Nesse momento, será enviado as informações para o Firebase, que desenvolverá uma mensagem de erro ou sucesso e esse pagamento passa a ter a classificação de PAGO no sistema.

Figura 8 - Diagrama de Sequência: Efetivar Contas à Pagar
![Figura 8 - Diagrama de Sequência: Efetivar Contas à Pagar](https://github.com/raulfdm/tcc/blob/master/Files/img/diagrama-sequencia/consultar-carteira.png)
<br>Fonte: Autoria Própria

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Na figura 9, é exibido o filtro do fluxo de efetivação de uma conta pendente de recebimento no sistema. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;O usuário (vendedor (a)) acessará a tela de contas à receber, onde o sistema fará uma consulta no Firebase e retornará a lista das contas pendentes de recebimento do último mês em ordem crescente de vencimento e por cliente. Ele também poderá filtrar por uma conta específica, e somente essa será exibida no grid. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Ao selecionar o menu de administração da conta, o usuário confirmará o valor e o dia que a conta foi recebida. Nesse momento, será enviado as informações para o Firebase, que devolverá uma mensagem de erro ou sucesso e, caso sucesso, esse recebimento passa a ter a classificação de PAGO no sistema.

Figura 9 - Diagrama de Sequência: Efetivar Recebimento
![Figura 9 - Diagrama de Sequência: Efetivar Recebimento](https://github.com/raulfdm/tcc/blob/master/Files/img/diagrama-sequencia/efetivar-recebimento.png)
<br>Fonte: Autoria Própria

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Na figura 10, é possível observar o fluxo de Login no sistema, onde, estará disponível tanto para o Cliente, quanto para o vendedor.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;O usuário acessará a tela de Login digitará suas credenciais. O sistema pegará essas informações e consultará no Firebase se as mesmas são válidas.
Caso dê sucesso, o usuário será redirecionado para a tela de home (Dashboard) no sistema. Caso dê erro, o usuário receberá uma mensagem informando que as credenciais incorretas e o mesmo tentará fazer _Login_ novamente.

Figura 10 - Diagrama de Sequência: Login no Sistema
![Figura 10 - Diagrama de Sequência: Login no Sistema](https://github.com/raulfdm/tcc/blob/master/Files/img/diagrama-sequencia/login.png)
<br>Fonte: Autoria Própria

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Na figura 11, é apresentado o fluxo de Pedido de Cadastro de Pedido de Compra.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nesse momento, o usuário acessará a tela do sistema e preencherá um formulário com as informações gerais do pedido de compra, como por exemplo, para qual fornecedor se destina, quais os produtos, os valores de cada produto, a margem de lucro e as informações inerentes ao pedido.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Na seleção de produtos, caso o produto não esteja cadastrado na base, ele terá a opção de fazer um cadastro sem sair da tela, através de um formulário que será exibido em formato de modal.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Após o preenchimento de todas as opções, o usuário clicará em salvar e o sistema fará a captura de todas as informações digitadas e enviará para o Firebase. Caso o processo ocorra com sucesso, o usuário receberá uma mensagem de feedback e será redirecionado para a tela geral de Pedidos de Compra.

Figura 11 - Diagrama de Sequência: Gerar Pedido de Compra
![Figura 11 - Diagrama de Sequência: Gerar Pedido de Compra](https://github.com/raulfdm/tcc/blob/master/Files/img/diagrama-sequencia/gerar-pedido-compra.png)
<br>Fonte: Autoria Própria

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Na figura 12, é exibido o fluxo de Gerar de Pedido de Venda, que será acessada apenas pelo (a) vendedor (a).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nele, o usuário acessará a tela de Pedidos de Venda ou a tela principal e selecionará a opção de cadastrar um novo pedido. Nesse momento, o mesmo será redirecionado para uma página com um formulário com as informações que deverão ser preenchidas.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;O usuário terá a opção de selecionar um cliente, ou de cadastrar um. Caso opte pelo cadastro, será exibido um modal com o formulário de cadastro de cliente, onde deverão ser preenchidas as informações do cliente. Ao salvar esse formulário, será enviado para o Firebase os dados, que retornará uma mensagem de sucesso ou erro, e, caso sucesso, a lista de clientes será atualizada, contemplando o novo cliente.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Após o preenchimento de todas as informações inerentes ao pedido de vendas, o usuário confirmará o salvamento e essas informações serão enviadas para o Firebase, que retornará uma mensagem de sucesso ou erro.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Caso a operação seja concluída com sucesso, o usuário receberá uma mensagem de sucesso e será redirecionada para a página principal de pedidos de venda.

Figura 12 - Diagrama de Sequência: Gerar de Pedido de Venda
![Figura 12 - Diagrama de Sequência: Gerar de Pedido de Venda](https://github.com/raulfdm/tcc/blob/master/Files/img/diagrama-sequencia/gerar-pedido-venda.png)
<br>Fonte: Autoria Própria

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Na figura 13, é exibido o fluxo de extração de relatórios, onde somente o vendedor (a) terá acesso. O usuário acessará a tela e escolherá qual o relatório que deseja ter acesso. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Caso escolha o relatório de estoque, o sistema fará uma consulta do estoque disponível, junto com a previsão de sua quantidade valorada no Firebase. Quando retornar, será exibido em formato de gráficos para o usuário.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Caso opte pelo relatório de fluxo de caixa, o sistema fará consultas no Firebase, buscando os recebimentos, pagamentos e quando os dados retornarem, o sistema exibirá graficamente a relação de compra e venda dos últimos 30 dias.

Figura 13 - Diagrama de Sequência: Extração de Relatórios
![Figura 13 - Diagrama de Sequência: Extração de Relatórios](https://github.com/raulfdm/tcc/blob/master/Files/img/diagrama-sequencia/relatorios.png)
<br>Fonte: Autoria Própria

[menu↑](#topo)


# <a name="modelagem-db">MODELAGEM DO BANCO DE DADOS</a>

## <a name="modelagem-mer">MODELO ENTIDADE RELACIONAMENTO (MER)</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;O modelo entidade-relacionamento é a implementação do modelo conceito, obtido a partir do diagrama entidade-relacionamento, para um SGBD em específico. No caso do sistema proposto, o banco de dados a ser utilizado será o Firebase Realtime Database.

[menu↑](#topo)

### <a name="modelagem-mer-firebase">O Banco de dados Firebase Realtime Database</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;O Firebase Realtime Database é um banco de dados oferecido pelo pela Google, é um SGBD NoSQL, ou seja, é um SGBD não relacional.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Bancos de dados não-relacionais tem como principal objetivo a alta escalabilidade e o alto desempenho alinhados com um baixo custo de manutenção e armazenamento de dados. Análogo à tabela em bancos de dados relacionais, no mundo não-relacional temos coleções. Essas coleções são compostas por objetos baseados no JavaScript Object Notation (JSON), onde possui uma estruturação simples de chave e valor. Na figura 14, podemos ver um exemplo de um documento em representação JSON, onde temos como chave as informações da esquerda como o nome, a idade e os filmes favoritos e ao lado direito temos o valor de cada chave. Por usar como base objetos JavaScript, podemos armazenar como valor de chave coleções (listas) e objetos, como pode ser visto na chave filmes-favoritos.

Figura 14 - Exemplo de documento objeto JSON gravado em um banco de dados NoSQL
<br>![Figura 14 - Exemplo de documento objeto JSON gravado em um banco de dados NoSQL](https://github.com/raulfdm/tcc/blob/master/Files/img/exemplo-json.png)
<br>Fonte: Autoria Própria

[menu↑](#topo)

### <a name="modelagem-mer-nosql">O Modelo Entidade-Relacionamento e o NoSQL</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Para a modelagem dos dados no Firebase Realtime Database, faz-se necessário uma abordagem diferente da convencional, pois, não temos relacionamentos diretos (chaves primárias ou estrangeiras) entre as coleções.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Apesar de não ter um relacionamento direto, podemos ter valores fazendo referencias para outros objetos em outras coleções, como pode ser visto na figura 15, onde, cada registro da coleção Usuário possui uma lista de cursos no qual estão matriculados. Essa lista por sua vez, possui apenas o id do curso, que faz referência para os valores da coleção de Cursos.

Figura 15 - Exemplo de relacionamento entre coleções
<br>![Figura 15 - Exemplo de relacionamento entre coleções](https://github.com/raulfdm/tcc/blob/master/Files/img/relacionamento-colecoes.png)
<br>Fonte: Autoria Própria

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Apesar de existir essa forma de interligação entre coleções, fica por parte da aplicação realizar a manipulação de informações para eventuais consultas. Uma vez que todo o controle será feito pela aplicação, as informações que serão armazenadas serão exatamente as mesmas das descritas no diagrama de classe.

[menu↑](#topo)

## <a name="modelagem-der">DIAGRAMA ENTIDADE RELACIONAMENTO (DER)</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;O Diagrama Entidade Relacionamento (DER) é a representação gráfica do modelo conceitual (MER). Como explicado anteriormente, a modelagem deste projeto utiliza banco de dados não relacional, assim, toda a relação entre as entidades (classes) bem como as informações que serão gravadas, foi representada no diagrama de classe, bem como sua cardinalidade. Assim, essa abordagem não é aplicável à arquitetura definida para o projeto.

[menu↑](#topo)

# <a name="story-board">STORY BOARD</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;As figuras abaixo têm o propósito de fornecer uma visão gráfica de como será a aparência visual do sistema em sua concepção.

Figura 16 - Tela: Login
![Figura 16 - Tela: Login](https://github.com/raulfdm/tcc/blob/master/Files/mockup/1.%20Login.png)
<br>Fonte: Autoria Própria

[menu↑](#topo)

Figura 17 - Tela: Login com o Google
![Figura 17 - Tela: Login com o Google](https://github.com/raulfdm/tcc/blob/master/Files/mockup/1.1%20Login%20com%20Google.png)
<br>Fonte: Autoria Própria

[menu↑](#topo)

Figura 18 - Tela: Dashboard (principal)
![Figura 18 - Tela: Dashboard (principal)](https://github.com/raulfdm/tcc/blob/master/Files/mockup/2.%20Home%20-%20Dashboard.png)
<br>Fonte: Autoria Própria

[menu↑](#topo)

Figura 19 - Tela: Dashboard - Menu de cadastro
![Figura 19 - Tela: Dashboard - Menu de cadastro](https://github.com/raulfdm/tcc/blob/master/Files/mockup/2.3%20Home%20-%20Dashboard%20-%20A%C3%A7%C3%B5es%20Op%C3%A7%C3%B5es.png)
<br>Fonte: Autoria Própria

[menu↑](#topo)

Figura 20 - Tela: Dashboard - Menu de sessão
![Figura 20 - Tela: Dashboard - Menu de sessão](https://github.com/raulfdm/tcc/blob/master/Files/mockup/2.4%20Home%20-%20Dashboard%20-%20Perfil%20Op%C3%A7%C3%B5es.png)
<br>Fonte: Autoria Própria

[menu↑](#topo)

Figura 21 - Tela: Clientes
![Figura 21 - Tela: Clientes](https://github.com/raulfdm/tcc/blob/master/Files/mockup/3.%20Home%20-%20Clientes.png)
<br>Fonte: Autoria Própria

[menu↑](#topo)

Figura 22 - Tela: Carteira de Cliente 1/3
![Figura 22 - Tela: Carteira de Cliente 1/3](https://github.com/raulfdm/tcc/blob/master/Files/mockup/3.1%20Home%20-%20Cliente%20-%20Administrar%201_3.png)
<br>Fonte: Autoria Própria

[menu↑](#topo)

Figura 23 - Tela: Carteira de Cliente 2/3
![Figura 23 - Tela: Carteira de Cliente 2/3](https://github.com/raulfdm/tcc/blob/master/Files/mockup/3.2%20Home%20-%20Cliente%20-%20Administrar%202_3.png)
<br>Fonte: Autoria Própria

[menu↑](#topo)

Figura 24 - Tela: Carteira de Cliente 3/3
![Figura 24 - Tela: Carteira de Cliente 3/3](https://github.com/raulfdm/tcc/blob/master/Files/mockup/3.3%20Home%20-%20Cliente%20-%20Administrar%203_3.png)
<br>Fonte: Autoria Própria

[menu↑](#topo)

Figura 25 - Tela: Cadastrar Cliente
![Figura 25 - Tela: Cadastrar Cliente](https://github.com/raulfdm/tcc/blob/master/Files/mockup/3.4%20Home%20-%20Clientes%20-%20Cadastrar.png)
<br>Fonte: Autoria Própria

[menu↑](#topo)

Figura 26 - Tela: Editar Cliente
![Figura 26 - Tela: Editar Cliente](https://github.com/raulfdm/tcc/blob/master/Files/mockup/3.5%20Home%20-%20Clientes%20-%20Editar.png)
<br>Fonte: Autoria Própria

[menu↑](#topo)

Figura 27 - Tela: Fornecedores
![Figura 27 - Tela: Fornecedores](https://github.com/raulfdm/tcc/blob/master/Files/mockup/4.%20Home%20-%20Fornecedores.png)
<br>Fonte: Autoria Própria

[menu↑](#topo)

Figura 28 - Tela: Pedido de Compra
![Figura 28 - Tela: Pedido de Compra](https://github.com/raulfdm/tcc/blob/master/Files/mockup/6.%20Home%20-%20Pedidos%20de%20Compra.png)
<br>Fonte: Autoria Própria

[menu↑](#topo)

Figura 29 - Tela: Cadastrar Pedido de Compra 1/2
![Figura 29 - Tela: Cadastrar Pedido de Compra 1/2](https://github.com/raulfdm/tcc/blob/master/Files/mockup/6.1%20Home%20-%20Pedidos%20de%20Compra%20-%20Cadastrar%201_2.png)
<br>Fonte: Autoria Própria

[menu↑](#topo)

Figura 30 - Tela: Cadastrar Pedido de Compra 2/2
![Figura 30 - Tela: Cadastrar Pedido de Compra 2/2](https://github.com/raulfdm/tcc/blob/master/Files/mockup/6.4%20Home%20-%20Pedidos%20de%20Compra%20-%20Cadastrar%202_2.png)
<br>Fonte: Autoria Própria

[menu↑](#topo)

## <a name="cronograma">CRONOGRAMA PARA O DESENVOLVIMENTO</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;O quadro 26 tem mostra o cronograma proposto para o desenvolvimento de projeto, focando em entregas contínuas por módulos.

Quadro 26 - Calendário de Entregas

|   Data   | Entrega     |
| :------: |:-----------:| 
|16/08/2016|Proposta do Projeto|
|02/09/2016|Introdução|
|02/09/2016|Escopo|
|07/09/2016|Use Case de Negócio|
|13/09/2016|Descrição dos Stakeholders|
|13/09/2016|Definição do Problema|
|13/09/2016|Diagrama de Ishikawa|
|13/09/2016|Lista de Restrições|
|20/09/2016|Descrição Geral do Sistema|
|20/09/2016|Proposta|
|20/09/2016|Fronteira Sistêmica|
|27/09/2016|Use Case de Sistema|
|03/10/2016|Slides|
|04/10/2016|Pré-Banca|
|11/10/2016|Pré-Banca|
|25/10/2016|Diagrama de Classe|
|08/11/2016|Diagrama de Sequência|
|15/11/2016|MER e DER|
|22/11/2016|Storyboard|
|29/11/2016|Entrega Impressos|
|12/11/2016|Banca|

[menu↑](#topo)

## <a name="referencias">Referências Bibliográficas</a>

DEVELOPER NETWORK, Mozila. *JSON: JavaScript Object Notation*. Disponível em: <https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/JSON>. Acesso em: 05 set. 2016

DEVELOPERS, Google. *Progressive Web Apps: A new way to devliver amazing user experiences on the web*. Disponível em: <https://developers.google.com/web/progressive-web-apps/>. Acesso em: 18 out. 2016.

RODRIGUES, Joel. *Modelo Entidade Relacionamento (MER) e Diagrama Entidade-Relacionamento (DER)*.
Disponível em: <http://www.devmedia.com.br/modelo-entidade-relacionamento-mer-e-diagrama-entidade-relacionamento-der/14332>. Acesso em: 26 nov. 2016.

W3Schools. *CSS Introduction*. Disponível em: <http://www.w3schools.com/css/css_intro.asp>. Acesso em: 23 nov. 2016

W3Schools. *HTML Introduction*. Disponível em: <http://www.w3schools.com/html/html_intro.asp>. Acesso em: 23 nov. 2016

WIKIPEDIA, Wikimedia Foundation. *NoSQL*. Disponível em: <https://en.wikipedia.org/wiki/NoSQL>. Acesso em: 30 nov. 2016

WIKIPEDIA, Wikimedia Foundation. *Stakeholder*. Disponível em: <https://pt.wikipedia.org/wiki/Stakeholder>. Acesso em: 01 set. 2016

WIKIPEDIA, Wikimedia Foundation. *Word Wide Web*. Disponível em: <https://pt.wikipedia.org/wiki/World_Wide_Web>. Acesso em: 24 nov. 2016.

[menu↑](#topo)

