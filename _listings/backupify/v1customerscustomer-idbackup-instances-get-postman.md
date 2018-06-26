{
  "info": {
    "name": "Backupify Retrieves a list of backup_instances associated with the specified customer",
    "_postman_id": "ed498ef1-6454-4384-9215-a57772d6ab09",
    "description": "It is only possible to retrieve backup_instances for customers you are authorized to access. Records are returned in ascending order (by id), with a default of 20 per page. Links to the next, previous, first, and last pages can be found in the response headers.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "V1",
      "item": [
        {
          "id": "06517637-c1bb-4c28-bad3-0a74f16f95ee",
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
              "id": "899dc3f4-3cd9-4ec8-be8b-665b1c750261"
            }
          ]
        },
        {
          "id": "3019d5e7-a48c-4327-b930-9222ba59133a",
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
              "id": "dae70621-9263-44ee-b9dd-f5a3a603b9b5"
            }
          ]
        },
        {
          "id": "39f8a4a8-e3ca-4f77-871f-31044ce7ab28",
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
              "id": "30a70ca2-8a9e-4e28-aaab-27fab6b803c5"
            }
          ]
        },
        {
          "id": "55f0408c-b8a1-450a-a41b-2bb64b69e56d",
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
              "id": "3ba5875b-f6b7-4c11-85e4-547e74c72c8d"
            }
          ]
        },
        {
          "id": "a9bd6fa7-40b0-4bdb-bdaa-659c516d8cb2",
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
              "id": "d5b3f4d6-25cc-4ec0-8788-85c46f0bb876"
            }
          ]
        },
        {
          "id": "cfd77c0c-daf0-4ded-a117-cf94ce5c0f6b",
          "name": "getV1CustomersCustomerBackupInstances",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.backupify.com",
              "path": [
                "v1/customers/:customer_id/backup_instances"
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
            "description": "It is only possible to retrieve backup_instances for customers you are authorized to access. Records are returned in ascending order (by id), with a default of 20 per page. Links to the next, previous, first, and last pages can be found in the response headers."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "55e20e91-746f-425f-9b04-b1b24c140b08"
            }
          ]
        }
      ]
    }
  ]
}