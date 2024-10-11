# Sistema de Vendas

Este projeto implementa um sistema básico de gerenciamento de vendas, onde os dados de clientes, produtos e vendas são armazenados em um banco de dados. Ele inclui funcionalidades para registrar novos clientes, produtos disponíveis para venda, vendas realizadas e atualizações automáticas no estoque após cada venda.

## Funcionalidades

- **Gestão de Clientes**: Registra informações de clientes como nome, e-mail e telefone.
- **Gestão de Produtos**: Armazena os produtos disponíveis, preços e quantidade em estoque.
- **Gestão de Vendas**: Permite registrar as vendas realizadas, associando clientes aos produtos adquiridos, além de data e quantidade de cada venda.

## Estrutura do Banco de Dados

### Tabelas

- **Clientes**:
  - `ClienteID`: Identificador único do cliente.
  - `Nome`: Nome completo do cliente.
  - `Email`: E-mail do cliente.
  - `Telefone`: Número de telefone do cliente.

- **Produtos**:
  - `ProdutoID`: Identificador único do produto.
  - `Nome`: Nome do produto.
  - `Preco`: Preço do produto.
  - `QuantidadeEstoque`: Quantidade do produto disponível em estoque.

- **Vendas**:
  - `VendaID`: Identificador único da venda.
  - `ClienteID`: Referência ao cliente que realizou a compra.
  - `ProdutoID`: Referência ao produto vendido.
  - `QuantidadeVendida`: Quantidade de produtos vendidos na transação.
  - `DataVenda`: Data da venda.

## Consultas Disponíveis

1. **Mostrar todas as vendas realizadas, com nome do cliente e produto**:
   - Exibe o histórico completo de vendas, relacionando cliente, produto, quantidade e data.

2. **Mostrar todas as compras realizadas por um cliente específico**:
   - Exibe os produtos comprados por um cliente específico, junto com a quantidade e data da compra.

3. **Exibir o total de vendas realizadas por produto**:
   - Mostra a quantidade total vendida de cada produto.

## Atualização e Deleção de Dados

1. **Atualizar o estoque de um produto após uma venda**:
   - Reduz automaticamente o estoque do produto após a venda ser registrada.

2. **Atualizar informações de um cliente**:
   - Permite modificar dados de clientes, como nome e e-mail.

3. **Deletar uma venda e, se necessário, o cliente associado**:
   - Remove uma venda específica e, opcionalmente, exclui o cliente, caso ele não tenha outras vendas registradas.

## Como Usar

1. **Criar o Banco de Dados**:
   Execute o script SQL fornecido para criar o banco de dados e as tabelas.

2. **Inserir Dados**:
   Insira dados nas tabelas de Clientes, Produtos e Vendas conforme necessário, utilizando o script SQL.

3. **Consultar, Atualizar e Deletar**:
   Utilize as consultas SQL para visualizar e modificar os dados no banco de dados.

## Licença

Este projeto está licenciado sob a Licença MIT. Consulte o arquivo `LICENSE` para mais detalhes.

## Requisitos

- MySQL ou outro sistema de gerenciamento de banco de dados compatível com SQL.
- Ferramenta para execução de scripts SQL, como MySQL Workbench ou phpMyAdmin.
