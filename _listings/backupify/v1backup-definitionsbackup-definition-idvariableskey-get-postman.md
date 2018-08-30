{
  "info": {
    "name": "Backupify Retrieve a specific variable by key for the specified backup_definition",
    "_postman_id": "09ba46e9-5432-4473-8c60-01247083bf0d",
    "description": "You can only retrieve variables for backup_definitions you have access to",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "V1",
      "item": [
        {
          "id": "1b9f6e77-ae00-4699-99c3-ced4419ff022",
          "name": "getV1BackupDefinitionsBackupDefinitionVariables",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.backupify.com",
              "path": [
                "v1/backup_definitions/:backup_definition_id/variables"
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
            "description": "You can only retrieve variables for backup_definitions you have access to. Records are returned in ascending order (by id), with a default of 20 per page. Links to the next, previous, first, and last pages can be found in the response headers."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "84619222-b40e-4a0c-8457-4557ccef7e69"
            }
          ]
        },
        {
          "id": "f6964fac-6dcb-4bdb-9271-e9eb79cb66f4",
          "name": "postV1BackupDefinitionsBackupDefinitionVariables",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.backupify.com",
              "path": [
                "v1/backup_definitions/:backup_definition_id/variables"
              ],
              "variable": [
                {
                  "id": "backup_definition_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
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
                  "key": "variable[default_value]",
                  "value": "{}",
                  "disabled": false,
                  "description": "A default value that can be used when no instance specific value is provided"
                },
                {
                  "key": "variable[description]",
                  "value": "{}",
                  "disabled": false,
                  "description": "Description offering additional information or detail about the variable"
                },
                {
                  "key": "variable[key]",
                  "value": "{}",
                  "disabled": false,
                  "description": "The symbolic name or identifier to access the defined variable by"
                },
                {
                  "key": "variable[name]",
                  "value": "{}",
                  "disabled": false,
                  "description": "A human-friendly name for the variable"
                },
                {
                  "key": "variable[optional]",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag indicating whether this variable is optional or if a value is required"
                }
              ]
            },
            "description": "It is only possible to create variables for backup_definitions you have permission to manage."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d4f3d131-3334-4796-9622-cb6f98ca0c18"
            }
          ]
        },
        {
          "id": "66d6d86b-89a4-45d1-95f9-353a305a118f",
          "name": "getV1BackupDefinitionsBackupDefinitionVariablesKey",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.backupify.com",
              "path": [
                "v1/backup_definitions/:backup_definition_id/variables/:key"
              ],
              "variable": [
                {
                  "id": "backup_definition_id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "key",
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
            "description": "You can only retrieve variables for backup_definitions you have access to"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6e7f0c4f-0851-4b56-b117-7fdc6378eda9"
            }
          ]
        }
      ]
    }
  ]
}