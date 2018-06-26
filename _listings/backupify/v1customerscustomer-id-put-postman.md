{
  "info": {
    "name": "Backupify Update a customer instance identified by the given customer_id",
    "_postman_id": "2d674de1-7f63-4afd-96cc-fd1f6a37cc5f",
    "description": "Update a customer instance identified by the given customer_id.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "V1",
      "item": [
        {
          "id": "842feefd-d290-49d0-9a95-35ea483d6ab7",
          "name": "getV1AuthenticateCustomer",
          "request": {
            "url": "http://api.backupify.com/v1/authenticate_customer",
            "method": "GET",
            "header": [
              {
                "key": "Authorization",
                "value": "{}",
                "description": "Bearer Access Token granted for customer",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "A simple method to test authentication of a customer access token.."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e77023a5-3f75-46a2-9867-bc4e84cea72e"
            }
          ]
        },
        {
          "id": "035c569c-a0e1-4a0f-8e16-9df746612725",
          "name": "getV1Customers",
          "request": {
            "url": "http://api.backupify.com/v1/customers",
            "method": "GET",
            "header": [
              {
                "key": "Authorization",
                "value": "{}",
                "description": "Bearer Access Token granted from client credentials authorizing vendor to perform action",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Requires Access Token granted from client credentials. Records are returned in ascending order (by id), with a default of 20 per page. Links to the next, previous, first, and last pages can be found in the response headers."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "947d8b34-a2c8-4937-a0c6-ce27109d7fc0"
            }
          ]
        },
        {
          "id": "3210f673-8d6b-495b-917e-c9da89a5c5cb",
          "name": "postV1Customers",
          "request": {
            "url": "http://api.backupify.com/v1/customers",
            "method": "POST",
            "header": [
              {
                "key": "Authorization",
                "value": "{}",
                "description": "Bearer Access Token granted from client credentials authorizing vendor to perform action",
                "disabled": false
              }
            ],
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "customer[email]",
                  "value": "{}",
                  "disabled": false,
                  "description": "Email address associated with the customer"
                },
                {
                  "key": "customer[name]",
                  "value": "{}",
                  "disabled": false,
                  "description": "Vendor provided ID uniquely identifying customer"
                }
              ]
            },
            "description": "Create a new customer instance identified by the given {name} identifier."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "761639ea-cd2e-478d-8f35-34d486c5d0e9"
            }
          ]
        },
        {
          "id": "68fb0364-4169-4f7c-8200-a122d9188c64",
          "name": "getV1CustomersCustomer",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.backupify.com",
              "path": [
                "v1/customers/:customer_id"
              ],
              "variable": [
                {
                  "id": "customer_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Authorization",
                "value": "{}",
                "description": "Bearer Access Token granted from client credentials authorizing vendor to perform action",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Requires Access Token granted from client credentials."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "724ce147-2b00-458d-b337-677535096fb4"
            }
          ]
        },
        {
          "id": "d550a511-df4b-4f96-a52f-b7b549647a4b",
          "name": "putV1CustomersCustomer",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.backupify.com",
              "path": [
                "v1/customers/:customer_id"
              ],
              "variable": [
                {
                  "id": "customer_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
            "header": [
              {
                "key": "Authorization",
                "value": "{}",
                "description": "Bearer Access Token granted from client credentials authorizing vendor to perform action",
                "disabled": false
              }
            ],
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "customer[name]",
                  "value": "{}",
                  "disabled": false,
                  "description": "Vendor provided ID uniquely identifying customer"
                }
              ]
            },
            "description": "Update a customer instance identified by the given customer_id."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "efa1e8b6-d052-4fc9-ac13-fddba8d19cd7"
            }
          ]
        }
      ]
    }
  ]
}