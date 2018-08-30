{
  "info": {
    "name": "Backupify Retrieve a specific record by id for the specified endpoint and backup_instance",
    "_postman_id": "ba018879-5515-4379-b7ce-cff1decc2174",
    "description": "You can only retrieve records for endpoints of backup_instances you have access to",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "V1",
      "item": [
        {
          "id": "1de7ec8b-caa8-463a-bebe-55a48ba21e49",
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
              "id": "208190b9-b1fc-4dad-9d7c-b751cc9b35af"
            }
          ]
        },
        {
          "id": "43e79f2b-7e1b-45f8-94d3-04ed0749c041",
          "name": "getV1BackupInstancesBackupInstanceEndpointsEndpointName",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.backupify.com",
              "path": [
                "v1/backup_instances/:backup_instance_id/endpoints/:endpoint_name"
              ],
              "variable": [
                {
                  "id": "backup_instance_id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "endpoint_name",
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
            "description": "You can only retrieve endpoints for backup_instances you have access to"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5c834f8a-3211-4cd5-becd-aad34665d9b9"
            }
          ]
        },
        {
          "id": "c1d041e6-cb8a-4f08-95da-89e210728737",
          "name": "getV1BackupInstancesBackupInstanceEndpointsEndpointNameRecords",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.backupify.com",
              "path": [
                "v1/backup_instances/:backup_instance_id/endpoints/:endpoint_name/records"
              ],
              "variable": [
                {
                  "id": "backup_instance_id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "endpoint_name",
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
            "description": "You can only retrieve records for endpoints that belong to backup_instances you have access to. Records are returned in ascending order (by id), with a default of 20 per page. Links to the next, previous, first, and last pages can be found in the response headers."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5c46b9dd-491a-46b6-810c-9d0f2c7fa666"
            }
          ]
        },
        {
          "id": "807c8f6b-00ef-4795-96de-68faac4930df",
          "name": "getV1BackupInstancesBackupInstanceEndpointsEndpointNameRecordsRecord",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.backupify.com",
              "path": [
                "v1/backup_instances/:backup_instance_id/endpoints/:endpoint_name/records/:record_id"
              ],
              "variable": [
                {
                  "id": "backup_instance_id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "endpoint_name",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "record_id",
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
            "description": "You can only retrieve records for endpoints of backup_instances you have access to"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a89cb556-aa08-462b-9e13-31c0533acaa3"
            }
          ]
        }
      ]
    }
  ]
}