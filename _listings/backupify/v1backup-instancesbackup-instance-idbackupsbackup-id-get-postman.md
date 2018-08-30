{
  "info": {
    "name": "Backupify Retrieve the specified backup for the specified backup_instance",
    "_postman_id": "d65e9cc9-65e5-47db-bd89-96ec4348437a",
    "description": "Only backups belonging to backup_instances you have permission to access can be retrieved",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "V1",
      "item": [
        {
          "id": "1a633e82-578c-4b6a-8396-9bd6811edc48",
          "name": "getV1BackupInstances",
          "request": {
            "url": "http://api.backupify.com/v1/backup_instances?backup_definition_id=%7B%7D",
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
            "description": "It is only possible to retrieve backup_instances for customers you are authorized to access. Records are returned in ascending order (by id), with a default of 20 per page. Links to the next, previous, first, and last pages can be found in the response headers."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a00675f8-08e0-42ba-9540-234f1686e0d2"
            }
          ]
        },
        {
          "id": "1ee637aa-ef5c-48dd-a683-d3a8d5d02912",
          "name": "postV1BackupInstances",
          "request": {
            "url": "http://api.backupify.com/v1/backup_instances",
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
                  "key": "backup_instance[backup_definition_id]",
                  "value": "{}",
                  "disabled": false,
                  "description": "ID of the backup_definition to create a backup_instance for"
                },
                {
                  "key": "backup_instance[backup_frequency]",
                  "value": "{}",
                  "disabled": false,
                  "description": "Frequency with which scheduled backups are performed"
                },
                {
                  "key": "backup_instance[customer_id]",
                  "value": "{}",
                  "disabled": false,
                  "description": "ID of the customer to create the backup_instance for"
                }
              ]
            },
            "description": "Create a new backup_instance from the specified backup_definition for the specified customer."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fefab860-adaa-493f-a246-d71b0224eb83"
            }
          ]
        },
        {
          "id": "d00f774a-2088-4bde-9255-8f03ec5397a7",
          "name": "getV1BackupInstancesBackupInstance",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.backupify.com",
              "path": [
                "v1/backup_instances/:backup_instance_id"
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
            "description": "Only backup_instances you have permission to view will be returned"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "531c8189-22c1-461b-afb3-c081ffa31c98"
            }
          ]
        },
        {
          "id": "1749e4d0-4778-4585-b3f5-85f3b7b3830a",
          "name": "putV1BackupInstancesBackupInstance",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.backupify.com",
              "path": [
                "v1/backup_instances/:backup_instance_id"
              ],
              "variable": [
                {
                  "id": "backup_instance_id",
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
                  "key": "backup_instance[backup_frequency]",
                  "value": "{}",
                  "disabled": false,
                  "description": "Frequency with which scheduled backups will be performed"
                }
              ]
            },
            "description": "Only backup_instances you have permission to change can be modified"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "17365789-d24f-4264-b660-d28be9f78a0b"
            }
          ]
        },
        {
          "id": "52bf3e06-d0fe-4395-9d65-e2eff9573390",
          "name": "getV1BackupInstancesBackupInstanceBackups",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.backupify.com",
              "path": [
                "v1/backup_instances/:backup_instance_id/backups"
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
            "description": "Only backups belonging to backup_instances you have permission to manage can be retrieved. Records are returned in ascending order (by id), with a default of 20 per page. Links to the next, previous, first, and last pages can be found in the response headers."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5dc3fd78-3649-4892-ad14-388752eb06a2"
            }
          ]
        },
        {
          "id": "a7ec9ffe-252a-46b2-846a-78b2f3d1b8d1",
          "name": "postV1BackupInstancesBackupInstanceBackups",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.backupify.com",
              "path": [
                "v1/backup_instances/:backup_instance_id/backups"
              ],
              "variable": [
                {
                  "id": "backup_instance_id",
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
              "mode": "raw"
            },
            "description": "Only backup_instances you have permission to manage can be backed up"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2f35ee41-0f71-47a1-bc35-9c1558ab5831"
            }
          ]
        },
        {
          "id": "1e756467-f450-4eb4-ac95-928a7782fad8",
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
              "id": "e2094b69-149c-4008-b60d-fb086a220a6d"
            }
          ]
        },
        {
          "id": "4162963e-c04a-4fb7-a58e-f37e6c019fbd",
          "name": "getV1BackupInstancesBackupInstanceBackupsBackup",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.backupify.com",
              "path": [
                "v1/backup_instances/:backup_instance_id/backups/:backup_id"
              ],
              "variable": [
                {
                  "id": "backup_id",
                  "value": "{}",
                  "type": "string"
                },
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
              "id": "34dfed14-ee20-43bc-89ba-10ce23859921"
            }
          ]
        }
      ]
    }
  ]
}