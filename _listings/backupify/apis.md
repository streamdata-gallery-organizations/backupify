---
name: Backupify
x-slug: backupify
description: ""
image: ""
x-kinRank: "7"
x-alexaRank: "0"
tags: Backupify
created: "2018-06-26"
modified: "2018-06-26"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/apis.md
specificationVersion: "0.14"
apis:
- name: Backupify Retrieve an Access Token authenticated using the provided client_id
    and client_secret.
  x-api-slug: backupify
  description: All actions and visibility is limited in scope to items that are descendents
    of the authenticated vendor and the backup_definitions owned thereby. At this
    time, all Access Tokens are scoped with full write capabilities.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////oauth/token
  tags: Oauth,Token
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/oauthtoken-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/oauthtoken-post-openapi.md
- name: Backupify A simple method to test authentication of a customer access token.
  x-api-slug: backupify
  description: A simple method to test authentication of a customer access token..
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/authenticate_customer
  tags: V1,Authenticate,Customer
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1authenticate-customer-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1authenticate-customer-get-openapi.md
- name: Backupify A simple method to test authentication of a vendor access token.
    The response body is empty JSON object.
  x-api-slug: backupify
  description: A simple method to test authentication of a vendor access token. the
    response body is empty json object..
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/authenticate_vendor
  tags: V1,Authenticate,Vendor
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1authenticate-vendor-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1authenticate-vendor-get-openapi.md
- name: Backupify Retrieve an index of all backup_definitions
  x-api-slug: backupify
  description: This will retrieve a list of backup_defintions from all vendors. To
    view backup_defintions for a particular vendor, see the vendors API. Records are
    returned in ascending order (by id), with a default of 20 per page. Links to the
    next, previous, first, and last pages can be found in the response headers.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/backup_definitions
  tags: V1,Backup,Definitions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-definitions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-definitions-get-openapi.md
- name: Backupify Create a new backup_definition
  x-api-slug: backupify
  description: Create a new backup_definition.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/backup_definitions
  tags: V1,Backup,Definitions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-definitions-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-definitions-post-openapi.md
