{
  "info": {
    "name": "Backupify A simple method to test authentication of a customer access token.",
    "_postman_id": "ab6564e7-ce86-4472-be68-b11d8fba2f25",
    "description": "A simple method to test authentication of a customer access token..",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "V1",
      "item": [
        {
          "id": "3be115df-a991-4ceb-85b9-fb2561b350f2",
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
              "id": "084798d2-1e6e-4db8-a803-623056741246"
            }
          ]
        }
      ]
    }
  ]
}