{
  "info": {
    "name": "Backupify Update a specific variable by key for the specified backup_definition",
    "_postman_id": "14cb2680-fa15-4977-addc-1ae3dd5c77f7",
    "description": "You can only update variables for backup_definitions you have access to. Additionally, it is not possible to update a variable's key. Requests including a modified key name will result in an error.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "V1",
      "item": [
        {
          "id": "29cfb290-3a3e-4904-a742-8b8754f8dbdf",
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
              "id": "77ec5128-9ae1-4bfc-91a1-e86f3d7d5c3d"
            }
          ]
        },
        {
          "id": "6c2b5195-f752-48ab-b762-b82682a335cb",
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
              "id": "cd3a81df-97e7-4b2b-8ce6-08a791116cbd"
            }
          ]
        },
        {
          "id": "954d8aa3-fc1b-4e59-97a9-120168506773",
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
              "id": "067ada20-8fd7-4c6e-8a52-408b873d5002"
            }
          ]
        },
        {
          "id": "baa3d5c5-8b14-42d7-91cf-ed52a6c8188a",
          "name": "putV1BackupDefinitionsBackupDefinitionVariablesKey",
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
                  "key": "name",
                  "value": "{}",
                  "disabled": false,
                  "description": "The human-friendly name to use for the variable"
                },
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
                  "key": "variable[optional]",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag indicating whether this variable is optional or if a value is required"
                }
              ]
            },
            "description": "You can only update variables for backup_definitions you have access to. Additionally, it is not possible to update a variable's key. Requests including a modified key name will result in an error."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3f206fd2-d551-47dd-88f5-e9668758af44"
            }
          ]
        }
      ]
    }
  ]
}