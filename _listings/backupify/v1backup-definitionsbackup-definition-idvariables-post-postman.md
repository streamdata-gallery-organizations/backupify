{
  "info": {
    "name": "Backupify Create a new variable for the specified key for the specified backup_definition",
    "_postman_id": "72ca15b5-bf8f-44da-9577-b72903365b21",
    "description": "It is only possible to create variables for backup_definitions you have permission to manage.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "V1",
      "item": [
        {
          "id": "7aab43b3-9e5d-4928-b4a1-b6151a07b0ee",
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
              "id": "c6fc8899-6d1a-44d5-8ac6-2fb4ec1b3e3f"
            }
          ]
        },
        {
          "id": "4e5fdda6-21e5-4604-8f89-a6bc2189a440",
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
              "id": "f9925766-ccbc-4505-92dc-9631beb23f24"
            }
          ]
        }
      ]
    }
  ]
}