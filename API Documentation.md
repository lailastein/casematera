# OpenAPI Specification for Account Alias API

## Table of contents
- [1. Introduction](#1-introduction)
- [2.  Overview](#2-overview)
- [3. Request/Response Schemas](#3-request/Response-Schemas)
    + [3.1 Request Schema](#31-request-schema)
    + [3.2 Response Schema](#32-response-schema)
- [4. Additional Endpoint](#4-Additional-Endpoint)
- [5. Conclusion](#5-Conclusion)
- [6. Implementation](#6-Implementation)
- [7. Testing](#7-Testing)
- [8. Security](#8-Security)
- [9. Maintenance](#9-Maintenance)
- [10. Documentation](#10-Documentation)


## **1. Introduction**

This OpenAPI Specification (OAS) document defines an API that allows users to register an alias for their bank account. The alias is a string of letters and numbers that are used to represent the account number. The alias is then used instead of the actual account number when making transactions or sharing account information with others.

## **2. Overview**

The API consists of a single endpoint:

* `POST /api/v1/account-aliases`

This endpoint is used to create a new account alias. The request body contains the account information and the desired alias type. The response body contains the alias ID and a confirmation message.

## **3. Request/Response Schemas**

### 3.1 Request Schema

```json
{
  "accountAlias": {
    "alias": "string",
    "aliasType": "string"
  },
  "account": {
    "id": "string",
    "type": "string",
    "openingDate": "string"
  },
  "accountOwner": {
    "id": "string",
    "fullName": "string",
    "tradeName": "string"
  }
}
```

**Properties:**

* `accountAlias`:
    * `alias`: The desired alias for the bank account.
    * `aliasType`: The type of alias to create. Valid values are `EMAIL`, `PHONE`, and `RANDOM`.

* `account`:
    * `id`: The ID of the bank account.
    * `type`: The type of bank account. Valid values are `CHECKING`, `SAVINGS`, and `LOAN`.
    * `openingDate`: The date the account was opened.

* `accountOwner`:
    * `id`: The ID of the bank account owner.
    * `fullName`: The full name of the bank account owner.
    * `tradeName`: The trade name of the bank account owner (if applicable).

### 3.2 Response Schema

```json
{
  "aliasId": "string",
  "message": "string"
}
```

**Properties:**

* `aliasId`: The ID of the newly created account alias.
* `message`: A confirmation message.

## **4. Additional Endpoint**

In addition to the existing endpoint, the following endpoint could be added to the API to enhance its capabilities:

* `GET /api/v1/account-aliases/{aliasId}`

This endpoint would be used to retrieve information about a specific account alias. The request body would contain the alias ID, and the response body would contain the alias information.

## **5. Conclusion**

This OpenAPI Specification defines a simple and easy-to-use API for registering account aliases. The API is consistent with other APIs and is easy for developers to understand and use. The additional endpoint that was suggested would further enhance the API's capabilities and make it more valuable to users.

## **6. Implementation**

The API can be implemented using a variety of programming languages and frameworks. Some popular options include:

* Java with Spring Boot
* Python with Flask
* JavaScript with Node.js

The API can be deployed to a variety of cloud platforms, such as Amazon Web Services (AWS), Google Cloud Platform (GCP), and Microsoft Azure.

## **7. Testing**

The API can be tested using a variety of tools and techniques, such as:

* Unit tests
* Integration tests
* End-to-end tests

The API can also be tested using a variety of test automation tools, such as Selenium and Cypress.

## **8. Security**

The API should be secured using a variety of security measures, such as:

* Authentication
* Authorization
* Encryption

The API should also be monitored for security threats and vulnerabilities.

## **9. Maintenance**

The API should be maintained regularly to ensure that it is up-to-date and secure.

The API should also be monitored for performance and scalability.

##**10. Documentation**

Documentation was also done through [Swagger UI](https://app.swaggerhub.com/apis-docs/LAILAPINHEIROO/Casemateraa/1.0).
