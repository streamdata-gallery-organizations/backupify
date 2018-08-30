---
swagger: "2.0"
x-collection-name: Backupify
x-complete: 0
info:
  title: Backupify Retrieve an Access Token authenticated using the provided client_id
    and client_secret.
  description: All actions and visibility is limited in scope to items that are descendents
    of the authenticated vendor and the backup_definitions owned thereby. At this
    time, all Access Tokens are scoped with full write capabilities.
  version: 1.0.0
host: api.backupify.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /oauth/token:
    post:
      summary: Retrieve an Access Token authenticated using the provided client_id
        and client_secret.
      description: All actions and visibility is limited in scope to items that are
        descendents of the authenticated vendor and the backup_definitions owned thereby.
        At this time, all Access Tokens are scoped with full write capabilities.
      operationId: postOauthToken
      x-api-path-slug: oauthtoken-post
      parameters:
      - in: formData
        name: client_id
        description: API Client ID
      - in: formData
        name: client_secret
        description: API Client secret
      - in: formData
        name: grant_type
        description: String identifying the grant type to be used for token retrieval
      - in: formData
        name: scope
        description: A space separated list of operational scopes available to the
          returned token
      responses:
        200:
          description: OK
      tags:
      - Oauth
      - Token
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---