---
swagger: "2.0"
x-collection-name: ConvertAPI
x-complete: 0
info:
  title: Convert API Open Office to Image
  description: The API for converting OpenOffice documents to PDF files and Images.
    These file formats mml, odc, odf, odg, odi, odm, odp, ods, odt, otg, oth, otp,
    ots, pxl, sgl, smf, srw, stc, sti, stw, sxc, sxg, sxi, sxm, sxw, vor, wv2 can
    be converted to png, jpg, tif.
  version: v1
host: do.convertapi.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /OpenOffice2Image:
    post:
      summary: Open Office to Image
      description: The API for converting OpenOffice documents to PDF files and Images.
        These file formats mml, odc, odf, odg, odi, odm, odp, ods, odt, otg, oth,
        otp, ots, pxl, sgl, smf, srw, stc, sti, stw, sxc, sxg, sxi, sxm, sxw, vor,
        wv2 can be converted to png, jpg, tif.
      operationId: openoffice2image
      x-api-path-slug: openoffice2image-post
      parameters:
      - in: query
        name: AlternativeParser
        description: If some objects are missing in converted Pdf files from original
          source files this option can be enabled to improve conversion
      - in: query
        name: ApiKey
        description: API Key should be passed if you purchased membership with credits
      - in: query
        name: File
        description: 'Supported source file formats: mml, odc, odf, odg, odi, odm,
          odp, ods, odt, otg, oth, otp, ots, pxl, sgl, smf, srw, stc, sti, stw, sxc,
          sxg, sxi, sxm, sxw, vor, wv2'
      - in: query
        name: ImageResolutionH
        description: Image horizontal resolution (DPI)
      - in: query
        name: ImageResolutionV
        description: Image vertical resolution (DPI)
      - in: query
        name: JpgQuality
        description: Jpg image quality
      - in: query
        name: OutputFormat
        description: Supported output file formats png, jpg, tif
      - in: query
        name: StoreFile
        description: Store file on server and return url to file instead of file stream
          response
      - in: query
        name: Timeout
        description: Conversion timeout in seconds
      responses:
        200:
          description: OK
      tags:
      - Open
      - Office
      - Image
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