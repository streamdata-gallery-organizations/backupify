{
  "info": {
    "name": "Backupify Retrieve a backup_definition by backup_definition_id",
    "_postman_id": "62f8a0a0-5cbf-4772-9716-e39023a5e868",
    "description": "Only backup_definitions you have permission to view will be returned",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Oauth",
      "item": [
        {
          "id": "14697cf0-8f23-45bf-ad66-12fad909ebac",
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
              "id": "e8b3f811-e6fd-4037-8db5-80611fe76331"
            }
          ]
        }
      ]
    },
    {
      "name": "V1",
      "item": [
        {
          "id": "cf7bd854-5f60-46bd-89c4-f9d914247c0d",
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
              "id": "2999c58f-58d2-4a8d-aad7-bd22b0474546"
            }
          ]
        },
        {
          "id": "cedd74ce-4cfb-4bba-a80c-805976b3d35a",
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
              "id": "6270c3ab-203b-42ba-a7f3-a8f42c7c6b66"
            }
          ]
        },
        {
          "id": "d000bf7f-6a41-4d14-a64f-86e25a1e2aec",
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
              "id": "79674917-016f-498e-9fb3-e6440ec5c1b1"
            }
          ]
        },
        {
          "id": "8bd19c6b-673f-4310-8dbf-7c06addb7093",
          "name": "postV1BackupDefinitions",
          "request": {
            "url": "http://api.backupify.com/v1/backup_definitions",
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
                  "key": "backup_definition[description]",
                  "value": "{}",
                  "disabled": false,
                  "description": "Description of the backup_definition"
                },
                {
                  "key": "backup_definition[name]",
                  "value": "{}",
                  "disabled": false,
                  "description": "Name for the backup_definition"
                },
                {
                  "key": "backup_definition[published]",
                  "value": "{}",
                  "disabled": false,
                  "description": "Boolean flag indicating whether the backup definition is published and available for use"
                }
              ]
            },
            "description": "Create a new backup_definition."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e848a734-6541-46c9-a26b-8405aa111365"
            }
          ]
        },
        {
          "id": "75e272b6-24af-4c18-a9f2-74f2e0ee7c6c",
          "name": "getV1BackupDefinitionsBackupDefinition",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.backupify.com",
              "path": [
                "v1/backup_definitions/:backup_definition_id"
              ],
              "variable": [
                {
                  "id": "backup_definition_id",
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
            "description": "Only backup_definitions you have permission to view will be returned"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "40dd38f1-efaf-4bb1-a1cf-6542770014f0"
            }
          ]
        }
      ]
    }
  ]
}