# OpenAPI Specification for Account Alias API

## Table of contents
- [1. Introduction](#1-introduction)
- [2.  API Information](#2-API-Information)
- [3. Server](#3.-Server)
- [4. Overview](#4-Overview)
- [5. Request/Response Schemas](#3-request/Response-Schemas)
    + [5.1 Request Schema](#31-request-schema)
    + [5.2 Response Schema](#32-response-schema)
- [6. Additional Endpoint](#4-Additional-Endpoint)
- [7. Conclusion](#5-Conclusion)
- [8. Implementation](#6-Implementation)
- [9. Testing](#7-Testing)
- [10. Security](#8-Security)
- [11. Maintenance](#9-Maintenance)
- [12. Documentation](#10-Documentation)


## **1. Introduction**

This OpenAPI Specification (OAS) document defines an API that allows users to register an alias for their bank account. The alias is a string of letters and numbers that are used to represent the account number. The alias is then used instead of the actual account number when making transactions or sharing account information with others.

## **2.API Information**

- **Title:** Account Alias API
- **Description:** An API for registering aliases for bank accounts
- **Version:** 1.0.0

## **3. Server**

**URL:** https://api.example.com/v1

## **4. Overview**

The API provides two endpoints:

**Register Account Alias**

`POST /account/alias`: This endpoint allows you to register a new alias for a bank account.

**Retrieve Account Details by Alias**

`GET /account/details`: This endpoint allows you to retrieve the details of a bank account associated with a specific alias.

## **5. Request/Response Schemas**

### 5.1 Request Schema for endpoint `POST /account/alias`

```json
{
  "accountAlias": {
    "alias": "my-savings",
    "aliasType": "email"
  },
  "account": {
    "id": "acc_123456",
    "type": "savings",
    "openingDate": "2023-01-01"
  },
  "accountOwner": {
    "id": "owner_789012",
    "fullName": "John Doe"
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

### 5.2 Response Schema for endpoint `POST /account/alias`

**Response Codes**

200: The alias was successfully registered.
400: Bad request. This could be due to invalid data in the request body or missing required fields.

```json
{
  "description": "Alias successfully registered"
}
```

**Properties:**

* `aliasId`: The ID of the newly created account alias.
* `message`: A confirmation message.

## **6. Additional Endpoint**

In addition to the existing endpoint, the following endpoint could be added to the API to enhance its capabilities:

* `GET /api/v1/account-aliases/{aliasId}`

This endpoint would be used to retrieve information about a specific account alias. The request body would contain the alias ID, and the response body would contain the alias information.

## **7. Conclusion**

This OpenAPI Specification defines a simple and easy-to-use API for registering account aliases. The API is consistent with other APIs and is easy for developers to understand and use. The additional endpoint that was suggested would further enhance the API's capabilities and make it more valuable to users.

## **8. Implementation**

The API can be implemented using a variety of programming languages and frameworks. Some popular options include:

* Java with Spring Boot
* Python with Flask
* JavaScript with Node.js

The API can be deployed to a variety of cloud platforms, such as Amazon Web Services (AWS), Google Cloud Platform (GCP), and Microsoft Azure.

## **9. Testing**

The API can be tested using a variety of tools and techniques, such as:

* Unit tests
* Integration tests
* End-to-end tests

The API can also be tested using a variety of test automation tools, such as Selenium and Cypress.

## **10. Security**

The API should be secured using a variety of security measures, such as:

* Authentication
* Authorization
* Encryption

The API should also be monitored for security threats and vulnerabilities.

## **11. Maintenance**

The API should be maintained regularly to ensure that it is up-to-date and secure.

The API should also be monitored for performance and scalability.

## **12. Documentation**

Documentation was also done through [Swagger UI](https://app.swaggerhub.com/apis-docs/LAILAPINHEIROO/Casemateraa/1.0).
