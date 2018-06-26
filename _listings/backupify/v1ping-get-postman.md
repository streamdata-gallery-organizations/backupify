{
  "info": {
    "name": "Backupify A simple method that returns a 200 response if the connection succeeds",
    "_postman_id": "5dade841-dbb3-4d14-afae-8e0e92ea8dc0",
    "description": "A simple method that returns a 200 response if the connection succeeds.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Oauth",
      "item": [
        {
          "id": "0c2cdc75-8a06-43bf-977c-a62449c51421",
          "name": "postOauthToken",
          "request": {
            "url": "http://api.backupify.com/oauth/token",
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "client_id",
                  "value": "{}",
                  "disabled": false,
                  "description": "API Client ID"
                },
                {
                  "key": "client_secret",
                  "value": "{}",
                  "disabled": false,
                  "description": "API Client secret"
                },
                {
                  "key": "grant_type",
                  "value": "{}",
                  "disabled": false,
                  "description": "String identifying the grant type to be used for token retrieval"
                },
                {
                  "key": "scope",
                  "value": "{}",
                  "disabled": false,
                  "description": "A space separated list of operational scopes available to the returned token"
                }
              ]
            },
            "description": "All actions and visibility is limited in scope to items that are descendents of the authenticated vendor and the backup_definitions owned thereby. At this time, all Access Tokens are scoped with full write capabilities."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "79e43ee7-955f-4d7a-820e-2eb6e2dccdec"
            }
          ]
        }
      ]
    },
    {
      "name": "V1",
      "item": [
        {
          "id": "57f805ae-fbe8-404b-a79f-b44a5cb7524f",
          "name": "getV1AuthenticateCustomer",
          "request": {
            "url": "http://api.backupify.com/v1/authenticate_customer",
            "method": "GET",
            "header": [
              {
                "key": "Authorization",
                "value": "{}",
                "description": "Bearer Access Token granted for customer",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "A simple method to test authentication of a customer access token.."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2e0734f0-bf34-4bb1-85b5-721040333a50"
            }
          ]
        },
        {
          "id": "ce1999a8-2aef-4dae-a20c-757fe361eaba",
          "name": "getV1AuthenticateVendor",
          "request": {
            "url": "http://api.backupify.com/v1/authenticate_vendor",
            "method": "GET",
            "header": [
              {
                "key": "Authorization",
                "value": "{}",
                "description": "Bearer Access Token granted from client_credentials for vendor",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "A simple method to test authentication of a vendor access token. the response body is empty json object.."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "08dfd8ab-e0c2-4fc4-9393-d7c79563780f"
            }
          ]
        },
        {
          "id": "42bf58a9-bf78-459c-99be-80ea051bff0f",
          "name": "getV1BackupDefinitions",
          "request": {
            "url": "http://api.backupify.com/v1/backup_definitions?vendor_id=%7B%7D",
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
            "description": "This will retrieve a list of backup_defintions from all vendors. To view backup_defintions for a particular vendor, see the vendors API. Records are returned in ascending order (by id), with a default of 20 per page. Links to the next, previous, first, and last pages can be found in the response headers."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f539bf62-b2be-4505-b551-0c0ea7ac70ca"
            }
          ]
        },
        {
          "id": "084d323a-ca15-4480-82bf-ae0814ee1c14",
          "name": "postV1BackupDefinitions",
          "request": {
            "url": "http://api.backupify.com/v1/backup_definitions",
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
                  "key": "backup_definition[description]",
                  "value": "{}",
                  "disabled": false,
                  "description": "Description of the backup_definition"
                },
                {
                  "key": "backup_definition[name]",
                  "value": "{}",
                  "disabled": false,
                  "description": "Name for the backup_definition"
                },
                {
                  "key": "backup_definition[published]",
                  "value": "{}",
                  "disabled": false,
                  "description": "Boolean flag indicating whether the backup definition is published and available for use"
                }
              ]
            },
            "description": "Create a new backup_definition."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "063d7a03-3abd-44e1-a027-c4f961e4ba39"
            }
          ]
        },
        {
          "id": "85b43bdc-d94d-48ac-b622-a477b366474b",
          "name": "getV1BackupDefinitionsBackupDefinition",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.backupify.com",
              "path": [
                "v1/backup_definitions/:backup_definition_id"
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
            "description": "Only backup_definitions you have permission to view will be returned"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "173baa96-356d-4117-8594-566e98686893"
            }
          ]
        },
        {
          "id": "116d00c3-126f-4277-8645-90f3bca0d714",
          "name": "putV1BackupDefinitionsBackupDefinition",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.backupify.com",
              "path": [
                "v1/backup_definitions/:backup_definition_id"
              ],
              "variable": [
                {
                  "id": "backup_definition_id",
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
                  "key": "backup_definition[description]",
                  "value": "{}",
                  "disabled": false,
                  "description": "Description of the backup_definition"
                },
                {
                  "key": "backup_definition[name]",
                  "value": "{}",
                  "disabled": false,
                  "description": "Name for the backup_definition"
                },
                {
                  "key": "backup_definition[published]",
                  "value": "{}",
                  "disabled": false,
                  "description": "Boolean flag indicating whether the backup definition is published and available for use"
                }
              ]
            },
            "description": "Only backup_definitions you have permission to change can be modified"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "dd2649a6-810e-4776-a24e-7deb68d75fe5"
            }
          ]
        },
        {
          "id": "a1b86c95-34d4-47fb-b429-6ae9aedac0db",
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
              "id": "299ddb98-4d6b-4fbb-95ca-338d110d75b7"
            }
          ]
        },
        {
          "id": "1c8e3063-6420-4c0c-932d-c7bcb7979197",
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
              "id": "d2c7456d-1ceb-40c6-ac9b-85694613169a"
            }
          ]
        },
        {
          "id": "4e04e5b4-c8bb-4c07-99d6-b2b02df94592",
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
              "id": "bfe93568-fb6c-4116-8413-eda8f16454a2"
            }
          ]
        },
        {
          "id": "66ccba4e-6f2c-4705-8250-dbc728020a8c",
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
              "id": "80a09656-90e5-4fd5-911f-f94c9f5b28df"
            }
          ]
        },
        {
          "id": "0e206a99-cd2c-4a49-9fc6-c0d2dc4d259e",
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
              "id": "bc9f42c3-e8f1-4557-875a-30da459e1e68"
            }
          ]
        },
        {
          "id": "d7045ec7-80ad-4b10-baed-d081686c46ac",
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
              "id": "e6566458-58fa-42c2-abf1-b386f52b0854"
            }
          ]
        },
        {
          "id": "1ce273f9-a970-4a8e-9fdb-abcaf241842d",
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
              "id": "e7a406cb-1f1f-4b1f-9007-9292209b0936"
            }
          ]
        },
        {
          "id": "bb0290ac-f17d-4f85-8f63-c2ce21ee2a3a",
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
              "id": "2e80ee7d-496a-4407-926f-3e85ca597e68"
            }
          ]
        },
        {
          "id": "81e802b3-21e4-4551-a518-2ed03946faf7",
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
              "id": "6e75285c-bd04-4f9c-88bd-15badaaf710a"
            }
          ]
        },
        {
          "id": "595eb3ab-051e-45eb-858c-5a4c616f158a",
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
              "id": "b860b6b2-08a1-4366-8dd5-22750691386e"
            }
          ]
        },
        {
          "id": "2f9f030c-e7fa-402b-b621-cab4293d636d",
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
              "id": "07d422c0-6390-40d4-9226-c817aa16d06f"
            }
          ]
        },
        {
          "id": "c8d36ba3-8a53-4316-9d17-941812db825f",
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
              "id": "446f82c7-f0c8-4091-bd00-d5390a4f404c"
            }
          ]
        },
        {
          "id": "eba56551-ebe0-450c-bca8-225bdb8f2e46",
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
              "id": "112b0738-76f6-48fd-8fa2-0d6867872b8a"
            }
          ]
        },
        {
          "id": "768e5a49-8376-481c-90e9-eb6cc3ce215f",
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
              "id": "e888522c-bede-47b4-bd18-b514e7134bc8"
            }
          ]
        },
        {
          "id": "1e6bfd9d-72fd-4e06-9555-16850059db67",
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
              "id": "55c6f675-5832-4eff-b1e2-2a2d45cf77bf"
            }
          ]
        },
        {
          "id": "04d9ab06-42fe-48ef-8433-638a92515ff7",
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
              "id": "13f9b02d-b268-424b-badd-d6a0e6a665e5"
            }
          ]
        },
        {
          "id": "1b59ac1b-242a-4316-b4e5-6b526db1332f",
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
              "id": "89b00fcc-50d8-4492-80df-263cc0369198"
            }
          ]
        },
        {
          "id": "5d932d08-28a6-4fc1-8361-f5b52040e073",
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
              "id": "f4a8962a-1645-4063-8b63-f43ee387058b"
            }
          ]
        },
        {
          "id": "e8374312-552b-4847-ab08-963eb8d1d854",
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
              "id": "ad5689ee-76b3-45c6-b041-3ad65a865cd4"
            }
          ]
        },
        {
          "id": "5ec803dc-818a-4bd2-a035-61b5890f8963",
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
              "id": "53880ffc-7bbf-431b-a70c-de3837f363e8"
            }
          ]
        },
        {
          "id": "8c99c0f9-edda-43e0-9620-3e10061fb075",
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
              "id": "f2c6b55a-f2cb-4435-a69c-5ad442dc647c"
            }
          ]
        },
        {
          "id": "ba1c0e6d-a9e4-468d-95ac-ff91e0f70f53",
          "name": "getV1BackupInstancesBackupInstanceLogs",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.backupify.com",
              "path": [
                "v1/backup_instances/:backup_instance_id/logs"
              ],
              "query": [
                {
                  "key": "date",
                  "value": "%7B%7D",
                  "disabled": false
                }
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
            "description": "Returns the logs for a given backup instance."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3ac1b649-1c8e-4b39-b36d-7bcb4dd40ddd"
            }
          ]
        },
        {
          "id": "2d44328a-62e7-4120-8ec0-f6f283b32cc8",
          "name": "getV1BackupInstancesBackupInstanceLogsScroll",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.backupify.com",
              "path": [
                "v1/backup_instances/:backup_instance_id/logs/:scroll_id"
              ],
              "variable": [
                {
                  "id": "backup_instance_id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "scroll_id",
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
            "description": "Returns the logs for a given backup instance."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6ce9efd7-9ef8-4ac7-bb87-8c60dbd2c1d3"
            }
          ]
        },
        {
          "id": "bb57137a-919d-4b70-9815-2367e860466a",
          "name": "getV1BackupInstancesBackupInstanceVariables",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.backupify.com",
              "path": [
                "v1/backup_instances/:backup_instance_id/variables"
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
            "description": "You can only retrieve variables for backup_instances you have access to. Records are returned in ascending order (by id), with a default of 20 per page. Links to the next, previous, first, and last pages can be found in the response headers."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "08c750a2-aad6-4ccb-acd4-834cbd66f1bd"
            }
          ]
        },
        {
          "id": "cb4f65e8-525f-45d3-9833-eed5b84976c6",
          "name": "postV1BackupInstancesBackupInstanceVariables",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.backupify.com",
              "path": [
                "v1/backup_instances/:backup_instance_id/variables"
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
                  "key": "variable[key]",
                  "value": "{}",
                  "disabled": false,
                  "description": "The key, as defined by the backup_definition, to set a value for"
                },
                {
                  "key": "variable[value]",
                  "value": "{}",
                  "disabled": false,
                  "description": "The value or information to store for the specified key"
                }
              ]
            },
            "description": "The key specified must refer to the key of a previously defined backup_definition variable. It is only possible to create variables for backup_instances you have permission to manage."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "477e4e7f-c42a-41e6-8bf2-2dd1fb531abe"
            }
          ]
        },
        {
          "id": "79d6b1da-6467-4f84-96c8-6306489138cb",
          "name": "getV1BackupInstancesBackupInstanceVariablesKey",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.backupify.com",
              "path": [
                "v1/backup_instances/:backup_instance_id/variables/:key"
              ],
              "variable": [
                {
                  "id": "backup_instance_id",
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
            "description": "You can only retrieve variables for backup_instances you have access to"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3059c0d6-5345-4cff-81d0-c66e88570fcd"
            }
          ]
        },
        {
          "id": "f1b08ff6-76ff-4f45-9797-2611b81e95b8",
          "name": "putV1BackupInstancesBackupInstanceVariablesKey",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.backupify.com",
              "path": [
                "v1/backup_instances/:backup_instance_id/variables/:key"
              ],
              "variable": [
                {
                  "id": "backup_instance_id",
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
                  "key": "variable[value]",
                  "value": "{}",
                  "disabled": false,
                  "description": "The updated data to store at the specified key"
                }
              ]
            },
            "description": "You can only alter variables for backup_instances you have access to manage"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "20a2bb2b-c859-406b-a959-500a3b33cd37"
            }
          ]
        },
        {
          "id": "81e40524-1fda-42c5-85ef-a0615c6e14e1",
          "name": "getV1Customers",
          "request": {
            "url": "http://api.backupify.com/v1/customers",
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
            "description": "Requires Access Token granted from client credentials. Records are returned in ascending order (by id), with a default of 20 per page. Links to the next, previous, first, and last pages can be found in the response headers."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7f0aedee-cff0-4f38-a064-39ab7a49ffc4"
            }
          ]
        },
        {
          "id": "01e8b899-7a6e-4865-9d0c-4beb96d854d8",
          "name": "postV1Customers",
          "request": {
            "url": "http://api.backupify.com/v1/customers",
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
                  "key": "customer[email]",
                  "value": "{}",
                  "disabled": false,
                  "description": "Email address associated with the customer"
                },
                {
                  "key": "customer[name]",
                  "value": "{}",
                  "disabled": false,
                  "description": "Vendor provided ID uniquely identifying customer"
                }
              ]
            },
            "description": "Create a new customer instance identified by the given {name} identifier."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "34cedb39-30fc-47eb-a44a-eb05b3d65c36"
            }
          ]
        },
        {
          "id": "f00f7df4-e94a-4757-a0c4-81834c20cc3f",
          "name": "getV1CustomersCustomer",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.backupify.com",
              "path": [
                "v1/customers/:customer_id"
              ],
              "variable": [
                {
                  "id": "customer_id",
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
            "description": "Requires Access Token granted from client credentials."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "032aaf40-ddb0-48d4-a0ba-ff110e9bf694"
            }
          ]
        },
        {
          "id": "12cd4d91-d4a8-452c-a3ae-5a761f107846",
          "name": "putV1CustomersCustomer",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.backupify.com",
              "path": [
                "v1/customers/:customer_id"
              ],
              "variable": [
                {
                  "id": "customer_id",
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
                  "key": "customer[name]",
                  "value": "{}",
                  "disabled": false,
                  "description": "Vendor provided ID uniquely identifying customer"
                }
              ]
            },
            "description": "Update a customer instance identified by the given customer_id."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "290ae065-6b17-4277-b426-6095c1b7cde3"
            }
          ]
        },
        {
          "id": "cb4156a9-ac98-45b9-b1d6-e0727fb04b50",
          "name": "getV1CustomersCustomerBackupInstances",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.backupify.com",
              "path": [
                "v1/customers/:customer_id/backup_instances"
              ],
              "variable": [
                {
                  "id": "customer_id",
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
            "description": "It is only possible to retrieve backup_instances for customers you are authorized to access. Records are returned in ascending order (by id), with a default of 20 per page. Links to the next, previous, first, and last pages can be found in the response headers."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "28e8e6f9-86f1-47d3-98d5-36365b6fc8f2"
            }
          ]
        },
        {
          "id": "c8087cc2-724e-47f8-8acb-8a370450aa9c",
          "name": "getV1Ping",
          "request": {
            "url": "http://api.backupify.com/v1/ping",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "A simple method that returns a 200 response if the connection succeeds."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "008ce8aa-8547-4ed0-bcc5-22220b2ea3c1"
            }
          ]
        }
      ]
    }
  ]
}