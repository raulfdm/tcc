# <a name="topo">Menu</a>
1. [Introdução](#intro)
  1. [Objetivo Geral](#obj-geral)
  1. [Objetivos Específicos](#obj-espec)
  1. [Escopo](#escopo)
1. [Análise do Negócio](#analise-de-negocio)
  1. [Use Case de Negócio](#use-case-negocio)
  1. [Descrição dos Processos de Negócio](#descricao-dos-processos)
  1. [Descrição dos Stakeholders](#stakeholders)
  1. [Definição do Problema](#definicao-problema)
  1. [Diagrama de Causa e Efeito](#ishikawa)
  1. [Lista de Restrições](#restricoes)

1. [Referências](#referencias)


# <a name="intro">Introdução</a>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;A empresa alvo deste projeto possui apenas duas pessoas, uma comerciante autônoma, vendedora de roupas e acessórios que atua no ramo há 25 anos e sua filha que está iniciando no ramo de vendas. Por se tretar de uma micro empresa, ambas cuidam de todas as áreas, desde as vendas, contas a pagar, contas a receber e até mesmo as compras de mercadorias. Seus(uas) clientes são pessoas físicas que as solicitam uma visita residencial para a apresentação das mercadorias trazidas de outras cidades, como por exemplo Rio Preto, São Paulo, Goiânia, entre outras.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Após realizada a apresentação e venda, a vendedora cria uma ficha cadastral, onde é anotado informações básicas para contato e identificação do cliente e informações gerais sobre as vendas realizadas, como a quantidade total da compra e as parcelas com suas respectivas datas de pagamento. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Diariamente essas fichas são consultadas para avaliar duas informações cruciais ao negócio. A primeira é identificar quais são os recebimentos a serem feitos no dia e a segunda é identificar os clientes que estão perto de quitar sua dívida, com o intuito de realizar contato e agendar um horário para a apresentação das novas mercadorias.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nas viagens de compra de mercadoria, quase todas as negociações são feitas através de cheques pré-datados. Desta maneira, também faz-se necessário validar diariamente os cheques que deverão ser pagos no dia, para que seja feito o depósito do valor em questão.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Assim, o sistema deverá proporcionar um controle dos pagamentos e recebimentos, bem como exibir ao usuário todas as informações importantes para o início das atividades de forma automatizada, otimizando o tempo gasto nas tarefas manuais.

[menu↑](#topo)

## <a name="obj-geral">Objetivo Geral</a>
O objetivo deste projeto é criar um sistema de informação para uma empreendedora autônoma no seguimento de venda de roupas e acessórios.

[menu↑](#topo)

## <a name="obj-espec">Objetivos Específicos</a>
Os objetivos específicos são:
* Controlar a compra de mercadorias;
* Manter um cadastro de todas clientes;
* Cadastrar pedidos de vendas;
* Controlar contas a receber;
* Controlar prospecção das vendas;
* Implementar no sistema o acesso por perfis de usuário
* Disparar e-mail list e mensagens para smartphones

[menu↑](#topo)

##	<a name="escopo">Escopo</a>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;O trabalho é feito por duas pessoas. O(A) comerciante acompanha as tendências da moda através das mídias sociais, televisão, revistas e encartes enviados pelas lojas para saber quais as novidades e potencial comercial para seu público alvo. Com essas referências em mente, o primeiro passo é a compra das mercadorias.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;O(A) vendedor(a) entra em contato com uma agência que realiza viagens para cidades que possuam um centro comercial atacadista e consulta as datas previstas para as viagens e quais as cidades. Cada cidade possui um tipo específico de mercadorias, assim, caso o(a) vendedor(a) não tenha experiência com compras, ele pode consultar o representante da agência, que saberá informar o destino que melhor atenderá suas necessidades e passar informações sobre condições de pagamento dos locais.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;No dia da viagem, o(a) vendedor(a) se dirige ao local onde o ônibus sairá e partem rumo a cidade destino. Chegado ao destino, (o)a vendedor(a) assiste desfiles de modas e consome a divulgação das mercadorias feitas por cada loja, afim de fazer uma breve apresentação de quais mercadorias estão disponíveis para compra.
Na loja, a vendedora analisa as mercadorias e efetiva a compra das peças que lhe interessaram, no mínimo 6 (seis) ou mais peças, por se tratar de lojas atacadistas. É combinado com o(a) vendedor(a) da loja, o valor total, o desconto e a forma de pagamento, que podem ser à vista, cartão de crédito parcelado ou cheques pré-datados.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;As viagens tem duração de 1 ou 2 dias, variando conforme a agência e/ou destino escolhidos. No retorno, (o)a vendedor(a) organiza-se para fazer o controle e separação de toda mercadoria adquirida.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;O primeiro passo é a organização das mercadorias para facilitar a marcação de preços, separando as mercadorias em grupos definidos por loja ou por marca. Após a organização física, o(a) vendedor(a) anota peça a peça o tipo da mercadoria, por exemplo, calça, blusa, vestido, seu preço de custo e de venda em um caderno. A anotação do preço acontece tanto no caderno, quanto em sua etiqueta, para facilitar a visualização do mesmo na hora da venda. Após esse processo, as mercadorias são separadas por tamanho (P, M, G, etc.) e guardadas em sacolas. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;No processo seguinte, no mesmo caderno onde foram anotados os valores de cada mercadoria, é feita a somatória do valor total investido e do valor total a ser vendido. Caso as mercadorias tenham sido adquiridas por cheque pré-datado, é anotado o valor do cheque e a data a ser pago. Esses dados servirão de consulta para as contas a pagar por dia.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Terminado o processo de organização e separação das mercadorias, o(a) vendedor(a) entra em contato com a sua carteira de cliente, sempre priorizando os clientes que possuem maior credibilidade no histórico de pagamentos e compras. No contato, é informado que estão disponíveis noças mercadorias e caso o(a) cliente tenha interesse, é agendado a data e o local para que seja feita a apresentação.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Na data e hora combinada, o(a) vendedor(a) vai até o local escolhido pelo(a) cliente, que pode ser desde o local de trabalho ou sua própria casa, e apresenta as mercadorias de acordo com o tamanho do cliente. O(A) cliente assiste a apresentação e escolhe as peças que tem interesse em adquirir e a vendedora opina sobre como fazer combinações entre peças, combinação de cores, combinação do próprio estilo da pessoa com a roupa. O(A) cliente tem a possibilidade de experimentar a peça durante a visita.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;No fim da visita, o cliente informa a vendedora quais as mercadorias que deseja adquirir. Caso seja um cliente novo, a vendedora pega uma pasta com as fichas de todos os clientes e cria uma nova ficha  que contém informações básicas para o contato, como o nome completo, telefones para contato, endereço. Caso seja um cliente já antigo, a vendedora procura a ficha deste cliente na pasta para fazer as anotações da compra. Em seguida, a vendedora soma o total e informa o cliente quais as condições disponíveis de pagamento. Essas, podem ser à vista ou à prazo (30/60/90 dias) no cheque ou na caderneta. Após o cliente escolher a forma de pagamento, é anotado em sua ficha as datas e o valor de cada parcela, junto com o valor total da compra.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Uma das condições mais usadas como condição de pagamento é o fiado. Esse método é baseado na confiança, ou seja, a cliente faz a compra, divide o valor total em no máximo 4 meses e informa o dia que poderá pagar a parcela. Na data informada, a vendedora entra em contato com a cliente para fazer o recebimento. O controle é todo feito através da ficha da cliente.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Logo, todos os dias pela manhã a vendedora consulta as fichas de cada cliente para verificar se há recebimentos a serem feitos naquele dia. Caso haja, é feito um contato com a mesma, que diz se a vendedora pode ou não fazer o recebimento. Caso a cliente não tenha dinheiro naquele dia, é agendado para uma nova data, substituindo a data anotada pela data informada pela cliente.

[menu↑](#topo)

# <a name="analise-de-negocio">Análise do Negócio</a>

## <a name="use-case-negocio">Use Case de Negócio</a>
![Use case de negócio](https://github.com/raulfdm/tcc/blob/master/Files/UML/img/use-case-negocio.png)

[menu↑](#topo)

### <a name="descricao-dos-processos">Descrição dos processos de negócio</a>

<table>
<caption>Quadro 1 - Use Case de Negócio: Agendar Viagem</caption>
  <tr>
  <td>Use Case de Negócio:</td>
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
<caption>Quadro 2 - Use Case de Negócio: Comprar Mercadorias</caption>
  <tr>
  <td>Use Case de Negócio:</td>
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
<caption>Quadro 3 - Use Case de Negócio: Organizar Mercadorias</caption>
  <tr>
  <td>Use Case de Negócio:</td>
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
<caption>Quadro 4 - Use Case de Negócio: Anotar Preços nas Mercadorias</caption>
  <tr>
  <td>Use Case de Negócio:</td>
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
<caption>Quadro 5 - Use Case de Negócio: Consultar Contas a Pagar</caption>
  <tr>
  <td>Use Case de Negócio:</td>
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
<caption>Quadro 6 - Use Case de Negócio: Pagar Contas</caption>
  <tr>
  <td>Use Case de Negócio:</td>
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
<caption>Quadro 7 - Use Case de Negócio: Consultar Contas a Receber</caption>
  <tr>
  <td>Use Case de Negócio:</td>
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
<caption>Quadro 8 - Use Case de Negócio: Ligar para o Cliente</caption>
  <tr>
  <td>Use Case de Negócio:</td>
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
<caption>Quadro 9 - Use Case de Negócio: Ligar para o Cliente</caption>
  <tr>
  <td>Use Case de Negócio:</td>
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
<caption>Quadro 11 - Use Case de Negócio: Visitar Cliente</caption>
  <tr>
  <td>Use Case de Negócio:</td>
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
<caption>Quadro 12 - Use Case de Negócio: Fazer Recebimento</caption>
  <tr>
  <td>Use Case de Negócio:</td>
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
<caption>Quadro 13 - Use Case de Negócio: Dar baixa do pagatamento na ficha do cliente</caption>
  <tr>
  <td>Use Case de Negócio:</td>
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
<caption>Quadro 14 - Use Case de Negócio: Mostrar Mercadorias</caption>
  <tr>
  <td>Use Case de Negócio:</td>
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
<caption>Quadro 15 - Use Case de Negócio: Realizar Venda</caption>
  <tr>
  <td>Use Case de Negócio:</td>
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
<caption>Quadro 16 - Use Case de Negócio: Anotar Venda na Ficha do Cliente</caption>
  <tr>
  <td>Use Case de Negócio:</td>
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

## <a name="stakeholders">Descrição dos Stakeholders</a>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;O termo Stackholder se refere a uma pessoa ou grupo de pessoas interessadas  em uma empresa, negócio ou indústria. Assim, o stakeholder da empresa é a própria fundadora. 

[menu↑](#topo)

## <a name="definicao-problema"> Definição do Problema</a>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Baseado no escopo de negócio, podemos afirmar que o problema é o controle de todas as atividades pertinentes ao trabalho do(a) comerciante serem feitas em papeis e caderno. Essa atitude apesar de ter sido adotada há muito tempo, possibilita as chances de alguma falha no processo acontecer, como por exemplo perda de dados de clientes ou de pagamentos a serem feitos, e também diminui de forma significativa a capacidade de analisar de forma precisa o histórico de venda para tomadas de decisão.

[menu↑](#topo)

## <a name="ishikawa>Diagrama de Causa e Efeito (Espinha de Peixe)</a>
![Diagrama de causa e efeito (Ishikawa)](https://github.com/raulfdm/tcc/blob/master/Files/UML/img/diagrama-ishikawa.png)

[menu↑](#topo)

## <a name="restricoes">Lista de Restrições</a> 
|   Restrição   | Descrição           
| :-----------: |:-------------:
| Linguagem de Programação (Front-end) | Javascript, HTML5, CSS3 
| Servidor Web      |       
| Banco de Dados e |  NoSQL (firebase)
|      

[menu↑](#topo)

## <a name="referencias">Referências (em construção)</a>
Stakeholder: https://www.significados.com.br/stakeholder/

[menu↑](#topo)
