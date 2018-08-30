{
  "info": {
    "name": "Backupify Create a new backup_definition",
    "_postman_id": "61fcf362-eea6-4524-b953-c92805e096c1",
    "description": "Create a new backup_definition.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Oauth",
      "item": [
        {
          "id": "578be63f-0d66-4df2-af49-d48b3082f10c",
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
              "id": "f53f588f-0380-4d8e-9a92-0e99bb472afb"
            }
          ]
        }
      ]
    },
    {
      "name": "V1",
      "item": [
        {
          "id": "60572cb1-74e5-451e-a142-0800c8fb4e5d",
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
              "id": "39dc3be3-4d8d-4271-95c4-0e688e7f1803"
            }
          ]
        },
        {
          "id": "51620dee-220d-4983-b483-7c4f0c32ea05",
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
              "id": "488f3c91-759b-4d4f-8d28-fb7be87b19db"
            }
          ]
        },
        {
          "id": "3d216485-a161-401c-a348-441d62dfcf49",
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
              "id": "4cf27547-098d-462c-84a4-bc7157137eef"
            }
          ]
        },
        {
          "id": "f791c64a-634d-40e4-aba8-a2663c8bb394",
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
              "id": "b7211774-4dc3-4e06-89de-7492828ebef1"
            }
          ]
        }
      ]
    }
  ]
}