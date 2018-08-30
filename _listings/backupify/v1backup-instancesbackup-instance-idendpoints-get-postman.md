{
  "info": {
    "name": "Backupify Retrieve a list of endpoints for the specified backup_instance",
    "_postman_id": "563cf89f-40c7-4370-96a9-deb91587266d",
    "description": "You can only retrieve endpoints for backup_instances you have access to. Records are returned in ascending order (by id), with a default of 20 per page. Links to the next, previous, first, and last pages can be found in the response headers.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "V1",
      "item": [
        {
          "id": "5b37fb6b-1ccf-425e-84c4-6a8e5d193b26",
          "name": "getV1BackupInstancesBackupInstanceEndpoints",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.backupify.com",
              "path": [
                "v1/backup_instances/:backup_instance_id/endpoints"
              ],
              "variable": [
                {
                  "id": "backup_instance_id",
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
            "description": "You can only retrieve endpoints for backup_instances you have access to. Records are returned in ascending order (by id), with a default of 20 per page. Links to the next, previous, first, and last pages can be found in the response headers."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "47a34649-8b69-4aff-9543-27fbfb0a3648"
            }
          ]
        }
      ]
    }
  ]
}