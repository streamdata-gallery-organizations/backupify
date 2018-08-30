{
  "info": {
    "name": "Backupify Update the specified backup_definition",
    "_postman_id": "c273482c-4067-4418-ba07-84772045cc77",
    "description": "Only backup_definitions you have permission to change can be modified",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Oauth",
      "item": [
        {
          "id": "a6f8451f-e6b7-444c-b8c3-51d34c0ab253",
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
              "id": "6efa5f68-e0c6-46fb-bf25-a1cbee03d138"
            }
          ]
        }
      ]
    },
    {
      "name": "V1",
      "item": [
        {
          "id": "4c1ee04f-16f6-4a41-bf57-41c8e84fc396",
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
              "id": "f2281104-bdc5-4a37-a805-f82ed919ff61"
            }
          ]
        },
        {
          "id": "3bbc846e-6fda-49fb-ac5d-e69e39981bbc",
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
              "id": "da93c619-c191-47ea-8dea-7ac0857f239a"
            }
          ]
        },
        {
          "id": "71cd2f83-e513-4cee-a88d-10f56939e084",
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
              "id": "46043fc9-8c71-4fef-b611-abb1bdb82709"
            }
          ]
        },
        {
          "id": "a8cf52ae-13af-43f4-81e9-eac0613c5874",
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
              "id": "e7b757b5-e4a0-4b42-9674-752bab92c43c"
            }
          ]
        },
        {
          "id": "f17850a0-fd3f-41e2-af17-1549888675ea",
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
              "id": "317f71f7-4ac9-4c14-85e4-9f11cae0b96c"
            }
          ]
        },
        {
          "id": "f6aa0ad7-7dda-4cbf-9fe2-030a020b1654",
          "name": "putV1BackupDefinitionsBackupDefinition",
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
            "description": "Only backup_definitions you have permission to change can be modified"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9d37a0f1-6388-4595-96b5-0880f41b14be"
            }
          ]
        }
      ]
    }
  ]
}