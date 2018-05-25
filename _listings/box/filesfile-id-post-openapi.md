---
swagger: "2.0"
x-collection-name: Box
x-complete: 0
info:
  title: Box Restore Item
  description: Restores an item that has been moved to the trash. Default behavior
    is to restore the item to the folder it was in before it was moved to the trash.
    If that parent folder no longer exists or if there is now an item with the same
    name in that parent folder, the new parent folder and/or new name will need to
    be included in the request.
  version: 1.0.0
host: api.box.com
basePath: /2.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /files/content:
    options:
      summary: File upload preflight check
      description: The Pre-flight check API will verify that a file will be accepted
        by Box before you send all the bytes over the wire.
      operationId: fileUploadPreflightCheck
      x-api-path-slug: filescontent-options
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Documents
      - Files
      - Content
  /files/{FILE_ID}:
    get:
      summary: Get File's Info, Get Embed Link
      description: Used to retrieve the metadata about a file.
      operationId: getFile
      x-api-path-slug: filesfile-id-get
      parameters:
      - in: query
        name: fields
        description: Attribute(s) to include in the response
      - in: path
        name: FILE_ID
      responses:
        200:
          description: OK
      tags:
      - Documents
      - Files
      - File
    put:
      summary: Update File Info, Lock and Unlock, Create Shared Link
      description: |-
        Used to update individual or multiple fields in the file object, including renaming the file, changing its description, and creating a shared link for the file. To move a file, change the ID of its parent folder. An optional If-Match header can be included to prevent race conditions.

        To lock and unlock files, you execute a PUT operation on the /files/{file id} endpoint and set or clear the lock properties on the file.

        Used to create a shared link for this particular file. Please see here for more information on the permissions available for shared links. In order to get default shared link status, set it to an empty access level, i.e. {"shared_link": {}}. In order to disable a shared link, send this same type of PUT request with the value of shared_link set to null, i.e. {"shared_link": null}
      operationId: updateFileInfo
      x-api-path-slug: filesfile-id-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: FILE_ID
      - in: header
        name: If-Match
        description: The etag of the file can be included as an If-Match header to
          prevent race conditions
      responses:
        200:
          description: OK
      tags:
      - Documents
      - Files
      - File
    delete:
      summary: Delete File
      description: "Discards a file to the trash. The etag of the file can be included
        as an \u2018If-Match\u2019 header to prevent race conditions."
      operationId: deleteFile
      x-api-path-slug: filesfile-id-delete
      parameters:
      - in: path
        name: FILE_ID
      - in: header
        name: If-Match
        description: The etag of the file
      responses:
        200:
          description: OK
      tags:
      - Documents
      - Files
      - File
    post:
      summary: Restore Item
      description: Restores an item that has been moved to the trash. Default behavior
        is to restore the item to the folder it was in before it was moved to the
        trash. If that parent folder no longer exists or if there is now an item with
        the same name in that parent folder, the new parent folder and/or new name
        will need to be included in the request.
      operationId: restoreTrashedFile
      x-api-path-slug: filesfile-id-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: FILE_ID
      responses:
        200:
          description: OK
      tags:
      - Documents
      - Files
      - File
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