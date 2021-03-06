---
swagger: "2.0"
x-collection-name: Site24x7
x-complete: 0
info:
  title: Scheduled Report API Update Scheduled Report
  description: Update the configuration of an existing Scheduled Report.
  version: 1.0.0
host: www.site24x7.com.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /scheduled_reports:
    post:
      summary: Schedule a Report
      description: Schedule a report to be received on a specific day and time.
      operationId: schedule-a-report
      x-api-path-slug: scheduled-reports-post
      parameters:
      - in: path
        name: "display_name\n        \n        \n            required\n            Display
          name for the Report.\n        \n    \n    \n        \n        report_type\n
          \       \n        \n            required\n            Type of report to
          be Scheduled.Report Constants"
      responses:
        "":
          description: ""
        400:
          description: Bad input parameter
        401:
          description: Bad or expired token
        403:
          description: Bad OAuth request (wrong consumer key, bad nonce, expired timestamp
        404:
          description: File or folder not found at the specified path
        405:
          description: Request method not expected (generally should be GET or POST)
        429:
          description: Your app is making too many requests and is being rate limited
        503:
          description: If the response includes the Retry-After header, this means
            your OAuth 1
        507:
          description: User is over Dropbox storage quota
        5xx:
          description: Server error
        Maximum record size:
          description: 100 KiB
        Maximum number of records per datastore:
          description: "100,000"
        Maximum datastore size:
          description: 10 MiB
        Maximum size of a delta:
          description: 2 MiB
        200:
          description: OK
      tags:
      - Scheduled Reports
  /scheduled_reports/{report_id}:
    put:
      summary: Update Scheduled Report
      description: Update the configuration of an existing Scheduled Report.
      operationId: update-scheduled-report
      x-api-path-slug: scheduled-reportsreport-id-put
      parameters:
      - in: path
        name: "display_name\n        \n        \n            required\n            Display
          name for the Report.\n        \n    \n    \n        \n        report_type\n
          \       \n        \n            required\n            Type of report to
          be Scheduled.Report Constants"
      responses:
        200:
          description: OK
      tags:
      - Scheduled Reports
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