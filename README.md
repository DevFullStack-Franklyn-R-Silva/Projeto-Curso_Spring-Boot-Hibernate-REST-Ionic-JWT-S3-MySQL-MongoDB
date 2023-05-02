# Projeto E-commerce
Esse é um projeto de um sistema de e-commerce desenvolvido em Java com o framework Spring Boot, banco de dados H2. O Maven é usado como gerenciador de dependências. A aplicação usa o padrão de projeto DTO (Data Transfer Object) para transferir dados entre as camadas.

O projeto foi desenvolvido com a finalidade de ser um exemplo de implementação de um sistema de e-commerce básico, utilizando as tecnologias mencionadas abaixo. Ele pode ser utilizado como referência para o desenvolvimento de projetos semelhantes ou para fins educacionais.
## Dependências
O projeto usa as seguintes dependências:
- devtools
- jpa
- h2
- spring boot starter web

## Estrutura do projeto
- O projeto possui as seguintes classes:
- Categoria
- Cidade
- Cliente
- Endereço
- Estado
- ItemPedido
- ItemPedidoPK
- Pagamento
- PagamentoComBoleto
- PagamentoComCartao
- Pedido
- Produto



## Atributos das classes
Categoria
- id (Integer)
- nome (String)
- produtos (List)

Cidade
- id (Integer)
- nome (String)
- estado (Estado)

Cliente
- id (Integer)
- nome (String)
- email (String)
- cpfOuCnpj (String)
- tipo (Integer)
- enderecos (List)
- telefones (Set)
- pedidos (List)

Endereço
- id (Integer)
- logradouro (String)
- numero (String)
- complemento (String)
- bairro (String)
- cep (String)
- cliente (Cliente)
- cidade (Cidade)

Estado
- id (Integer)
- nome (String)
- cidades (List)

ItemPedido
- id (ItemPedidoPK)
- desconto (Double)
- quantidade (Integer)
- preco (Double)

ItemPedidoPK
- pedido (Pedido)
- produto (Produto)

Pagamento
- id (Integer)
- estado (Integer)
- pedido (Pedido)

PagamentoComBoleto
- dataVencimento (Date)
- dataPagamento (Date)

PagamentoComCartao
- numeroDeParcelas (Integer)

Pedido
- id (Integer)
- instante (Date)
- pagamento (Pagamento)
- cliente (Cliente)
- enderecoDeEntrega (Endereco)
- itens (Set)

Produto
- id (Integer)
- nome (String)
- preco (Double)
- categorias (List)
- itens (Set)

## Build
O projeto foi construído usando Maven.
