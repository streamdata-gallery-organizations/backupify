{
  "info": {
    "name": "Backupify Retrieve an Access Token authenticated using the provided client_id and client_secret.",
    "_postman_id": "ef30f997-d39d-4bac-a48a-2dd776bf7c9c",
    "description": "All actions and visibility is limited in scope to items that are descendents of the authenticated vendor and the backup_definitions owned thereby. At this time, all Access Tokens are scoped with full write capabilities.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Oauth",
      "item": [
        {
          "id": "b774aad2-8e3b-47d4-99d6-0f24f1a36b4a",
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
              "id": "17742b59-44d2-4c63-ab00-84c9aabfbce9"
            }
          ]
        }
      ]
    }
  ]
}