- name: Backupify Retrieve a backup_definition by backup_definition_id
  x-api-slug: backupify
  description: Only backup_definitions you have permission to view will be returned
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/backup_definitions/{backup_definition_id}
  tags: V1,Backup,Definitions,Backup,Definition,Id
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-definitionsbackup-definition-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-definitionsbackup-definition-id-get-openapi.md
- name: Backupify Update the specified backup_definition
  x-api-slug: backupify
  description: Only backup_definitions you have permission to change can be modified
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/backup_definitions/{backup_definition_id}
  tags: V1,Backup,Definitions,Backup,Definition,Id
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-definitionsbackup-definition-id-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-definitionsbackup-definition-id-put-openapi.md
- name: Backupify Retrieve a list of variables for the specified backup_definition
  x-api-slug: backupify
  description: You can only retrieve variables for backup_definitions you have access
    to. Records are returned in ascending order (by id), with a default of 20 per
    page. Links to the next, previous, first, and last pages can be found in the response
    headers.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/backup_definitions/{backup_definition_id}/variables
  tags: V1,Backup,Definitions,Backup,Definition,Id,Variables
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-definitionsbackup-definition-idvariables-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-definitionsbackup-definition-idvariables-get-openapi.md
- name: Backupify Create a new variable for the specified key for the specified backup_definition
  x-api-slug: backupify
  description: It is only possible to create variables for backup_definitions you
    have permission to manage.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/backup_definitions/{backup_definition_id}/variables
  tags: V1,Backup,Definitions,Backup,Definition,Id,Variables
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-definitionsbackup-definition-idvariables-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-definitionsbackup-definition-idvariables-post-openapi.md
- name: Backupify Retrieve a specific variable by key for the specified backup_definition
  x-api-slug: backupify
  description: You can only retrieve variables for backup_definitions you have access
    to
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/backup_definitions/{backup_definition_id}/variables/{key}
  tags: V1,Backup,Definitions,Backup,Definition,Id,Variables,Key
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-definitionsbackup-definition-idvariableskey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-definitionsbackup-definition-idvariableskey-get-openapi.md
- name: Backupify Update a specific variable by key for the specified backup_definition
  x-api-slug: backupify
  description: You can only update variables for backup_definitions you have access
    to. Additionally, it is not possible to update a variable's key. Requests including
    a modified key name will result in an error.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/backup_definitions/{backup_definition_id}/variables/{key}
  tags: V1,Backup,Definitions,Backup,Definition,Id,Variables,Key
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-definitionsbackup-definition-idvariableskey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-definitionsbackup-definition-idvariableskey-put-openapi.md
- name: Backupify Retrieves a list of backup_instances associated with the specified
    backup_definition
  x-api-slug: backupify
  description: It is only possible to retrieve backup_instances for customers you
    are authorized to access. Records are returned in ascending order (by id), with
    a default of 20 per page. Links to the next, previous, first, and last pages can
    be found in the response headers.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/backup_instances
  tags: V1,Backup,Instances
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instances-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instances-get-openapi.md
- name: Backupify Create a new backup_instance from the specified backup_definition
    for the specified customer
  x-api-slug: backupify
  description: Create a new backup_instance from the specified backup_definition for
    the specified customer.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/backup_instances
  tags: V1,Backup,Instances
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instances-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instances-post-openapi.md
- name: Backupify Retrieve a backup_instance by backup_instance_id
  x-api-slug: backupify
  description: Only backup_instances you have permission to view will be returned
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/backup_instances/{backup_instance_id}
  tags: V1,Backup,Instances,Backup,Instance,Id
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-id-get-openapi.md
- name: Backupify Modify the specified backup_instance
  x-api-slug: backupify
  description: Only backup_instances you have permission to change can be modified
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/backup_instances/{backup_instance_id}
  tags: V1,Backup,Instances,Backup,Instance,Id
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-id-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-id-put-openapi.md
- name: Backupify Retrieve a list of all backups for the specified backup_instance.
  x-api-slug: backupify
  description: Only backups belonging to backup_instances you have permission to manage
    can be retrieved. Records are returned in ascending order (by id), with a default
    of 20 per page. Links to the next, previous, first, and last pages can be found
    in the response headers.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/backup_instances/{backup_instance_id}/backups
  tags: V1,Backup,Instances,Backup,Instance,Id,Backups
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idbackups-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idbackups-get-openapi.md
- name: Backupify Perform an immediate backup of the specified backup_instance
  x-api-slug: backupify
  description: Only backup_instances you have permission to manage can be backed up
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/backup_instances/{backup_instance_id}/backups
  tags: V1,Backup,Instances,Backup,Instance,Id,Backups
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idbackups-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idbackups-post-openapi.md
- name: Backupify Retrieve the active backup for the specified backup_instance if
    one exists
  x-api-slug: backupify
  description: Only backups belonging to backup_instances you have permission to access
    can be retrieved
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/backup_instances/{backup_instance_id}/backups/active
  tags: V1,Backup,Instances,Backup,Instance,Id,Backups,Active
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idbackupsactive-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idbackupsactive-get-openapi.md
- name: Backupify Retrieve the specified backup for the specified backup_instance
  x-api-slug: backupify
  description: Only backups belonging to backup_instances you have permission to access
    can be retrieved
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/backup_instances/{backup_instance_id}/backups/{backup_id}
  tags: V1,Backup,Instances,Backup,Instance,Id,Backups,Backup,Id
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idbackupsbackup-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idbackupsbackup-id-get-openapi.md
- name: Backupify Retrieve a list of endpoints for the specified backup_instance
  x-api-slug: backupify
  description: You can only retrieve endpoints for backup_instances you have access
    to. Records are returned in ascending order (by id), with a default of 20 per
    page. Links to the next, previous, first, and last pages can be found in the response
    headers.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/backup_instances/{backup_instance_id}/endpoints
  tags: V1,Backup,Instances,Backup,Instance,Id,Endpoints
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idendpoints-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idendpoints-get-openapi.md
- name: Backupify Retrieve a specific endpoint by name for the specified backup_instance
  x-api-slug: backupify
  description: You can only retrieve endpoints for backup_instances you have access
    to
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/backup_instances/{backup_instance_id}/endpoints/{endpoint_name}
  tags: V1,Backup,Instances,Backup,Instance,Id,Endpoints,Endpoint,Name
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idendpointsendpoint-name-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idendpointsendpoint-name-get-openapi.md
- name: Backupify Retrieve a list of records stored for the specified endpoint and
    backup_instance
  x-api-slug: backupify
  description: You can only retrieve records for endpoints that belong to backup_instances
    you have access to. Records are returned in ascending order (by id), with a default
    of 20 per page. Links to the next, previous, first, and last pages can be found
    in the response headers.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/backup_instances/{backup_instance_id}/endpoints/{endpoint_name}/records
  tags: V1,Backup,Instances,Backup,Instance,Id,Endpoints,Endpoint,Name,Records
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idendpointsendpoint-namerecords-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idendpointsendpoint-namerecords-get-openapi.md
- name: Backupify Retrieve a specific record by id for the specified endpoint and
    backup_instance
  x-api-slug: backupify
  description: You can only retrieve records for endpoints of backup_instances you
    have access to
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/backup_instances/{backup_instance_id}/endpoints/{endpoint_name}/records/{record_id}
  tags: V1,Backup,Instances,Backup,Instance,Id,Endpoints,Endpoint,Name,Records,Record,Id
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idendpointsendpoint-namerecordsrecord-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idendpointsendpoint-namerecordsrecord-id-get-openapi.md
- name: Backupify Retrieve the blob associated with the specified record for the specified
    endpoint and backup_instance
  x-api-slug: backupify
  description: Retrieve the blob associated with the specified record for the specified
    endpoint and backup_instance.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/backup_instances/{backup_instance_id}/endpoints/{endpoint_name}/records/{record_id}/blob
  tags: V1,Backup,Instances,Backup,Instance,Id,Endpoints,Endpoint,Name,Records,Record,Id,Blob
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idendpointsendpoint-namerecordsrecord-idblob-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idendpointsendpoint-namerecordsrecord-idblob-get-openapi.md
- name: Backupify Retrieve a list of exports for the specified backup_instance
  x-api-slug: backupify
  description: You can only retrieve exports for backup_instances you have access
    to. Records are returned in ascending order (by id), with a default of 20 per
    page. Links to the next, previous, first, and last pages can be found in the response
    headers.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/backup_instances/{backup_instance_id}/exports
  tags: V1,Backup,Instances,Backup,Instance,Id,Exports
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idexports-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idexports-get-openapi.md
- name: Backupify Perform an export of the most recent backup of the specified backup_instance
  x-api-slug: backupify
  description: Perform an export of the most recent backup of the specified backup_instance.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/backup_instances/{backup_instance_id}/exports
  tags: V1,Backup,Instances,Backup,Instance,Id,Exports
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idexports-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idexports-post-openapi.md
- name: Backupify Retrieve a specific export for the specified backup_instance
  x-api-slug: backupify
  description: You can only retrieve exports for backup_instances you have access
    to
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/backup_instances/{backup_instance_id}/exports/{export_id}
  tags: V1,Backup,Instances,Backup,Instance,Id,Exports,Export,Id
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idexportsexport-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idexportsexport-id-get-openapi.md
- name: Backupify Retrieve an updated exported_data_url for a specific export for
    the specified backup_instance
  x-api-slug: backupify
  description: Retrieve an updated exported_data_url for a specific export for the
    specified backup_instance.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/backup_instances/{backup_instance_id}/exports/{export_id}/reauth
  tags: V1,Backup,Instances,Backup,Instance,Id,Exports,Export,Id,Reauth
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idexportsexport-idreauth-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idexportsexport-idreauth-post-openapi.md
- name: Backupify Returns the logs for a given backup instance
  x-api-slug: backupify
  description: Returns the logs for a given backup instance.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/backup_instances/{backup_instance_id}/logs
  tags: V1,Backup,Instances,Backup,Instance,Id,Logs
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idlogs-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idlogs-get-openapi.md
- name: Backupify Returns the logs for a given backup instance
  x-api-slug: backupify
  description: Returns the logs for a given backup instance.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/backup_instances/{backup_instance_id}/logs/{scroll_id}
  tags: V1,Backup,Instances,Backup,Instance,Id,Logs,Scroll,Id
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idlogsscroll-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idlogsscroll-id-get-openapi.md
- name: Backupify Retrieve a list of variables for the specified backup_instance
  x-api-slug: backupify
  description: You can only retrieve variables for backup_instances you have access
    to. Records are returned in ascending order (by id), with a default of 20 per
    page. Links to the next, previous, first, and last pages can be found in the response
    headers.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/backup_instances/{backup_instance_id}/variables
  tags: V1,Backup,Instances,Backup,Instance,Id,Variables
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idvariables-get-openapi.md
- name: Backupify Create a custom variable value for the specified key for the specified
    backup_instance
  x-api-slug: backupify
  description: The key specified must refer to the key of a previously defined backup_definition
    variable. It is only possible to create variables for backup_instances you have
    permission to manage.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/backup_instances/{backup_instance_id}/variables
  tags: V1,Backup,Instances,Backup,Instance,Id,Variables
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idvariables-post-openapi.md
- name: Backupify Retrieve a specific variable by key for the specified backup_instance
  x-api-slug: backupify
  description: You can only retrieve variables for backup_instances you have access
    to
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/backup_instances/{backup_instance_id}/variables/{key}
  tags: V1,Backup,Instances,Backup,Instance,Id,Variables,Key
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idvariableskey-get-openapi.md
- name: Backupify Update the value of a variable by key for the specified backup_instance
  x-api-slug: backupify
  description: You can only alter variables for backup_instances you have access to
    manage
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/backup_instances/{backup_instance_id}/variables/{key}
  tags: V1,Backup,Instances,Backup,Instance,Id,Variables,Key
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idvariableskey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idvariableskey-put-openapi.md
- name: Backupify Retrieve a list of customers associated with the authenticated vendor
  x-api-slug: backupify
  description: Requires Access Token granted from client credentials. Records are
    returned in ascending order (by id), with a default of 20 per page. Links to the
    next, previous, first, and last pages can be found in the response headers.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/customers
  tags: V1,Customers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1customers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1customers-get-openapi.md
