

## Pessoa
```
Pessoa
--
- id: string
- cep: number
- endereco: string
- numeroEndereco: number
- complemento: string
- telefone: string
- celular: string
--
```

## Fornecedor
```
Fornecedor
--
- cnpj: string
- razaoSocial: string
--
```

## Cliente
```
Cliente
--
- nomeCompleto: string
- cpf: string
- dataNascimento: date
--
```

## Pedido

```
Pedido
--
- idvendedor: string
- idpedido: string
- produtos: Array
- data: Date
--
+ totalPedido(): Number
+ listaProdutos(): Array
```

```
Pedido de venda
--
- idcliente: string
```
	
```
Pedido de Compra	
--
- idfornecedor: string
```
