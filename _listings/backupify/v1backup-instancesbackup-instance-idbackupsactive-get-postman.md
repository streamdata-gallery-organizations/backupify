{
  "info": {
    "name": "Backupify Retrieve the active backup for the specified backup_instance if one exists",
    "_postman_id": "23f0ac39-6186-45f2-8bce-e7524fdb4aeb",
    "description": "Only backups belonging to backup_instances you have permission to access can be retrieved",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "V1",
      "item": [
        {
          "id": "09ec0963-1268-40e0-9726-465bd8872b74",
          "name": "getV1BackupInstancesBackupInstanceBackupsActive",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.backupify.com",
              "path": [
                "v1/backup_instances/:backup_instance_id/backups/active"
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
            "description": "Only backups belonging to backup_instances you have permission to access can be retrieved"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3bbc63af-4ff0-4e81-ac62-44db3095a294"
            }
          ]
        }
      ]
    }
  ]
}