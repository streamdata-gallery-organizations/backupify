{
  "info": {
    "name": "Backupify Retrieve an updated exported_data_url for a specific export for the specified backup_instance",
    "_postman_id": "c20fc7c1-3ef5-42a0-8b3f-f9ee9b1ef553",
    "description": "Retrieve an updated exported_data_url for a specific export for the specified backup_instance.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "V1",
      "item": [
        {
          "id": "6a8cebb5-b54c-4e91-8da5-12de9f06b07f",
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
              "id": "76ed1f1b-67dc-415e-901e-751545ceb320"
            }
          ]
        },
        {
          "id": "fef83cbe-7b0d-4354-b4cf-735abbe9eb57",
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
              "id": "50e14557-9090-4cd9-af30-343bff5edc01"
            }
          ]
        },
        {
          "id": "05ac9856-0d5c-4572-9b6d-310b2d5792d7",
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
              "id": "0fde1bde-7cd3-4f81-9f9e-a11004258af6"
            }
          ]
        },
        {
          "id": "5ed93c51-3778-428c-a9f1-6741b22fd369",
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
              "id": "998b3da3-a2e6-4bfe-ae08-139c0f596a36"
            }
          ]
        },
        {
          "id": "66421937-6acd-4110-b0b3-8758fbc1ea3e",
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
              "id": "c515e722-d5a9-4387-a4dd-e8bd5e4fdd9f"
            }
          ]
        },
        {
          "id": "37e7fd2b-cc4e-429d-86e1-0bc8488f2a4e",
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
              "id": "95d20d56-9f78-4615-8060-00ea8d6453b5"
            }
          ]
        },
        {
          "id": "c6b0fdb4-a8f8-4404-88e0-86f6004ee6e1",
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
              "id": "7123c00e-d81a-4713-a18b-73b48cea3086"
            }
          ]
        },
        {
          "id": "99439302-5db4-401e-b148-3d78763d7843",
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
              "id": "cfa4cd7d-4689-46cd-a552-119562da5206"
            }
          ]
        },
        {
          "id": "b4fdae8a-7723-4825-b987-de6ced01abd6",
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
              "id": "9810e8c8-23b3-40a7-b3fe-343df54a90df"
            }
          ]
        },
        {
          "id": "43f50664-3860-48ef-86cd-3e4be1e12d27",
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
              "id": "2237f444-b7fc-4fa5-8be7-2769a7e64f45"
            }
          ]
        },
        {
          "id": "42feec1e-a336-4410-9741-6c374ef2745b",
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
              "id": "20be5680-a45a-42c9-af72-fb980a129079"
            }
          ]
        },
        {
          "id": "849c9349-d5a4-4c74-b47b-c85011aeb123",
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
              "id": "4e2f190b-db50-4afd-b542-5eea6d9c1d02"
            }
          ]
        },
        {
          "id": "09889165-5851-4328-9c7e-74c6697170e4",
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
              "id": "cb0ca685-e504-4396-8eaa-b71823e5c746"
            }
          ]
        },
        {
          "id": "3316d6d1-2820-4758-b909-b1cb900493ba",
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
              "id": "c2d2f2b7-b5cd-498f-a0fd-d961621d8d96"
            }
          ]
        },
        {
          "id": "715e5137-3a34-4857-8388-d843c8967e61",
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
              "id": "8b01c26d-171f-4951-b154-aceee8c6928f"
            }
          ]
        },
        {
          "id": "7c9f7cd8-c388-472e-b56c-efd5e9ae338f",
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
              "id": "4c796482-3d4a-46c4-9455-8fccbd7b4470"
            }
          ]
        },
        {
          "id": "886604be-e4cb-45df-88fb-cb1f01928a62",
          "name": "postV1BackupInstancesBackupInstanceExportsExportReauth",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.backupify.com",
              "path": [
                "v1/backup_instances/:backup_instance_id/exports/:export_id/reauth"
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
            "description": "Retrieve an updated exported_data_url for a specific export for the specified backup_instance."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b00ed4eb-25c3-40f0-91a4-bcf418e87ffd"
            }
          ]
        }
      ]
    }
  ]
}