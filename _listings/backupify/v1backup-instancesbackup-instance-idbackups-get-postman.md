{
  "info": {
    "name": "Backupify Retrieve a list of all backups for the specified backup_instance.",
    "_postman_id": "f032f884-e832-43e6-8352-34876535b846",
    "description": "Only backups belonging to backup_instances you have permission to manage can be retrieved. Records are returned in ascending order (by id), with a default of 20 per page. Links to the next, previous, first, and last pages can be found in the response headers.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "V1",
      "item": [
        {
          "id": "c5349692-b86b-455d-8171-daa688c710fb",
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
              "id": "f955a6c6-cd2a-457b-abfd-309a47733857"
            }
          ]
        },
        {
          "id": "ad527318-fc4a-425c-a57a-683173b37bff",
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
              "id": "1cb84d35-1053-4a09-abee-b80ed762a2e3"
            }
          ]
        },
        {
          "id": "0b17f10d-5613-4f1b-abef-621ad865bd75",
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
              "id": "a5a0a49d-9e48-4ed6-8f8a-06f1d6af97aa"
            }
          ]
        },
        {
          "id": "8d94f7c3-642c-4445-a0c3-ac725afee297",
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
              "id": "e94aaaf6-0732-43f6-b5af-4e517b903cb6"
            }
          ]
        },
        {
          "id": "01d21aa6-028b-461d-879d-d53908d91098",
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
              "id": "e7868bd1-295a-4f34-a9a7-c5db97bcdef7"
            }
          ]
        }
      ]
    }
  ]
}