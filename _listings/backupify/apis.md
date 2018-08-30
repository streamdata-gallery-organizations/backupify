---
name: Backupify
x-slug: backupify
description: ""
image: ""
x-kinRank: "7"
x-alexaRank: "0"
tags: Backupify
created: "2018-08-29"
modified: "2018-08-29"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/apis.md
specificationVersion: "0.14"
apis:
- name: Backupify - Retrieve an Access Token authenticated using the provided client_id
    and client_secret.
  x-api-slug: oauthtoken-post
  description: All actions and visibility is limited in scope to items that are descendents
    of the authenticated vendor and the backup_definitions owned thereby. At this
    time, all Access Tokens are scoped with full write capabilities.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/oauthtoken-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/oauthtoken-post-openapi.md
- name: Backupify - A simple method to test authentication of a customer access token.
  x-api-slug: v1authenticate-customer-get
  description: A simple method to test authentication of a customer access token..
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1authenticate-customer-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1authenticate-customer-get-openapi.md
- name: Backupify - A simple method to test authentication of a vendor access token.
    The response body is empty JSON object.
  x-api-slug: v1authenticate-vendor-get
  description: A simple method to test authentication of a vendor access token. the
    response body is empty json object..
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1authenticate-vendor-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1authenticate-vendor-get-openapi.md
- name: Backupify - Retrieve an index of all backup_definitions
  x-api-slug: v1backup-definitions-get
  description: This will retrieve a list of backup_defintions from all vendors. To
    view backup_defintions for a particular vendor, see the vendors API. Records are
    returned in ascending order (by id), with a default of 20 per page. Links to the
    next, previous, first, and last pages can be found in the response headers.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-definitions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-definitions-get-openapi.md
- name: Backupify - Create a new backup_definition
  x-api-slug: v1backup-definitions-post
  description: Create a new backup_definition.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-definitions-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-definitions-post-openapi.md
- name: Backupify - Retrieve a backup_definition by backup_definition_id
  x-api-slug: v1backup-definitionsbackup-definition-id-get
  description: Only backup_definitions you have permission to view will be returned
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-definitionsbackup-definition-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-definitionsbackup-definition-id-get-openapi.md
- name: Backupify - Update the specified backup_definition
  x-api-slug: v1backup-definitionsbackup-definition-id-put
  description: Only backup_definitions you have permission to change can be modified
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-definitionsbackup-definition-id-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-definitionsbackup-definition-id-put-openapi.md
- name: Backupify - Retrieve a list of variables for the specified backup_definition
  x-api-slug: v1backup-definitionsbackup-definition-idvariables-get
  description: You can only retrieve variables for backup_definitions you have access
    to. Records are returned in ascending order (by id), with a default of 20 per
    page. Links to the next, previous, first, and last pages can be found in the response
    headers.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-definitionsbackup-definition-idvariables-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-definitionsbackup-definition-idvariables-get-openapi.md
- name: Backupify - Create a new variable for the specified key for the specified
    backup_definition
  x-api-slug: v1backup-definitionsbackup-definition-idvariables-post
  description: It is only possible to create variables for backup_definitions you
    have permission to manage.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-definitionsbackup-definition-idvariables-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-definitionsbackup-definition-idvariables-post-openapi.md
- name: Backupify - Retrieve a specific variable by key for the specified backup_definition
  x-api-slug: v1backup-definitionsbackup-definition-idvariableskey-get
  description: You can only retrieve variables for backup_definitions you have access
    to
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-definitionsbackup-definition-idvariableskey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-definitionsbackup-definition-idvariableskey-get-openapi.md
- name: Backupify - Update a specific variable by key for the specified backup_definition
  x-api-slug: v1backup-definitionsbackup-definition-idvariableskey-put
  description: You can only update variables for backup_definitions you have access
    to. Additionally, it is not possible to update a variable's key. Requests including
    a modified key name will result in an error.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-definitionsbackup-definition-idvariableskey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-definitionsbackup-definition-idvariableskey-put-openapi.md
- name: Backupify - Retrieves a list of backup_instances associated with the specified
    backup_definition
  x-api-slug: v1backup-instances-get
  description: It is only possible to retrieve backup_instances for customers you
    are authorized to access. Records are returned in ascending order (by id), with
    a default of 20 per page. Links to the next, previous, first, and last pages can
    be found in the response headers.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instances-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instances-get-openapi.md
- name: Backupify - Create a new backup_instance from the specified backup_definition
    for the specified customer
  x-api-slug: v1backup-instances-post
  description: Create a new backup_instance from the specified backup_definition for
    the specified customer.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instances-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instances-post-openapi.md
