{
  "info": {
    "name": "Backupify Retrieve an index of all backup_definitions",
    "_postman_id": "bdf53dcc-773b-4ce6-83f3-69ac0fbe8711",
    "description": "This will retrieve a list of backup_defintions from all vendors. To view backup_defintions for a particular vendor, see the vendors API. Records are returned in ascending order (by id), with a default of 20 per page. Links to the next, previous, first, and last pages can be found in the response headers.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Oauth",
      "item": [
        {
          "id": "c7fc3104-e392-4faf-8b65-28223133acc2",
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
              "id": "003d8dbd-4350-4868-9528-3801e7d1c352"
            }
          ]
        }
      ]
    },
    {
      "name": "V1",
      "item": [
        {
          "id": "e7c2fe5c-d818-4f2e-900a-43896ad0ba92",
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
              "id": "a9be5481-db2d-4b0f-8d56-183ded289188"
            }
          ]
        },
        {
          "id": "77bf1266-a7e1-4a8b-bbce-7e454baefe02",
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
              "id": "1d065610-ffdd-4cb1-a9b9-49d989a8aef6"
            }
          ]
        },
        {
          "id": "603b57db-5747-4a54-8885-bb2408d7caa8",
          "name": "getV1BackupDefinitions",
          "request": {
            "url": "http://api.backupify.com/v1/backup_definitions?vendor_id=%7B%7D",
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
            "description": "This will retrieve a list of backup_defintions from all vendors. To view backup_defintions for a particular vendor, see the vendors API. Records are returned in ascending order (by id), with a default of 20 per page. Links to the next, previous, first, and last pages can be found in the response headers."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a93f75a1-c94b-4c39-8e6a-f55cd1782190"
            }
          ]
        }
      ]
    }
  ]
}