---
swagger: "2.0"
x-collection-name: Zencoder
x-complete: 0
info:
  title: Zencoder API Get Usage for VOD
  version: v2
  description: Get Usage for VOD
host: app.zencoder.com
basePath: /api/v2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /reports/all:
    get:
      summary: Get Usage for VOD & Live
      description: Get Usage for VOD & Live
      operationId: getReportsAll
      x-api-path-slug: reportsall-get
      parameters:
      - in: query
        name: api_key
        description: The API key
      - in: query
        name: from
        description: 'Start date in the format YYYY-MM-DD (default: 30 days ago)'
      - in: query
        name: grouping
        description: 'Hour usage for only one report grouping (default: none)'
      - in: query
        name: to
        description: 'End date in the format YYYY-MM-DD (default: yesterday)'
      responses:
        200:
          description: OK
      tags:
      - Reports
  /reports/live:
    get:
      summary: Get Usage for Live
      description: Get Usage for Live
      operationId: getReportsLive
      x-api-path-slug: reportslive-get
      parameters:
      - in: query
        name: api_key
        description: The API key
      - in: query
        name: from
        description: 'Start date in the format YYYY-MM-DD (default: 30 days ago)'
      - in: query
        name: grouping
        description: 'Hour usage for only one report grouping (default: none)'
      - in: query
        name: to
        description: 'End date in the format YYYY-MM-DD (default: yesterday)'
      responses:
        200:
          description: OK
      tags:
      - Reports
      - Live
  /reports/minutes:
    get:
      summary: Get Minutes Used
      description: Get Minutes Used
      operationId: getReportsMinutes
      x-api-path-slug: reportsminutes-get
      parameters:
      - in: query
        name: api_key
        description: The API Key
      responses:
        200:
          description: OK
      tags:
      - Reports
      - Minutes
  /reports/vod:
    get:
      summary: Get Usage for VOD
      description: Get Usage for VOD
      operationId: getReportsVod
      x-api-path-slug: reportsvod-get
      parameters:
      - in: query
        name: api_key
        description: The API key
      - in: query
        name: from
        description: 'Start date in the format YYYY-MM-DD (default: 30 days ago)'
      - in: query
        name: grouping
        description: 'Minute usage for only one report grouping (default: none)'
      - in: query
        name: to
        description: 'End date in the format YYYY-MM-DD (default: yesterday)'
      responses:
        200:
          description: OK
      tags:
      - Reports
      - Vod
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