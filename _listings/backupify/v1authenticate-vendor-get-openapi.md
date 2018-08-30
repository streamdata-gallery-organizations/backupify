---
swagger: "2.0"
x-collection-name: Backupify
x-complete: 0
info:
  title: Backupify A simple method to test authentication of a vendor access token.
    The response body is empty JSON object.
  description: A simple method to test authentication of a vendor access token. the
    response body is empty json object..
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
  /v1/authenticate_customer:
    get:
      summary: A simple method to test authentication of a customer access token.
      description: A simple method to test authentication of a customer access token..
      operationId: getV1AuthenticateCustomer
      x-api-path-slug: v1authenticate-customer-get
      parameters:
      - in: header
        name: Authorization
        description: Bearer Access Token granted for customer
      responses:
        200:
          description: OK
      tags:
      - V1
      - Authenticate
      - Customer
  /v1/authenticate_vendor:
    get:
      summary: A simple method to test authentication of a vendor access token. The
        response body is empty JSON object.
      description: A simple method to test authentication of a vendor access token.
        the response body is empty json object..
      operationId: getV1AuthenticateVendor
      x-api-path-slug: v1authenticate-vendor-get
      parameters:
      - in: header
        name: Authorization
        description: Bearer Access Token granted from client_credentials for vendor
      responses:
        200:
          description: OK
      tags:
      - V1
      - Authenticate
      - Vendor
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