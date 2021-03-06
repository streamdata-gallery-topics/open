---
swagger: "2.0"
x-collection-name: Postmark
x-complete: 1
info:
  title: Postmark
  description: send-emails-retrieve-bounces-and-start-accepting-inbound-emails-all-via-an-easytouse-http-api-
  version: 1.0.0
host: spamcheck.postmarkapp.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /messages/outbound/opens:
    get:
      summary: Get Messages Outbound Opens
      description: Get messages outbound opens.
      operationId: getMessagesOutboundOpens
      x-api-path-slug: messagesoutboundopens-get
      parameters:
      - in: query
        name: city
        description: Filter by full name of region messages were opened in, i
      - in: query
        name: client_company
        description: Filter by company, i
      - in: query
        name: client_family
        description: Filter by client family, i
      - in: query
        name: client_name
        description: Filter by client name, i
      - in: query
        name: count
        description: Number of message opens to return per request
      - in: query
        name: country
        description: Filter by country messages were opened in, i
      - in: query
        name: offset
        description: Number of messages to skip
      - in: query
        name: os_company
        description: Filter by company which produced the OS, i
      - in: query
        name: os_family
        description: Filter by kind of OS used without specific version, i
      - in: query
        name: os_name
        description: Filter by full OS name and specific version, i
      - in: query
        name: platform
        description: Filter by platform, i
      - in: query
        name: recipient
        description: Filter by To, Cc, Bcc
      - in: query
        name: region
        description: Filter by full name of region messages were opened in, i
      - in: query
        name: tag
        description: Filter by tag
      - in: header
        name: X-Postmark-Server-Token
        description: The token associated with the Server on which this request will
          operate
      responses:
        200:
          description: OK
      tags:
      - Messages
      - Outbound
      - Opens
  /messages/outbound/opens/{messageid}:
    get:
      summary: Get Messages Outbound Opens Message
      description: Get messages outbound opens message.
      operationId: getMessagesOutboundOpensMessage
      x-api-path-slug: messagesoutboundopensmessageid-get
      parameters:
      - in: query
        name: count
        description: Number of message opens to return per request
      - in: path
        name: messageid
        description: The ID of the Outbound Message for which open statistics should
          be retrieved
      - in: query
        name: offset
        description: Number of messages to skip
      - in: header
        name: X-Postmark-Server-Token
        description: The token associated with the Server on which this request will
          operate
      responses:
        200:
          description: OK
      tags:
      - Messages
      - Outbound
      - Opens
      - Messageid
  /stats/outbound/opens:
    get:
      summary: Get Stats Outbound Opens
      description: Get stats outbound opens.
      operationId: getStatsOutboundOpens
      x-api-path-slug: statsoutboundopens-get
      parameters:
      - in: query
        name: fromdate
        description: Filter stats starting from the date specified
      - in: query
        name: tag
        description: Filter by tag
      - in: query
        name: todate
        description: Filter stats up to the date specified
      - in: header
        name: X-Postmark-Server-Token
        description: The token associated with the Server on which this request will
          operate
      responses:
        200:
          description: OK
      tags:
      - Stats
      - Outbound
      - Opens
  /stats/outbound/opens/emailclients:
    get:
      summary: Get Stats Outbound Opens Emailclients
      description: Get stats outbound opens emailclients.
      operationId: getStatsOutboundOpensEmailclients
      x-api-path-slug: statsoutboundopensemailclients-get
      parameters:
      - in: query
        name: fromdate
        description: Filter stats starting from the date specified
      - in: query
        name: tag
        description: Filter by tag
      - in: query
        name: todate
        description: Filter stats up to the date specified
      - in: header
        name: X-Postmark-Server-Token
        description: The token associated with the Server on which this request will
          operate
      responses:
        200:
          description: OK
      tags:
      - Stats
      - Outbound
      - Opens
      - Emailclients
  /stats/outbound/opens/platforms:
    get:
      summary: Get Stats Outbound Opens Platforms
      description: Get stats outbound opens platforms.
      operationId: getStatsOutboundOpensPlatforms
      x-api-path-slug: statsoutboundopensplatforms-get
      parameters:
      - in: query
        name: fromdate
        description: Filter stats starting from the date specified
      - in: query
        name: tag
        description: Filter by tag
      - in: query
        name: todate
        description: Filter stats up to the date specified
      - in: header
        name: X-Postmark-Server-Token
        description: The token associated with the Server on which this request will
          operate
      responses:
        200:
          description: OK
      tags:
      - Stats
      - Outbound
      - Opens
      - Platforms
  /stats/outbound/opens/readtimes:
    get:
      summary: Get Stats Outbound Opens Readtimes
      description: Get stats outbound opens readtimes.
      operationId: getStatsOutboundOpensReadtimes
      x-api-path-slug: statsoutboundopensreadtimes-get
      parameters:
      - in: query
        name: fromdate
        description: Filter stats starting from the date specified
      - in: query
        name: tag
        description: Filter by tag
      - in: query
        name: todate
        description: Filter stats up to the date specified
      - in: header
        name: X-Postmark-Server-Token
        description: The token associated with the Server on which this request will
          operate
      responses:
        200:
          description: OK
      tags:
      - Stats
      - Outbound
      - Opens
      - Readtimes
---