- name: Backupify - Retrieve a backup_instance by backup_instance_id
  x-api-slug: v1backup-instancesbackup-instance-id-get
  description: Only backup_instances you have permission to view will be returned
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-id-get-openapi.md
- name: Backupify - Modify the specified backup_instance
  x-api-slug: v1backup-instancesbackup-instance-id-put
  description: Only backup_instances you have permission to change can be modified
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-id-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-id-put-openapi.md
- name: Backupify - Retrieve a list of all backups for the specified backup_instance.
  x-api-slug: v1backup-instancesbackup-instance-idbackups-get
  description: Only backups belonging to backup_instances you have permission to manage
    can be retrieved. Records are returned in ascending order (by id), with a default
    of 20 per page. Links to the next, previous, first, and last pages can be found
    in the response headers.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idbackups-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idbackups-get-openapi.md
- name: Backupify - Perform an immediate backup of the specified backup_instance
  x-api-slug: v1backup-instancesbackup-instance-idbackups-post
  description: Only backup_instances you have permission to manage can be backed up
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idbackups-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idbackups-post-openapi.md
- name: Backupify - Retrieve the active backup for the specified backup_instance if
    one exists
  x-api-slug: v1backup-instancesbackup-instance-idbackupsactive-get
  description: Only backups belonging to backup_instances you have permission to access
    can be retrieved
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idbackupsactive-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idbackupsactive-get-openapi.md
- name: Backupify - Retrieve the specified backup for the specified backup_instance
  x-api-slug: v1backup-instancesbackup-instance-idbackupsbackup-id-get
  description: Only backups belonging to backup_instances you have permission to access
    can be retrieved
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idbackupsbackup-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idbackupsbackup-id-get-openapi.md
- name: Backupify - Retrieve a list of endpoints for the specified backup_instance
  x-api-slug: v1backup-instancesbackup-instance-idendpoints-get
  description: You can only retrieve endpoints for backup_instances you have access
    to. Records are returned in ascending order (by id), with a default of 20 per
    page. Links to the next, previous, first, and last pages can be found in the response
    headers.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idendpoints-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idendpoints-get-openapi.md
- name: Backupify - Retrieve a specific endpoint by name for the specified backup_instance
  x-api-slug: v1backup-instancesbackup-instance-idendpointsendpoint-name-get
  description: You can only retrieve endpoints for backup_instances you have access
    to
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idendpointsendpoint-name-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idendpointsendpoint-name-get-openapi.md
- name: Backupify - Retrieve a list of records stored for the specified endpoint and
    backup_instance
  x-api-slug: v1backup-instancesbackup-instance-idendpointsendpoint-namerecords-get
  description: You can only retrieve records for endpoints that belong to backup_instances
    you have access to. Records are returned in ascending order (by id), with a default
    of 20 per page. Links to the next, previous, first, and last pages can be found
    in the response headers.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idendpointsendpoint-namerecords-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idendpointsendpoint-namerecords-get-openapi.md
- name: Backupify - Retrieve a specific record by id for the specified endpoint and
    backup_instance
  x-api-slug: v1backup-instancesbackup-instance-idendpointsendpoint-namerecordsrecord-id-get
  description: You can only retrieve records for endpoints of backup_instances you
    have access to
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idendpointsendpoint-namerecordsrecord-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idendpointsendpoint-namerecordsrecord-id-get-openapi.md
- name: Backupify - Retrieve the blob associated with the specified record for the
    specified endpoint and backup_instance
  x-api-slug: v1backup-instancesbackup-instance-idendpointsendpoint-namerecordsrecord-idblob-get
  description: Retrieve the blob associated with the specified record for the specified
    endpoint and backup_instance.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idendpointsendpoint-namerecordsrecord-idblob-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idendpointsendpoint-namerecordsrecord-idblob-get-openapi.md
- name: Backupify - Retrieve a list of exports for the specified backup_instance
  x-api-slug: v1backup-instancesbackup-instance-idexports-get
  description: You can only retrieve exports for backup_instances you have access
    to. Records are returned in ascending order (by id), with a default of 20 per
    page. Links to the next, previous, first, and last pages can be found in the response
    headers.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idexports-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idexports-get-openapi.md
- name: Backupify - Perform an export of the most recent backup of the specified backup_instance
  x-api-slug: v1backup-instancesbackup-instance-idexports-post
  description: Perform an export of the most recent backup of the specified backup_instance.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idexports-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idexports-post-openapi.md
