---
swagger: "2.0"
x-collection-name: Predix
x-complete: 0
info:
  title: Predix Enterprise Connect Get the EC system account
  description: Get an existing EC system account by predix zone id
  version: 1.0.0
host: ec-predix-service-osaka.run.aws-usw02-pr.ice.predix.io
basePath: /v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /admin/accounts/{predix-zone-id}:
    put:
      summary: Update the EC gateway setting in the account
      description: Update the EC gateway setting in the account with the CF details
      operationId: update-the-ec-gateway-setting-in-the-account-with-the-cf-details
      x-api-path-slug: adminaccountspredixzoneid-put
      parameters:
      - in: header
        name: Authorization
        description: Basic *token
      - in: path
        name: predix-zone-id
        description: Predix Zone Id
      - in: body
        name: settings
        description: Cloud Foundry setting destails
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: Successful response
      tags:
      - EC
      - Gateway
      - Setting
      - In
      - Account
    delete:
      summary: Delete the EC system account
      description: Delete an existing EC system account by predix zone id
      operationId: delete-an-existing-ec-system-account-by-predix-zone-id
      x-api-path-slug: adminaccountspredixzoneid-delete
      parameters:
      - in: header
        name: Authorization
        description: Basic *token
      - in: path
        name: predix-zone-id
        description: pass the predix zone id
      responses:
        200:
          description: Successful response
      tags:
      - EC
      - System
      - Account
    get:
      summary: Get the EC system account
      description: Get an existing EC system account by predix zone id
      operationId: get-an-existing-ec-system-account-by-predix-zone-id
      x-api-path-slug: adminaccountspredixzoneid-get
      parameters:
      - in: header
        name: Authorization
        description: Basic *token
      - in: path
        name: predix-zone-id
        description: pass the predix zone id
      responses:
        200:
          description: Successful response
      tags:
      - EC
      - System
      - Account
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