# Case Matera

Write an OpenAPI Specification for an Account API.
You have been assigned the task of documenting an API that allows users to register an alias for their bank account. In the US financial market, bank account numbers are considered sensitive information and cannot be shared publicly for security reasons. Instead, users can create an alias that represents their bank information. There are three options available for the user to choose from: email, phone number, or a randomly generated number. To ensure consistency and ease of use for developers who will be utilizing this API, you need to create an OpenAPI Specification (OAS) document using the following instructions:
1. Study the provided JSON document and scenario carefully to understand the structure of the account information required to register an alias.
2. Design an OpenAPI Specification document that defines this API.
3. Define the request/response schemas for this API.
4. Use the Swagger UI or any other tool to visualize and test the API.
5. Add one additional endpoint or functionality that would enhance the API’s capabilities.

> {
>   "accountAlias": {
>       "alias": "johndoe@email.com",
>       "aliasType": "EMAIL"
>   },
>   "account": {
>       "id": "8f8as77c-9ffa-4177-95df-619b587c99ca",
>       "type": "CHCK",
>       "openinData": "2020-06-18"
>   },
>   "accounOwner": {
>       "id": "0de30f85-084e-4753-953d-4c9217745d16",
>       "fullName": "John Smith",
>       "tradeName": "Oklahoma Gas & Eletric"
>   }
> }
