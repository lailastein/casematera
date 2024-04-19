# Case Matera

## Write an OpenAPI Specification for an Account API.
You have been assigned the task of documenting an API that allows users to register an alias for their bank account. In the US financial market, bank account numbers are considered sensitive information and cannot be shared publicly for security reasons. Instead, users can create an alias that represents their bank information. There are three options available for the user to choose from: email, phone number, or a randomly generated number. To ensure consistency and ease of use for developers who will be utilizing this API, you need to create an OpenAPI Specification (OAS) document using the following instructions:
1. Study the provided JSON document and scenario carefully to understand the structure of the account information required to register an alias.
2. Design an OpenAPI Specification document that defines this API.
3. Define the request/response schemas for this API.
4. Use the Swagger UI or any other tool to visualize and test the API.
5. Add one additional endpoint or functionality that would enhance the API’s capabilities.

```
{
  "accountAlias": {
      "alias": "johndoe@email.com",
      "aliasType": "EMAIL"
  },
  "account": {
      "id": "8f8as77c-9ffa-4177-95df-619b587c99ca",
      "type": "CHCK",
      "openinData": "2020-06-18"
  },
  "accounOwner": {
      "id": "0de30f85-084e-4753-953d-4c9217745d16",
      "fullName": "John Smith",
      "tradeName": "Oklahoma Gas & Eletric"
  }
}


```

## Case documentation
This OAS is use for registering an alias for a bank account. 

defines a POST endpoint at `/account/alias` for registering an alias for a bank account. The request body schema includes nested objects for `accountAlias`, `account`, and `accountOwner`. The `aliasType` property in the `AccountAlias` object is an enum representing the three options available for the user to choose from: email, phone, or random.

To enhance the API's capabilities, let's add an endpoint to retrieve account details using the alias:

Essa especificação OpenAPI define um endpoint POST em /conta/alias para registrar um alias para uma conta bancária. O esquema do corpo da solicitação inclui objetos aninhados para accountAlias, account e accountOwner. A propriedade aliasType no objeto AliasConta é um enum representando as três opções disponíveis para o usuário escolher: email, telefone ou aleatório.

Para aprimorar as capacidades da API, adicionamos um endpoint para recuperar os detalhes da conta usando o alias.

Este projeto é um sistema de gerenciamento desenvolvido em Java com Spring Boot, utilizando a arquitetura MVC. Ele oferece funcionalidades para cadastrar, listar e gerenciar informações de Pessoas, Usuários e Contas. A integração com um banco de dados PostgreSQL proporciona persistência segura e eficiente.
