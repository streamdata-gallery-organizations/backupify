{
  "info": {
    "name": "Backupify Retrieve a list of variables for the specified backup_definition",
    "_postman_id": "a61832a4-5bfd-430f-95b2-aa700d6fc933",
    "description": "You can only retrieve variables for backup_definitions you have access to. Records are returned in ascending order (by id), with a default of 20 per page. Links to the next, previous, first, and last pages can be found in the response headers.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "V1",
      "item": [
        {
          "id": "b4845a5c-b6ae-43c9-ae36-5a5a8aa7d9c2",
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
              "id": "917a7ec4-2c9f-4505-9937-5617b75edeb6"
            }
          ]
        }
      ]
    }
  ]
}