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
```

```
PessoaJuridica
--
- idfornecedor: String
- cnpj: String
- razaoSocial: String
```

```
PessoaFisica
--
- idusuario: String
- nomeCompleto: String
- cpf: String
- dataNascimento: Date
- usuarioSistema: UsuarioSistema
```

```
UsuarioSistema
--
- idusuario: String
- email: String
- senha: String
- tipousuario: String
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
- listaRecebeimentos: Array(Recebimento)
--
- gerarRecebimentos(): void
```
	
```
PedidoCompra	
--
- idfornecedor: String
- listaPagamentos: Array(Pagamento)
--
- gerarPagamentos(): void
```

## Financeiro

```
Contas
--
- idpedido: String
- dataPrevista: Date
- dataEfetivacao: Date
- quitado: Boolean

```

```
Recebimento
--
- idrecebimento: String

```

```
Pagamento
--
- idpagamento: String
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
- produtoEstoque: Object {
    - quantidade: Number
    - Produto: Produto
}
-- 
+ salvaProdutoEstoque(Produto): void
+ estoquePorProduto(): Array
+ valorEmEstoque(): Number

```

## Carteira Cliente
```
CarteiraCliente
--
- idcliente: String
--
+ listaCompras(): Array(Object)
+ listaPagamentos(): Array(Object)
+ saldoDevedor(): Number
```