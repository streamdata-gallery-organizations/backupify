{
  "info": {
    "name": "Backupify Retrieve a specific export for the specified backup_instance",
    "_postman_id": "7fd12ee6-cc34-4103-8991-14a17fd08044",
    "description": "You can only retrieve exports for backup_instances you have access to",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "V1",
      "item": [
        {
          "id": "21c9adba-a716-4b29-8752-78f8568aa1bb",
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
              "id": "32f8cbaf-067a-4630-a2fb-aeb15d966214"
            }
          ]
        },
        {
          "id": "ec64987a-7051-490e-8a5e-061c84581b9b",
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
              "id": "d9bb85f6-63f2-4c27-ae5b-94956cc96866"
            }
          ]
        },
        {
          "id": "19af4d44-2f41-4578-86fc-df454bacdd0e",
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
              "id": "58ab5913-7ce7-44e4-a32d-a25bef675bff"
            }
          ]
        },
        {
          "id": "dc9e7e3c-70b2-47f8-b5ea-87ca7cdb41cf",
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
              "id": "6b5632c0-b2f1-4441-abe6-254102d9fdbd"
            }
          ]
        },
        {
          "id": "b5976412-b56b-492d-a64a-c2c007a273e1",
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
              "id": "4b07657f-4c43-4271-9c97-629eabd03dbb"
            }
          ]
        },
        {
          "id": "558ccb95-b524-4cbb-9a63-4e6dda1aa20f",
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
              "id": "9bc565b1-e030-4625-b361-f94a73ccb1f4"
            }
          ]
        },
        {
          "id": "69435972-1f06-48f4-af13-195f2873930c",
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
              "id": "6fc5f07c-5cdb-4baf-be04-4f2945712a07"
            }
          ]
        },
        {
          "id": "4fc73579-108c-49a1-a95b-95446116d8cc",
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
              "id": "d0362aae-4a3b-406d-b2d1-413dc1f0fac9"
            }
          ]
        },
        {
          "id": "a5d40c3e-d951-4857-b5a5-71a733f90f92",
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
              "id": "5985fb66-5da4-4a63-bae4-8d6597d43458"
            }
          ]
        },
        {
          "id": "fc0cfaaf-73de-45e1-94c2-54a70a7e593c",
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
              "id": "a6b68333-e90e-4e5a-8e87-967b0eec5700"
            }
          ]
        },
        {
          "id": "e880e3dc-0bf2-4a8e-a4b5-965a1d987ef3",
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
              "id": "17c9aa82-b48b-42d5-8522-6a1efd1b35d5"
            }
          ]
        },
        {
          "id": "02ebf96e-deb5-4795-98dc-266f38491731",
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
              "id": "07983037-ba0b-4812-bd54-62dbb371ba9b"
            }
          ]
        },
        {
          "id": "6c8e4038-c23e-418a-8255-c6e12b0d288d",
          "name": "getV1BackupInstancesBackupInstanceEndpointsEndpointNameRecordsRecordBlob",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.backupify.com",
              "path": [
                "v1/backup_instances/:backup_instance_id/endpoints/:endpoint_name/records/:record_id/blob"
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
                "key": "Access-Token",
                "value": "{}",
                "description": "Access Token granted from client credentials authorizing vendor to perform action",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve the blob associated with the specified record for the specified endpoint and backup_instance."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "60cee5a6-fda4-4e7e-8225-524d87284aee"
            }
          ]
        },
        {
          "id": "51e843f8-2346-4976-b504-09349e5e200b",
          "name": "getV1BackupInstancesBackupInstanceExports",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.backupify.com",
              "path": [
                "v1/backup_instances/:backup_instance_id/exports"
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
            "description": "You can only retrieve exports for backup_instances you have access to. Records are returned in ascending order (by id), with a default of 20 per page. Links to the next, previous, first, and last pages can be found in the response headers."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "05737b84-0347-4f94-bffb-75f5e1094b9f"
            }
          ]
        },
        {
          "id": "7557c598-28b0-437e-bb95-a0ccf4f3f5b9",
          "name": "postV1BackupInstancesBackupInstanceExports",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.backupify.com",
              "path": [
                "v1/backup_instances/:backup_instance_id/exports"
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
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "export_run[backup_run_id]",
                  "value": "{}",
                  "disabled": false,
                  "description": "ID of a specific backup_run to export"
                },
                {
                  "key": "export_run[content_types]",
                  "value": "{}",
                  "disabled": false,
                  "description": "Comma separated list of blob content-types to export"
                },
                {
                  "key": "export_run[export_datetime]",
                  "value": "{}",
                  "disabled": false,
                  "description": "Date (format: YYYY-MM-DD) from which to export"
                },
                {
                  "key": "export_run[export_formats]",
                  "value": "{}",
                  "disabled": false,
                  "description": "Comma separated list of export format options"
                },
                {
                  "key": "export_run[force_full]",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag to force a full export, as opposed to re-authorizing an old export if the data is the same"
                },
                {
                  "key": "export_run[send_confirmation]",
                  "value": "{}",
                  "disabled": false,
                  "description": "Flag to send a confirmation email w/export link upon completion"
                }
              ]
            },
            "description": "Perform an export of the most recent backup of the specified backup_instance."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9fd7f798-c15f-4ebd-a84f-81f7f3ca93c4"
            }
          ]
        },
        {
          "id": "756ca41c-1821-45a3-987e-89db9a4c2624",
          "name": "getV1BackupInstancesBackupInstanceExportsExport",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.backupify.com",
              "path": [
                "v1/backup_instances/:backup_instance_id/exports/:export_id"
              ],
              "variable": [
                {
                  "id": "backup_instance_id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "export_id",
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
            "description": "You can only retrieve exports for backup_instances you have access to"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ba231e13-fb0c-4dc1-8a02-b908f35250c7"
            }
          ]
        }
      ]
    }
  ]
}