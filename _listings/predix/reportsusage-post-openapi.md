---
swagger: "2.0"
x-collection-name: Predix
x-complete: 0
info:
  title: Predix Enterprise Connect Report usage
  description: Report usage by zoneid
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
  /reports/usage:
    post:
      summary: Report usage
      description: Report usage by zoneid
      operationId: report-usage-by-zoneid
      x-api-path-slug: reportsusage-post
      parameters:
      - in: header
        name: Authorization
        description: Basic *token
      - in: body
        name: content
        description: The content for reporting the usage
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: predix-zone-id
        description: Cloud Foundry service instance id
      responses:
        200:
          description: Successful response
      tags:
      - Report
      - Usage
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