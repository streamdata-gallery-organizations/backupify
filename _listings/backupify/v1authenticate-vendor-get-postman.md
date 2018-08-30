{
  "info": {
    "name": "Backupify A simple method to test authentication of a vendor access token. The response body is empty JSON object.",
    "_postman_id": "7dd84566-151a-4528-89c5-7a1f400c443a",
    "description": "A simple method to test authentication of a vendor access token. the response body is empty json object..",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Oauth",
      "item": [
        {
          "id": "dac93e97-ff35-4309-a09b-7cfa69805ad3",
          "name": "postOauthToken",
          "request": {
            "url": "http://api.backupify.com/oauth/token",
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "client_id",
                  "value": "{}",
                  "disabled": false,
                  "description": "API Client ID"
                },
                {
                  "key": "client_secret",
                  "value": "{}",
                  "disabled": false,
                  "description": "API Client secret"
                },
                {
                  "key": "grant_type",
                  "value": "{}",
                  "disabled": false,
                  "description": "String identifying the grant type to be used for token retrieval"
                },
                {
                  "key": "scope",
                  "value": "{}",
                  "disabled": false,
                  "description": "A space separated list of operational scopes available to the returned token"
                }
              ]
            },
            "description": "All actions and visibility is limited in scope to items that are descendents of the authenticated vendor and the backup_definitions owned thereby. At this time, all Access Tokens are scoped with full write capabilities."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c26f9bca-b787-4814-94f8-8af20da9c107"
            }
          ]
        }
      ]
    },
    {
      "name": "V1",
      "item": [
        {
          "id": "25e0dff8-9e3b-4c7d-b12e-bcfaa8955df3",
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
              "id": "e73c0bab-e540-41f2-a8a3-9442a0c39f99"
            }
          ]
        },
        {
          "id": "c60ea57b-2bb3-41dc-b55b-3b8bcabd883c",
          "name": "getV1AuthenticateVendor",
          "request": {
            "url": "http://api.backupify.com/v1/authenticate_vendor",
            "method": "GET",
            "header": [
              {
                "key": "Authorization",
                "value": "{}",
                "description": "Bearer Access Token granted from client_credentials for vendor",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "A simple method to test authentication of a vendor access token. the response body is empty json object.."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1a2fdc21-16ae-49ea-97e5-6de5a0b96bb7"
            }
          ]
        }
      ]
    }
  ]
}