- name: Backupify Create a new customer instance identified by the given {name} identifier
  x-api-slug: backupify
  description: Create a new customer instance identified by the given {name} identifier.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/customers
  tags: V1,Customers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1customers-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1customers-post-openapi.md
- name: Backupify Retrieves the customer identified by customer_id
  x-api-slug: backupify
  description: Requires Access Token granted from client credentials.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/customers/{customer_id}
  tags: V1,Customers,Customer,Id
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1customerscustomer-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1customerscustomer-id-get-openapi.md
- name: Backupify Update a customer instance identified by the given customer_id
  x-api-slug: backupify
  description: Update a customer instance identified by the given customer_id.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/customers/{customer_id}
  tags: V1,Customers,Customer,Id
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1customerscustomer-id-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1customerscustomer-id-put-openapi.md
- name: Backupify Retrieves a list of backup_instances associated with the specified
    customer
  x-api-slug: backupify
  description: It is only possible to retrieve backup_instances for customers you
    are authorized to access. Records are returned in ascending order (by id), with
    a default of 20 per page. Links to the next, previous, first, and last pages can
    be found in the response headers.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/customers/{customer_id}/backup_instances
  tags: V1,Customers,Customer,Id,Backup,Instances
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1customerscustomer-idbackup-instances-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1customerscustomer-idbackup-instances-get-openapi.md
- name: Backupify A simple method that returns a 200 response if the connection succeeds
  x-api-slug: backupify
  description: A simple method that returns a 200 response if the connection succeeds.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/ping
  tags: V1,Ping
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1ping-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1ping-get-openapi.md
- name: Backupify Provides information about the currently authenticated vendor user
  x-api-slug: backupify
  description: Provides information about the currently authenticated vendor user.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com////v1/vendors/me
  tags: V1,Vendors,Me
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1vendorsme-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1vendorsme-get-openapi.md
- name: Backupify
  x-api-slug: backupify
  description: 'Backupify is a backup service for SaaS accounts. Backupify can help
    users backup their SaaS accounts and restore if and when needed. Backupify offers
    a developers program for developers to access and integrate the functionality
    of Backupify with other applications. Public documentation is not available; interested
    developers should sign up here for more information on the developers program:
    https://www.backupify.com/solutions/developers or email developerprogram@backupify.com.'
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: Backupify
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/openapi.md
x-common:
- type: x-blog
  url: https://www.backupify.com/blog
- type: x-website
  url: http://backupify.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---