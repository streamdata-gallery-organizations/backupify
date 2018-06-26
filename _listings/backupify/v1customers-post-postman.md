{
  "info": {
    "name": "Backupify Create a new customer instance identified by the given {name} identifier",
    "_postman_id": "66590189-a672-4cb7-bb38-cfe606e8ad83",
    "description": "Create a new customer instance identified by the given {name} identifier.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "V1",
      "item": [
        {
          "id": "03e51704-a9cc-4c0a-8fbe-d5177d2f3b1f",
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
              "id": "d0a31e55-5477-4e0b-8884-c0e365c48506"
            }
          ]
        },
        {
          "id": "b59abf6b-194e-44d3-a036-41b87259c720",
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
              "id": "52b434fb-2241-4477-9f91-b57c6da67e35"
            }
          ]
        },
        {
          "id": "6197285e-7e54-492c-bb1c-5fb5fdad2901",
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
              "id": "75ffa14d-f395-40c8-81a1-59945faab916"
            }
          ]
        }
      ]
    }
  ]
}