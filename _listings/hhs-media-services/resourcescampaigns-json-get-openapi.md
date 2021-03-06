---
swagger: "2.0"
x-collection-name: HHS Media Services
x-complete: 0
info:
  title: HHS Media Services Get Campaigns
  description: Returns the list of Campaigns.
  termsOfService: http://www.hhs.gov/web/socialmedia/policies/tos.html#ready
  version: "2"
host: api.digitalmedia.hhs.gov
basePath: /api/v2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /resources.json:
    get:
      summary: Get Resources by search query
      description: Returns the list of Resources matching the search query 'q'.The
        search query 'q' is a Lucene query.The syntax for a Lucene query can be found
        here.
      operationId: getResources
      x-api-path-slug: resources-json-get
      parameters:
      - in: query
        name: q
        description: The search query supplied by the user
      responses:
        200:
          description: OK
      tags:
      - Resources
  /resources/campaigns.json:
    get:
      summary: Get Campaigns
      description: Returns the list of Campaigns.
      operationId: getCampaigns
      x-api-path-slug: resourcescampaigns-json-get
      parameters:
      - in: query
        name: max
        description: The maximum number of records to return
      - in: query
        name: offset
        description: The offset of the records set to return for pagination
      - in: query
        name: sort
        description: '* Set of fields to sort the records by'
      responses:
        200:
          description: OK
      tags:
      - Resources
      - Campaigns
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