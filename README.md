# Projeto de Folha de Pagamento
Este projeto é uma API RESTful desenvolvida em C# usando o ASP.NET Core e Entity Framework. O objetivo é gerenciar informações sobre funcionários e suas respectivas folhas de pagamento.

## Funcionalidades
Cadastro de Funcionários: <br>Permite cadastrar novos funcionários com informações básicas, como nome e CPF.

Listagem de Funcionários:<br> Possibilita listar todos os funcionários cadastrados.

Atualização de Funcionários:<br> Permite atualizar as informações de um funcionário existente.

Busca de Funcionários:<br> Possibilita buscar um funcionário específico pelo seu ID.

Remoção de Funcionários:<br> Permite deletar um funcionário da base de dados.

Cadastro de Folhas de Pagamento:<br> Permite cadastrar folhas de pagamento, calculando automaticamente impostos e descontos.

Listagem de Folhas de Pagamento:<br> Possibilita listar todas as folhas de pagamento.

Busca de Folhas de Pagamento:<br> Permite buscar uma folha específica pelo CPF do funcionário, mês e ano.

Remoção de Folhas de Pagamento:<br> Permite deletar uma folha de pagamento da base de dados.

## Estrutura do Projeto
O projeto é dividido em três principais componentes:

### Models:
#### Funcionario:
Representa os dados do funcionário.

#### Folha: 
Representa os dados da folha de pagamento.

#### AppDataContext:
Contexto do Entity Framework que gerencia as entidades do banco de dados.

#### Program.cs:
Configura a aplicação, as rotas e a conexão com o banco de dados SQLite.
Define as rotas para as operações CRUD de funcionários e folhas de pagamento.
Como Executar o Projeto
Para executar o projeto, siga os passos abaixo:

## Como Executar o Projeto

### 1. Clone o repositório:
git clone https://github.com/GabrielDittrich/folha-de-pagamento

cd (nome-do-projeto)

### 2. Restaure as dependências:
dotnet restore

### 3. Execute o projeto
dotnet run

A aplicação estará disponível em http://localhost:(porta) (a porta será exibida ao rodar a aplicação).

## Exemplo de Requisições

###Cadastrar Funcionário<br>
POST /api/funcionario/cadastrar<br>
Content-Type: application/json<br>
<br>
{<br>
    "nome": "João da Silva",<br>
    "cpf": "123.456.789-00"<br>
}<br>
<br><hr>

###Listar Funcionários <br>
GET /api/funcionario/listar<br>
<br><hr>

###Cadastrar Folha de Pagamento<br>
POST /api/folha/cadastrar<br>
Content-Type: application/json<br>
<br>
{<br>
    "quantidade": 1,<br>
    "valor": 5000,<br>
    "mes": 10,<br>
    "ano": 2024,<br>
    "funcionarioId": 1<br>
}<br>
<br>
# Conclusão
Esse projeto é um exemplo prático de como construir uma API utilizando C# e Entity Framework, além de ilustrar a manipulação de dados com operações CRUD.

