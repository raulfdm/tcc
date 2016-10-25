## Pessoa
```
Pessoa
--
- id: String
- cep: Number
- endereco: String
- numeroEndereco: Number
- complemento: String
- telefone: String
- celular: String
--
```

```
Fornecedor
--
- cnpj: String
- razaoSocial: String
--
```

```
Cliente
--
- nomeCompleto: String
- cpf: String
- dataNascimento: Date
--
```

```
UsuarioSistema
--
- email: String
- senha: String
- user: Pessoa
- configuracoes: Object
--
+ login(): void
+ logout(): void
+ changePassword(): void
```

## Pedido

```
Pedido
--
- idvendedor: String
- idpedido: String
- produtos: Array(Produto)
- data: Date
- total: Number
--
- calculaTotal(): Number
+ totalPedido(): String
```

```
PedidoVenda
--
- idcliente: String
```
	
```
PedidoCompra	
--
- idfornecedor: String
```



## Produto
```
Produto
--
- id: String
- referencia: String
- Descricao: String
- idfornecedor: String
- pedido: Object {
    - idpedido: String
    - quantidade: Number
    - valorUnitario: Number
}
```

## Estoque
```
Estoque
--
- produtos: Array
```
