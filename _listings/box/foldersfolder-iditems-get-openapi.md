---
swagger: "2.0"
x-collection-name: Box
x-complete: 0
info:
  title: "Box Get Folder\u2019s Items"
  description: Retrieves the files and/or folders contained within this folder without
    any other metadata about the folder. Any attribute in the full files or folders
    objects can be passed in with the fields parameter to get specific attributes,
    and only those specific attributes back; otherwise, the mini format is returned
    for each item by default. Multiple attributes can be passed in separated by commas
    e.g. fields=name,created_at. Paginated results can be retrieved using the limit
    and offset parameters.
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
  /files/{FILE_ID}/content:
    get:
      summary: Download File
      description: Retrieves the actual data of the file. An optional version parameter
        can be set to download a previous version of the file.
      operationId: getFileContent
      x-api-path-slug: filesfile-idcontent-get
      parameters:
      - in: header
        name: BoxApi
        description: The shared link for this item
      - in: path
        name: FILE_ID
      - in: header
        name: Range
        description: The range value in bytes
      - in: query
        name: version
        description: The ID specific version of this file to download
      responses:
        200:
          description: OK
      tags:
      - Documents
      - Files
      - File
      - ""
      - Content
  /files/{FILE_ID}/versions:
    get:
      summary: View Versions
      description: If there are previous versions of this file, this method can be
        used to retrieve information about the older versions. (Versions are only
        tracked for Box users with premium accounts.)
      operationId: getFileVersions
      x-api-path-slug: filesfile-idversions-get
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
      - ""
      - Versions
  /files/{FILE_ID}/versions/current:
    post:
      summary: Promote Version
      description: If there are previous versions of this file, this method can be
        used to promote one of the older versions to the top of the stack. This actually
        mints a copy of the old version and puts it on the top of the versions stack.
        The file will have the exact same contents, the same SHA1/etag, and the same
        name as the original. Other properties such as comments do not get updated
        to their former values.
      operationId: promotoeFileVersion
      x-api-path-slug: filesfile-idversionscurrent-post
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
      - ""
      - Versions
      - Current
  /files/{FILE_ID}/versions/{VERSION_ID}:
    delete:
      summary: Delete Old Version
      description: Discards a specific file version to the trash. (Depending on the
        enterprise settings for this user, the item will either be actually deleted
        from Box or moved to the trash.)
      operationId: deleteFileVersion
      x-api-path-slug: filesfile-idversionsversion-id-delete
      parameters:
      - in: path
        name: FILE_ID
      - in: header
        name: If-Match
        description: The etag of the file
      - in: path
        name: VERSION_ID
      responses:
        200:
          description: OK
      tags:
      - Documents
      - Files
      - File
      - ""
      - Versions
      - Version
  /files/{FILE_ID}/copy:
    post:
      summary: Copy File
      description: Used to create a copy of a file in another folder. The original
        version of the file will not be altered.
      operationId: copyFile
      x-api-path-slug: filesfile-idcopy-post
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
      - ""
      - Copy
  /files/{FILE_ID}/thumbnail.{EXTENSION}:
    get:
      summary: Get Thumbnail
      description: Retrieves a thumbnail, or smaller image representation, of this
        file. Sizes of 32x32,64x64, 128x128, and 256x256 can be returned in the .png
        format and sizes of 32x32, 94x94, 160x160, and 320x320 can be returned in
        the .jpg format. Thumbnails can be generated for the image and video file
        formats listed here.
      operationId: getFileThumbnail
      x-api-path-slug: filesfile-idthumbnail-extension-get
      parameters:
      - in: path
        name: EXTENSION
        description: The preview format, e
      - in: path
        name: FILE_ID
      - in: query
        name: max_height
        description: The maximum height of the thumbnail
      - in: query
        name: max_width
        description: The maximum width of the thumbnail
      - in: query
        name: min_height
        description: The minimum height of the thumbnail
      - in: query
        name: min_width
        description: The minimum width of the thumbnail
      responses:
        200:
          description: OK
      tags:
      - Documents
      - Files
      - File
      - ""
      - Thumbnail.
      - Extension
  /files/{FILE_ID}/trash:
    get:
      summary: Get Trashed File
      description: Retrieves an item that has been moved to the trash.
      operationId: getTrashedFile
      x-api-path-slug: filesfile-idtrash-get
      parameters:
      - in: path
        name: FILE_ID
      responses:
        200:
          description: OK
      tags:
      - Documents
      - Files
      - File
      - ""
      - Trash
    delete:
      summary: Permanently Delete
      description: Permanently deletes an item that is in the trash. The item will
        no longer exist in Box. This action cannot be undone.
      operationId: deleteTrashedFile
      x-api-path-slug: filesfile-idtrash-delete
      parameters:
      - in: path
        name: FILE_ID
      responses:
        200:
          description: OK
      tags:
      - Documents
      - Files
      - File
      - ""
      - Trash
  /files/{FILE_ID}/comments:
    get:
      summary: Get File's Comments
      description: Retrieves the comments on a particular file, if any exist.
      operationId: getFileComments
      x-api-path-slug: filesfile-idcomments-get
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
      - ""
      - Comments
  /files/{FILE_ID}/collaborations:
    get:
      summary: Get File's Collaborations
      description: Use this to get a list of all the collaborations on a file
      operationId: getFileCollaborations
      x-api-path-slug: filesfile-idcollaborations-get
      parameters:
      - in: query
        name: fields
        description: Attribute(s) to include in the response
      - in: path
        name: FILE_ID
      - in: query
        name: limit
        description: The maximum number of items to return in a page
      - in: query
        name: offset
        description: The item at which to begin the response
      responses:
        200:
          description: OK
      tags:
      - Documents
      - Files
      - File
      - ""
      - Collaborations
  /files/{FILE_ID}/tasks:
    get:
      summary: Get File's Tasks
      description: Retrieves all of the tasks for given file.
      operationId: getFileTasks
      x-api-path-slug: filesfile-idtasks-get
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
      - ""
      - Tasks
  /folders:
    post:
      summary: Create Folder
      description: Used to create a new empty folder. The new folder will be created
        inside of the specified parent folder
      operationId: createFolder
      x-api-path-slug: folders-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: fields
        description: Attribute(s) to include in the response
      responses:
        200:
          description: OK
      tags:
      - Documents
      - Folders
  /folders/{FOLDER_ID}:
    get:
      summary: Get Folder's Info
      description: "Retrieves the full metadata about a folder, including information
        about when it was last updated as well as the files and folders contained
        in it. The root folder of a Box account is always represented by the id \u201C0\u201D."
      operationId: getFolder
      x-api-path-slug: foldersfolder-id-get
      parameters:
      - in: query
        name: fields
        description: Attribute(s) to include in the response
      - in: path
        name: FOLDER_ID
      responses:
        200:
          description: OK
      tags:
      - Documents
      - Folders
      - Folder
    put:
      summary: Update Folder, Create Shared Link, Create or Delete
      description: "Used to update information about the folder. To move a folder,
        update the ID of its parent. To enable an email address that can be used to
        upload files to this folder, update the folder_upload_email attribute. An
        optional If-Match header can be included to ensure that client only updates
        the folder if it knows about the latest version.\n\nUsed to create a shared
        link for this particular folder. Please see here for more information on the
        permissions available for shared links. In order to get default shared link
        status, set it to an empty access level, i.e. {\"shared_link\": {}}. In order
        to disable a shared link, send this same type of PUT request with the value
        of shared_link set to null, i.e. {\"shared_link\": null}\n\nTo add or remove
        an item from a collection, you do a PUT on that item and change the list of
        collections it belongs to. Philosophically, this is similar to the way \u201Cmove\u201D
        operations work on files and folders: you do a PUT on the item and change
        its parent. It\u2019s the same idea with collections, except you\u2019re changing
        which collection(s) the item belongs to instead of the folder it belongs to.
        Currently the only collection available is the favorites collection, and you\u2019ll
        need to know it\u2019s ID for the user that is making the API call, since
        every user has a different favorites collection_id.\nThe Add/Remove API handling
        will check all ids passed in before performing any add/removal operations.
        If any collection ids are malformed or do not exist in the user\u2019s account,
        the API call will throw a 400. Only if all of the collection ids are valid
        will the adds and removals be carried out."
      operationId: updateFolder
      x-api-path-slug: foldersfolder-id-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: fields
        description: Attribute(s) to include in the response
      - in: path
        name: FOLDER_ID
      - in: header
        name: If-Match
        description: This is in the etag field of the folder object
      responses:
        200:
          description: OK
      tags:
      - Documents
      - Folders
      - Folder
    delete:
      summary: Delete Folder
      description: Used to delete a folder. A recursive parameter must be included
        in order to delete folders that have items inside of them. An optional If-Match
        header can be included to ensure that client only deletes the folder if it
        knows about the latest version.
      operationId: deleteFolder
      x-api-path-slug: foldersfolder-id-delete
      parameters:
      - in: path
        name: FOLDER_ID
      - in: header
        name: If-Match
        description: This is in the etag field of the folder object
      - in: query
        name: recursive
      responses:
        200:
          description: OK
      tags:
      - Documents
      - Folders
      - Folder
    post:
      summary: Restore Folder
      description: Restores an item that has been moved to the trash. Default behavior
        is to restore the item to the folder it was in before it was moved to the
        trash. If that parent folder no longer exists or if there is now an item with
        the same name in that parent folder, the new parent folder and/or new name
        will need to be included in the request.
      operationId: restoreTrashedFolder
      x-api-path-slug: foldersfolder-id-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: fields
        description: Attribute(s) to include in the response
      - in: path
        name: FOLDER_ID
      responses:
        200:
          description: OK
      tags:
      - Documents
      - Folders
      - Folder
  /folders/{FOLDER_ID}/items:
    get:
      summary: "Get Folder\u2019s Items"
      description: Retrieves the files and/or folders contained within this folder
        without any other metadata about the folder. Any attribute in the full files
        or folders objects can be passed in with the fields parameter to get specific
        attributes, and only those specific attributes back; otherwise, the mini format
        is returned for each item by default. Multiple attributes can be passed in
        separated by commas e.g. fields=name,created_at. Paginated results can be
        retrieved using the limit and offset parameters.
      operationId: getFolderItems
      x-api-path-slug: foldersfolder-iditems-get
      parameters:
      - in: query
        name: fields
        description: Attribute(s) to include in the response
      - in: path
        name: FOLDER_ID
      - in: query
        name: limit
        description: The maximum number of items to return in a page
      - in: query
        name: offset
        description: The offset at which to begin the response
      responses:
        200:
          description: OK
      tags:
      - Documents
      - Folders
      - Folder
      - ""
      - Items
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