- name: Backupify - Retrieve a specific export for the specified backup_instance
  x-api-slug: v1backup-instancesbackup-instance-idexportsexport-id-get
  description: You can only retrieve exports for backup_instances you have access
    to
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idexportsexport-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idexportsexport-id-get-openapi.md
- name: Backupify - Retrieve an updated exported_data_url for a specific export for
    the specified backup_instance
  x-api-slug: v1backup-instancesbackup-instance-idexportsexport-idreauth-post
  description: Retrieve an updated exported_data_url for a specific export for the
    specified backup_instance.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idexportsexport-idreauth-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idexportsexport-idreauth-post-openapi.md
- name: Backupify - Returns the logs for a given backup instance
  x-api-slug: v1backup-instancesbackup-instance-idlogs-get
  description: Returns the logs for a given backup instance.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idlogs-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idlogs-get-openapi.md
- name: Backupify - Returns the logs for a given backup instance
  x-api-slug: v1backup-instancesbackup-instance-idlogsscroll-id-get
  description: Returns the logs for a given backup instance.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idlogsscroll-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idlogsscroll-id-get-openapi.md
- name: Backupify - Retrieve a list of variables for the specified backup_instance
  x-api-slug: v1backup-instancesbackup-instance-idvariables-get
  description: You can only retrieve variables for backup_instances you have access
    to. Records are returned in ascending order (by id), with a default of 20 per
    page. Links to the next, previous, first, and last pages can be found in the response
    headers.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idvariables-get-openapi.md
- name: Backupify - Create a custom variable value for the specified key for the specified
    backup_instance
  x-api-slug: v1backup-instancesbackup-instance-idvariables-post
  description: The key specified must refer to the key of a previously defined backup_definition
    variable. It is only possible to create variables for backup_instances you have
    permission to manage.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idvariables-post-openapi.md
- name: Backupify - Retrieve a specific variable by key for the specified backup_instance
  x-api-slug: v1backup-instancesbackup-instance-idvariableskey-get
  description: You can only retrieve variables for backup_instances you have access
    to
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idvariableskey-get-openapi.md
- name: Backupify - Update the value of a variable by key for the specified backup_instance
  x-api-slug: v1backup-instancesbackup-instance-idvariableskey-put
  description: You can only alter variables for backup_instances you have access to
    manage
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idvariableskey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1backup-instancesbackup-instance-idvariableskey-put-openapi.md
- name: Backupify - Retrieve a list of customers associated with the authenticated
    vendor
  x-api-slug: v1customers-get
  description: Requires Access Token granted from client credentials. Records are
    returned in ascending order (by id), with a default of 20 per page. Links to the
    next, previous, first, and last pages can be found in the response headers.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1customers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1customers-get-openapi.md
- name: Backupify - Create a new customer instance identified by the given {name}
    identifier
  x-api-slug: v1customers-post
  description: Create a new customer instance identified by the given {name} identifier.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1customers-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1customers-post-openapi.md
- name: Backupify - Retrieves the customer identified by customer_id
  x-api-slug: v1customerscustomer-id-get
  description: Requires Access Token granted from client credentials.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1customerscustomer-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1customerscustomer-id-get-openapi.md
- name: Backupify - Update a customer instance identified by the given customer_id
  x-api-slug: v1customerscustomer-id-put
  description: Update a customer instance identified by the given customer_id.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1customerscustomer-id-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1customerscustomer-id-put-openapi.md
- name: Backupify - Retrieves a list of backup_instances associated with the specified
    customer
  x-api-slug: v1customerscustomer-idbackup-instances-get
  description: It is only possible to retrieve backup_instances for customers you
    are authorized to access. Records are returned in ascending order (by id), with
    a default of 20 per page. Links to the next, previous, first, and last pages can
    be found in the response headers.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1customerscustomer-idbackup-instances-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1customerscustomer-idbackup-instances-get-openapi.md
- name: Backupify - A simple method that returns a 200 response if the connection
    succeeds
  x-api-slug: v1ping-get
  description: A simple method that returns a 200 response if the connection succeeds.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1ping-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1ping-get-openapi.md
- name: Backupify - Provides information about the currently authenticated vendor
    user
  x-api-slug: v1vendorsme-get
  description: Provides information about the currently authenticated vendor user.
  image: ""
  humanURL: http://backupify.com
  baseURL: https://api.backupify.com//
  tags: API Not Found, API Provider, Backups, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1vendorsme-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/backupify/master/_listings/backupify/v1vendorsme-get-openapi.md
x-common:
- type: x-api-gallery
  url: http://azure.virtual.network.api.gallery.streamdata.io
- type: x-api-stack
  url: http://backupify.stack.network
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