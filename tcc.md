## Introdução
A empresa alvo deste projeto é constituída por apenas uma pessoa, uma comerciante autônoma, vendedora de roupas e acessórios que atua no ramo há 25 anos. Seus (uas) clientes são pessoas físicas que as solicita uma visita residencial para a apresentação das mercadorias trazidas de outras cidades, como por exemplo Rio Preto, São Paulo, Goiânia, entre outras.
Após realizada a venda, é criado uma ficha cadastral, onde a vendedora anota as informações básicas para contato e identificação, a quantidade total da venda e as parcelas com suas respectivas datas de pagamento. Diariamente essas fichas são consultadas para avaliar duas informações cruciais ao negócio. A primeira é saber de quem fará os recebimentos pendentes do dia e a segunda é saber qual cliente está no fim da dívida, para realizar um contato e marcar um horário para a apresentação das novas mercadorias.
Nas viagens de compra de mercadoria, quase todas as negociações são feitas através de cheques pré-datados. Desta maneira, também faz-se necessário validar diariamente quais os cheques que deverão ser pagos no dia, para que seja feito o depósito do valor em questão.
Assim, o sistema deverá proporcionar um controle dos pagamentos e recebimentos, bem como informar ao usuário todas as informações importantes para o início das atividades de forma automatizada, otimizando o tempo gasto nas tarefas manuais.

###	Objetivo Geral
O objetivo deste projeto é criar um sistema de informação para uma empreendedora autônoma no seguimento de venda de roupas e acessórios.

###	Objetivos Específicos
Os objetivos específicos são:
* Controlar a compra de mercadorias;
* Manter um cadastro de todas clientes;
* Cadastrar pedidos de vendas;
* Controlar contas a receber;
* Controlar prospecção das vendas;
* Implementar no sistema o acesso por perfis de usuário
* Disparar e-mail list e mensagens para smartphones


##	Escopo
O trabalho é feito por no máximo duas pessoas. O comerciante acompanha as tendências da moda através das mídias sociais, televisão, revistas e encartes enviados pelas lojas para acompanhamento das novidades e potencial comercial para seu público alvo. Com essas referências em mente, o primeiro passo é a compra das mercadorias.
A vendedora entra em contato com uma agência que realiza viagens para cidades que possuam um centro comercial atacadista e consulta quais são as datas previstas para as viagens e quais as cidades. Cada cidade possui um tipo específico de mercadorias, assim, caso a vendedora não tenha experiência com compras, ele pode consultar com o representante da agência, que saberá informar o melhor destino para seu publico alvo. Também são fornecidas informações sobre condições de pagamento dos locais
No dia da viagem, a vendedora se dirige ao local onde o ônibus sairá e partem rumo a cidade destino. Chegando no shopping atacadista, a vendedora assiste desfiles de modas e consome a divulgação das mercadorias vendidas pelas lojas, afim de direcionar cada vendedor para a loja específica.
Na loja, a vendedora analisa as mercadorias e realiza a compra, sempre de 3 (três) ou mais peças, por se tratar de atacado. É combinado com a vendedora da loja, o valor total, o desconto e a forma de pagamento, que podem ser à vista, cartão de crédito parcelado ou cheques pré-datados.
As viagens tem duração de 1 ou 2 dias, dependendo do destino e agência escolhida. Assim, voltando para a cidade com as mercadorias adquiridas, a vendedora começa a se organizar para fazer o controle de toda mercadoria adquirida.
O primeiro passo é a organização de mercadorias para facilitar a marcação de preços. As mercadorias são separadas em grupos definidos por qual loja elas foram adquiridas. Após esta organização física, a vendedora passa anotando de cada peça, o tipo da mercadoria, por exemplo, calça, blusa, vestino, seu preço de custo e de venda. A anotação do preço acontece tanto no caderno, quanto na etiqueta, para facilitar a visualização do mesmo na hora da venda. Após esse processo, as mercadorias são separadas por tamanho (P, M, G, etc.) e guardadas em sacolas. 
No processo seguinte, no mesmo caderno onde foram anotados os valores de cada mercadoria, é feita uma somatória do total investido e do total a ser vendido. Caso as mercadorias tenham sido adquiridas por cheque pré-datado, é anotado o valor do cheque e a data a ser pago. Esses dados servirão de consulta para saber se há pagamentos a serem realizados no dia.
Terminado o processo de organização das mercadorias, a vendedora começa a entrar em contato com a sua carteira de cliente, sempre priorizando os clientes que possuem maior credibilidade no histórico de pagamentos e compras. No contato com o cliente, é agendado uma data e um local para que seja apresentado as mercadorias.
Na data combinada, a vendedora vai até o local escolhido pelo cliente, que pode ser desde o local de trabalho, quanto sua própria casa, e apresenta as mercadorias do tamanho do cliente. Essa apresentação é feita com o próprio cliente escolhendo das peças que gostou e a vendedora opina sobre como fazer combinações entre peças, combinação de cores, combinação do próprio estilo da pessoa com a roupa.
No fim da visita, o cliente informa a vendedora quais as mercadorias que mais lhe agradaram e que ele deseja comprar. Caso seja um cliente novo, a vendedora pega uma pasta com as fichas de todos os clientes e cria uma nova ficha. Esta, deve conter informações básicas para o contato, como o nome completo, telefones para contato, endereço. Caso seja um cliente já antigo, a vendedora procura a ficha deste cliente. Em seguida, a vendedora soma o total e informa o cliente quais as condições disponíveis de pagamento. Essas, podem ser à vista ou à prazo (30/60/90 dias) no cheque ou na caderneta. Após o cliente escolher a forma de pagamento, é anotado em sua fecha as datas e o valor de cada parcela, junto com o valor total da compra.
Uma das condições mais usadas como condição de pagamento é o fiado. Esse método é baseado na confiança, ou seja, a cliente faz a compra, divide o valor total em no máximo 4 meses e informa o dia que poderá pagar a parcela. Na data informada, a vendedora entra em contato com a cliente para fazer o recebimento.
Logo, todos os dias pela manhã a vendedora consulta as fichas de cada cliente para verificar se há recebimentos a serem feitos naquele dia. Caso haja, é feito um contato com a mesma, que diz se a vendedora pode ou não fazer o recebimento. Caso a cliente não tenha dinheiro naquele dia, é agendado para uma nova data, substituindo a data anotada pela data informada pela cliente.

## Use Case de Negócio
