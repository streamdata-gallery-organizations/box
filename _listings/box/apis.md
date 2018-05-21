---
name: Box
x-slug: box
description: Box Inc. (formerly Box.net) is an online file sharing and Cloud content
  management service for enterprise companies. The company has adopted a freemium
  business model, and provides 5 GB of free storage [3] for personal accounts. A mobile
  version of the service is available for Android, BlackBerry, iOS, WebOS, and Windows
  Phone devices. The company is based in Los Altos, California.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
x-kinRank: "9"
x-alexaRank: ""
tags: Box
created: "2018-05-21"
modified: "2018-05-21"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/apis.md
specificationVersion: "0.14"
apis:
- name: Box File upload preflight check
  x-api-slug: box
  description: The Pre-flight check API will verify that a file will be accepted by
    Box before you send all the bytes over the wire.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//files/content
  tags: Documents,Files, Content
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filescontent-options-openapi.md
- name: Box Get File's Info, Get Embed Link
  x-api-slug: box
  description: Used to retrieve the metadata about a file.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//files/{FILE_ID}
  tags: Documents,Files, File
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-id-get-openapi.md
- name: Box Update File Info, Lock and Unlock, Create Shared Link
  x-api-slug: box
  description: |-
    Used to update individual or multiple fields in the file object, including renaming the file, changing its description, and creating a shared link for the file. To move a file, change the ID of its parent folder. An optional If-Match header can be included to prevent race conditions.

    To lock and unlock files, you execute a PUT operation on the /files/{file id} endpoint and set or clear the lock properties on the file.

    Used to create a shared link for this particular file. Please see here for more information on the permissions available for shared links. In order to get default shared link status, set it to an empty access level, i.e. {"shared_link": {}}. In order to disable a shared link, send this same type of PUT request with the value of shared_link set to null, i.e. {"shared_link": null}
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//files/{FILE_ID}
  tags: Documents,Files, File
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-id-put-openapi.md
- name: Box Delete File
  x-api-slug: box
  description: "Discards a file to the trash. The etag of the file can be included
    as an \u2018If-Match\u2019 header to prevent race conditions."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//files/{FILE_ID}
  tags: Documents,Files, File
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-id-delete-openapi.md
- name: Box Restore Item
  x-api-slug: box
  description: Restores an item that has been moved to the trash. Default behavior
    is to restore the item to the folder it was in before it was moved to the trash.
    If that parent folder no longer exists or if there is now an item with the same
    name in that parent folder, the new parent folder and/or new name will need to
    be included in the request.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//files/{FILE_ID}
  tags: Documents,Files, File
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-id-post-openapi.md
- name: Box Download File
  x-api-slug: box
  description: Retrieves the actual data of the file. An optional version parameter
    can be set to download a previous version of the file.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//files/{FILE_ID}/content
  tags: Documents,Files, File, , Content
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-idcontent-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-idcontent-get-openapi.md
- name: Box View Versions
  x-api-slug: box
  description: If there are previous versions of this file, this method can be used
    to retrieve information about the older versions. (Versions are only tracked for
    Box users with premium accounts.)
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//files/{FILE_ID}/versions
  tags: Documents,Files, File, , Versions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-idversions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-idversions-get-openapi.md
- name: Box Promote Version
  x-api-slug: box
  description: If there are previous versions of this file, this method can be used
    to promote one of the older versions to the top of the stack. This actually mints
    a copy of the old version and puts it on the top of the versions stack. The file
    will have the exact same contents, the same SHA1/etag, and the same name as the
    original. Other properties such as comments do not get updated to their former
    values.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//files/{FILE_ID}/versions/current
  tags: Documents,Files, File, , Versions, Current
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-idversionscurrent-post-openapi.md
- name: Box Delete Old Version
  x-api-slug: box
  description: Discards a specific file version to the trash. (Depending on the enterprise
    settings for this user, the item will either be actually deleted from Box or moved
    to the trash.)
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//files/{FILE_ID}/versions/{VERSION_ID}
  tags: Documents,Files, File, , Versions, Version
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-idversionsversion-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-idversionsversion-id-delete-openapi.md
- name: Box Copy File
  x-api-slug: box
  description: Used to create a copy of a file in another folder. The original version
    of the file will not be altered.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//files/{FILE_ID}/copy
  tags: Documents,Files, File, , Copy
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-idcopy-post-openapi.md
- name: Box Get Thumbnail
  x-api-slug: box
  description: Retrieves a thumbnail, or smaller image representation, of this file.
    Sizes of 32x32,64x64, 128x128, and 256x256 can be returned in the .png format
    and sizes of 32x32, 94x94, 160x160, and 320x320 can be returned in the .jpg format.
    Thumbnails can be generated for the image and video file formats listed here.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//files/{FILE_ID}/thumbnail.{EXTENSION}
  tags: Documents,Files, File, , Thumbnail., Extension
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-idthumbnailextension-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-idthumbnailextension-get-openapi.md
- name: Box Get Trashed File
  x-api-slug: box
  description: Retrieves an item that has been moved to the trash.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//files/{FILE_ID}/trash
  tags: Documents,Files, File, , Trash
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-idtrash-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-idtrash-get-openapi.md
- name: Box Permanently Delete
  x-api-slug: box
  description: Permanently deletes an item that is in the trash. The item will no
    longer exist in Box. This action cannot be undone.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//files/{FILE_ID}/trash
  tags: Documents,Files, File, , Trash
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-idtrash-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-idtrash-delete-openapi.md
- name: Box Get File's Comments
  x-api-slug: box
  description: Retrieves the comments on a particular file, if any exist.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//files/{FILE_ID}/comments
  tags: Documents,Files, File, , Comments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-idcomments-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-idcomments-get-openapi.md
- name: Box Get File's Collaborations
  x-api-slug: box
  description: Use this to get a list of all the collaborations on a file
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//files/{FILE_ID}/collaborations
  tags: Documents,Files, File, , Collaborations
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-idcollaborations-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-idcollaborations-get-openapi.md
- name: Box Get File's Tasks
  x-api-slug: box
  description: Retrieves all of the tasks for given file.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//files/{FILE_ID}/tasks
  tags: Documents,Files, File, , Tasks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-idtasks-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-idtasks-get-openapi.md
- name: Box Create Folder
  x-api-slug: box
  description: Used to create a new empty folder. The new folder will be created inside
    of the specified parent folder
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//folders
  tags: Documents,Folders
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/folders-post-openapi.md
- name: Box Get Folder's Info
  x-api-slug: box
  description: "Retrieves the full metadata about a folder, including information
    about when it was last updated as well as the files and folders contained in it.
    The root folder of a Box account is always represented by the id \u201C0\u201D."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//folders/{FOLDER_ID}
  tags: Documents,Folders, Folder
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/foldersfolder-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/foldersfolder-id-get-openapi.md
- name: Box Update Folder, Create Shared Link, Create or Delete
  x-api-slug: box
  description: "Used to update information about the folder. To move a folder, update
    the ID of its parent. To enable an email address that can be used to upload files
    to this folder, update the folder_upload_email attribute. An optional If-Match
    header can be included to ensure that client only updates the folder if it knows
    about the latest version.\n\nUsed to create a shared link for this particular
    folder. Please see here for more information on the permissions available for
    shared links. In order to get default shared link status, set it to an empty access
    level, i.e. {\"shared_link\": {}}. In order to disable a shared link, send this
    same type of PUT request with the value of shared_link set to null, i.e. {\"shared_link\":
    null}\n\nTo add or remove an item from a collection, you do a PUT on that item
    and change the list of collections it belongs to. Philosophically, this is similar
    to the way \u201Cmove\u201D operations work on files and folders: you do a PUT
    on the item and change its parent. It\u2019s the same idea with collections, except
    you\u2019re changing which collection(s) the item belongs to instead of the folder
    it belongs to. Currently the only collection available is the favorites collection,
    and you\u2019ll need to know it\u2019s ID for the user that is making the API
    call, since every user has a different favorites collection_id.\nThe Add/Remove
    API handling will check all ids passed in before performing any add/removal operations.
    If any collection ids are malformed or do not exist in the user\u2019s account,
    the API call will throw a 400. Only if all of the collection ids are valid will
    the adds and removals be carried out."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//folders/{FOLDER_ID}
  tags: Documents,Folders, Folder
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/foldersfolder-id-put-openapi.md
- name: Box Delete Folder
  x-api-slug: box
  description: Used to delete a folder. A recursive parameter must be included in
    order to delete folders that have items inside of them. An optional If-Match header
    can be included to ensure that client only deletes the folder if it knows about
    the latest version.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//folders/{FOLDER_ID}
  tags: Documents,Folders, Folder
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/foldersfolder-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/foldersfolder-id-delete-openapi.md
- name: Box Restore Folder
  x-api-slug: box
  description: Restores an item that has been moved to the trash. Default behavior
    is to restore the item to the folder it was in before it was moved to the trash.
    If that parent folder no longer exists or if there is now an item with the same
    name in that parent folder, the new parent folder and/or new name will need to
    be included in the request.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//folders/{FOLDER_ID}
  tags: Documents,Folders, Folder
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/foldersfolder-id-post-openapi.md
- name: "Box Get Folder\u2019s Items"
  x-api-slug: box
  description: Retrieves the files and/or folders contained within this folder without
    any other metadata about the folder. Any attribute in the full files or folders
    objects can be passed in with the fields parameter to get specific attributes,
    and only those specific attributes back; otherwise, the mini format is returned
    for each item by default. Multiple attributes can be passed in separated by commas
    e.g. fields=name,created_at. Paginated results can be retrieved using the limit
    and offset parameters.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//folders/{FOLDER_ID}/items
  tags: Documents,Folders, Folder, , Items
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/foldersfolder-iditems-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/foldersfolder-iditems-get-openapi.md
- name: Box Copy Folder
  x-api-slug: box
  description: Used to create a copy of a folder in another folder. The original version
    of the folder will not be altered.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//folders/{FOLDER_ID}/copy
  tags: Documents,Folders, Folder, , Copy
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/foldersfolder-idcopy-post-openapi.md
- name: Box Get Folder Collaborations
  x-api-slug: box
  description: Use this to get a list of all the collaborations on a folder i.e. all
    of the users that have access to that folder.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//folders/{FOLDER_ID}/collaborations
  tags: Documents,Folders, Folder, , Collaborations
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/foldersfolder-idcollaborations-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/foldersfolder-idcollaborations-get-openapi.md
- name: Box Get Trashed Folder
  x-api-slug: box
  description: Retrieves an folder that has been moved to the trash.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//folders/{FOLDER_ID}/trash
  tags: Documents,Folders, Folder, , Trash
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/foldersfolder-idtrash-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/foldersfolder-idtrash-get-openapi.md
- name: Box Permanently Delete
  x-api-slug: box
  description: Permanently deletes an folder that is in the trash. The item will no
    longer exist in Box. This action cannot be undone.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//folders/{FOLDER_ID}/trash
  tags: Documents,Folders, Folder, , Trash
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/foldersfolder-idtrash-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/foldersfolder-idtrash-delete-openapi.md
- name: Box Get Trashed Items
  x-api-slug: box
  description: Retrieves the files and/or folders that have been moved to the trash.
    Any attribute in the full files or folders objects can be passed in with the fields
    parameter to get specific attributes, and only those specific attributes back;
    otherwise, the mini format is returned for each item by default. Multiple attributes
    can be passed in separated by commas e.g. fields=name,created_at. Paginated results
    can be retrieved using the limit and offset parameters.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//folders/trash/items
  tags: Documents,Folders, Trash, Items
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/folderstrashitems-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/folderstrashitems-get-openapi.md
- name: Box Get Watermark on File
  x-api-slug: box
  description: Used to retrieve the watermark for a corresponding Box file.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//files/{FILE_ID}/watermark
  tags: Documents,Files, File, , Watermark
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-idwatermark-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-idwatermark-get-openapi.md
- name: Box Apply Watermark on File
  x-api-slug: box
  description: Used to apply or update the watermark for a corresponding Box file.
    The endpoint accepts a JSON body describing the watermark to apply.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//files/{FILE_ID}/watermark
  tags: Documents,Files, File, , Watermark
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-idwatermark-put-openapi.md
- name: Box Remove Watermark on File
  x-api-slug: box
  description: Used to remove the watermark for a corresponding Box file.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//files/{FILE_ID}/watermark
  tags: Documents,Files, File, , Watermark
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-idwatermark-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-idwatermark-delete-openapi.md
- name: Box Get Watermark on Folder
  x-api-slug: box
  description: Used to retrieve the watermark for a corresponding Box folder.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//folders/{FOLDER_ID}/watermark
  tags: Documents,Folders, Folder, , Watermark
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/foldersfolder-idwatermark-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/foldersfolder-idwatermark-get-openapi.md
- name: Box Apply Watermark on Folder
  x-api-slug: box
  description: Used to apply or update the watermark for a corresponding Box folder.
    The endpoints accepts a JSON body describing the watermark to apply.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//folders/{FOLDER_ID}/watermark
  tags: Documents,Folders, Folder, , Watermark
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/foldersfolder-idwatermark-put-openapi.md
- name: Box Remove Watermark on Folder
  x-api-slug: box
  description: Used to remove the watermark for a corresponding Box Folder.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//folders/{FOLDER_ID}/watermark
  tags: Documents,Folders, Folder, , Watermark
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/foldersfolder-idwatermark-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/foldersfolder-idwatermark-delete-openapi.md
- name: Box Create Web Link
  x-api-slug: box
  description: Creates a web link object within a given folder.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//web_links
  tags: Documents,Web, Links
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/web-links-post-openapi.md
- name: Box Get Web Link
  x-api-slug: box
  description: Use to get information about the web link.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//web_links/{WEB_LINK_ID}
  tags: Documents,Web, Links, Web, Link
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/web-linksweb-link-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/web-linksweb-link-id-get-openapi.md
- name: Box Update Web Link
  x-api-slug: box
  description: Updates information for a web link.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//web_links/{WEB_LINK_ID}
  tags: Documents,Web, Links, Web, Link
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/web-linksweb-link-id-put-openapi.md
- name: Box Delete Web Link
  x-api-slug: box
  description: Deletes a web link and moves it to the trash
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//web_links/{WEB_LINK_ID}
  tags: Documents,Web, Links, Web, Link
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/web-linksweb-link-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/web-linksweb-link-id-delete-openapi.md
- name: Box Create Metadata Template
  x-api-slug: box
  description: Used to create a new metadata template with the specified schema.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//metadata_templates/schema
  tags: Documents,Metadata, Templates, Schema
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/metadata-templatesschema-post-openapi.md
- name: Box Get Enterprise Metadata
  x-api-slug: box
  description: Used to retrieve all metadata templates within a user's enterprise.
    Currently only the enterprise scope is supported.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//metadata_templates/{SCOPE}
  tags: Documents,Metadata, Templates, Scope
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/metadata-templatesscope-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/metadata-templatesscope-get-openapi.md
- name: Box Get Metadata Template
  x-api-slug: box
  description: Used to retrieve the schema for a given metadata template.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//metadata_templates/{SCOPE}/{TEMPLATE}/schema
  tags: Documents,Metadata, Templates, Scope, Template, Schema
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/metadata-templatesscopetemplateschema-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/metadata-templatesscopetemplateschema-get-openapi.md
- name: Box Update Metadata Template
  x-api-slug: box
  description: Used to update the schema of an existing template.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//metadata_templates/{SCOPE}/{TEMPLATE}/schema
  tags: Documents,Metadata, Templates, Scope, Template, Schema
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/metadata-templatesscopetemplateschema-put-openapi.md
- name: Box Get all Metadata on File
  x-api-slug: box
  description: Used to retrieve all metadata associated with a given file
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//files/{FILE_ID}/metadata
  tags: Documents,Files, File, , Metadata
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-idmetadata-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-idmetadata-get-openapi.md
- name: Box Create Metadata on File
  x-api-slug: box
  description: Used to create the metadata template instance for a corresponding Box
    file. When creating metadata, only values that adhere to the metadata template
    schema will be accepted.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//files/{FILE_ID}/metadata/{SCOPE}/{TEMPLATE}
  tags: Documents,Files, File, , Metadata, Scope, Template
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-idmetadatascopetemplate-post-openapi.md
- name: Box Get Metadata on File
  x-api-slug: box
  description: Used to retrieve the metadata template instance for a corresponding
    Box file.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//files/{FILE_ID}/metadata/{SCOPE}/{TEMPLATE}
  tags: Documents,Files, File, , Metadata, Scope, Template
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-idmetadatascopetemplate-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-idmetadatascopetemplate-get-openapi.md
- name: Box Update Metadata on File
  x-api-slug: box
  description: |-
    Used to update the template instance. The request body must follow the JSON-Patch specification, which is represented as a JSON array of operation objects (see examples for more details). Updates can be either add, replace, remove , test, move, or copy. The template instance can only be updated if the template instance already exists. When editing metadata, only values that adhere to the metadata template schema will be accepted.
    The update is applied atomically. If any errors occur during the application of the update operations, the metadata instance remains unchanged.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//files/{FILE_ID}/metadata/{SCOPE}/{TEMPLATE}
  tags: Documents,Files, File, , Metadata, Scope, Template
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-idmetadatascopetemplate-put-openapi.md
- name: Box Delete Metadata on File
  x-api-slug: box
  description: Used to delete the template instance. To delete custom key:value pairs
    within a template instance, you should refer to the updating metadata section.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//files/{FILE_ID}/metadata/{SCOPE}/{TEMPLATE}
  tags: Documents,Files, File, , Metadata, Scope, Template
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-idmetadatascopetemplate-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/filesfile-idmetadatascopetemplate-delete-openapi.md
- name: Box Get All Metadata on Folder
  x-api-slug: box
  description: Used to retrieve all metadata associated with a given folder
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//folders/{FOLDER_ID}/metadata
  tags: Documents,Folders, Folder, , Metadata
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/foldersfolder-idmetadata-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/foldersfolder-idmetadata-get-openapi.md
- name: Box Create Metadata on Folder
  x-api-slug: box
  description: Used to create the metadata template instance for a corresponding Box
    folder. When creating metadata, only values that adhere to the metadata template
    schema will be accepted.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//folders/{FOLDER_ID}/metadata/{SCOPE}/{TEMPLATE}
  tags: Documents,Folders, Folder, , Metadata, Scope, Template
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/foldersfolder-idmetadatascopetemplate-post-openapi.md
- name: Box Get Metadata on Folder
  x-api-slug: box
  description: Used to retrieve the metadata template instance for a corresponding
    Box folder.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//folders/{FOLDER_ID}/metadata/{SCOPE}/{TEMPLATE}
  tags: Documents,Folders, Folder, , Metadata, Scope, Template
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/foldersfolder-idmetadatascopetemplate-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/foldersfolder-idmetadatascopetemplate-get-openapi.md
- name: Box Update Metadata on Folder
  x-api-slug: box
  description: Used to update the template instance. Updates can be either add, replace,
    remove , or test. The template instance can only be updated if the template instance
    already exists. When editing metadata, only values that adhere to the metadata
    template schema will be accepted.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//folders/{FOLDER_ID}/metadata/{SCOPE}/{TEMPLATE}
  tags: Documents,Folders, Folder, , Metadata, Scope, Template
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/foldersfolder-idmetadatascopetemplate-put-openapi.md
- name: Box Delete Metadata on Folder
  x-api-slug: box
  description: Used to delete the template instance. To delete custom key:value pairs
    within a template instance, you should refer to the updating metadata section.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//folders/{FOLDER_ID}/metadata/{SCOPE}/{TEMPLATE}
  tags: Documents,Folders, Folder, , Metadata, Scope, Template
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/foldersfolder-idmetadatascopetemplate-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/foldersfolder-idmetadatascopetemplate-delete-openapi.md
- name: Box Pending Collaborations
  x-api-slug: box
  description: Used to retrieve all pending collaboration invites for this user.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//collaborations
  tags: Documents,Collaborations
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/collaborations-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/collaborations-get-openapi.md
- name: Box Create Collaboration
  x-api-slug: box
  description: Used to add a collaboration for a single user or a single group to
    a folder. Either an email address, a user ID, or a group id can be used to create
    the collaboration. If the collaboration is being created with a group, access
    to this endpoint is granted based on the group's invitability_level.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//collaborations
  tags: Documents,Collaborations
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/collaborations-post-openapi.md
- name: Box Get Collaboration
  x-api-slug: box
  description: "Used to get information about a single collaboration. All collaborations
    for a single folder can be retrieved through GET /folders/{id}/collaborations.
    A complete list of the user\u2019s pending collaborations can also be retrieved."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//collaborations/{COLLAB_ID}
  tags: Documents,Collaborations, Collab
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/collaborationscollab-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/collaborationscollab-id-get-openapi.md
- name: Box Update Collaboration
  x-api-slug: box
  description: Used to edit an existing collaboration. Descriptions of the various
    roles can be found here.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//collaborations/{COLLAB_ID}
  tags: Documents,Collaborations, Collab
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/collaborationscollab-id-put-openapi.md
- name: Box Delete Collaboration
  x-api-slug: box
  description: Used to delete a single collaboration.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//collaborations/{COLLAB_ID}
  tags: Documents,Collaborations, Collab
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/collaborationscollab-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/collaborationscollab-id-delete-openapi.md
- name: Box Searching for Content
  x-api-slug: box
  description: The search endpoint provides a powerful way of finding items that are
    accessible by a single user or an entire enterprise. Leverage the parameters listed
    below to generate targeted advanced searches.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//search
  tags: Documents,Search
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/search-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/search-get-openapi.md
- name: Box Shared Items
  x-api-slug: box
  description: "Shared items are any files or folders that are represented by a shared
    link. Shared items are different from other API resources in that a shared resource
    doesn\u2019t necessarily have to be in the account of the user accessing it. The
    actual shared link itself is used along with a normal access token.\nUsed to retrieve
    the metadata about a shared item when only given a shared link. Because of varying
    permission for shared links, a password may be required to retrieve the shared
    item. Once the item has been retrieved, you can make API requests against the
    actual resource /files/{id} or /folders/{id} as long as the shared link and optional
    password are in the header."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//shared_items
  tags: Documents,Shared, Items
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/shared-items-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/shared-items-get-openapi.md
- name: Box Get Collections
  x-api-slug: box
  description: Retrieves the collections for the given user. Currently, only the favorites
    collection is supported.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//collections
  tags: Documents,Collections
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/collections-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/collections-get-openapi.md
- name: Box Get Collection Items
  x-api-slug: box
  description: "Retrieves the files and/or folders contained within this collection.
    Collection item lists behave a lot like getting a folder\u2019s items.\nPaginated
    results can be retrieved using the limit and offset parameters.\nSub-object fields
    can be requested via the ?fields parameter"
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//collections/{COLLECTION_ID}/items
  tags: Documents,Collections, Collection, , Items
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/collectionscollection-iditems-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/collectionscollection-iditems-get-openapi.md
- name: Box Create Comment
  x-api-slug: box
  description: Used to add a comment by the user to a specific file or comment (i.e.
    as a reply comment).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//comments
  tags: Documents,Comments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/comments-post-openapi.md
- name: Box Get Comment
  x-api-slug: box
  description: Used to retrieve the message and metadata about a specific comment.
    Information about the user who created the comment is also included.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//comments/{COMMENT_ID}
  tags: Documents,Comments, Comment
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/commentscomment-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/commentscomment-id-get-openapi.md
- name: Box Update Comment
  x-api-slug: box
  description: Used to update the message of the comment.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//comments/{COMMENT_ID}
  tags: Documents,Comments, Comment
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/commentscomment-id-put-openapi.md
- name: Box Delete Comment
  x-api-slug: box
  description: Permanently deletes a comment.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//comments/{COMMENT_ID}
  tags: Documents,Comments, Comment
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/commentscomment-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/commentscomment-id-delete-openapi.md
- name: Box Create Task
  x-api-slug: box
  description: Used to create a single task for single user on a single file.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//tasks
  tags: Documents,Tasks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/tasks-post-openapi.md
- name: Box Get Task
  x-api-slug: box
  description: Fetches a specific task.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//tasks/{TASK_ID}
  tags: Documents,Tasks, Task
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/taskstask-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/taskstask-id-get-openapi.md
- name: Box Update Task
  x-api-slug: box
  description: Updates a specific task.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//tasks/{TASK_ID}
  tags: Documents,Tasks, Task
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/taskstask-id-put-openapi.md
- name: Box Delete Task
  x-api-slug: box
  description: Permanently deletes a specific task.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//tasks/{TASK_ID}
  tags: Documents,Tasks, Task
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/taskstask-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/taskstask-id-delete-openapi.md
- name: Box Get Assignments
  x-api-slug: box
  description: Retrieves all of the assignments for a given task.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//tasks/{TASK_ID}/assignments
  tags: Documents,Tasks, Task, , Assignments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/taskstask-idassignments-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/taskstask-idassignments-get-openapi.md
- name: Box Create Task Assignment
  x-api-slug: box
  description: Used to assign a task to a single user. There can be multiple assignments
    on a given task.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//task_assignments
  tags: Documents,Task, Assignments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/task-assignments-post-openapi.md
- name: Box Get Task Assignment
  x-api-slug: box
  description: Fetches a specific task assignment.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//task_assignments/{TASK_ASSIGNMENT_ID}
  tags: Documents,Task, Assignments, Task, Assignment
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/task-assignmentstask-assignment-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/task-assignmentstask-assignment-id-get-openapi.md
- name: Box Update Task Assignment
  x-api-slug: box
  description: Used to update a task assignment.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//task_assignments/{TASK_ASSIGNMENT_ID}
  tags: Documents,Task, Assignments, Task, Assignment
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/task-assignmentstask-assignment-id-put-openapi.md
- name: Box Delete Task Assignment
  x-api-slug: box
  description: Deletes a specific task assignment.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//task_assignments/{TASK_ASSIGNMENT_ID}
  tags: Documents,Task, Assignments, Task, Assignment
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/task-assignmentstask-assignment-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/task-assignmentstask-assignment-id-delete-openapi.md
- name: Box User Events, Enterprise Events
  x-api-slug: box
  description: |-
    Use this to get events for a given user. A chunk of event objects is returned for the user based on the parameters passed in. Parameters indicating how many chunks are left as well as the next stream_position are also returned.

    To retrieve Enterprise Events specify 'stream_type=admin_logs'. Retrieves up to a year' events for all users in an enterprise. Upper and lower bounds as well as filters can be applied to the results.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//events
  tags: Documents,Events
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/events-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/events-get-openapi.md
- name: Box Long polling
  x-api-slug: box
  description: "To get real-time notification of activity in a Box account, use the
    long poll feature of the /events API. To do so, first call the /events API with
    an OPTIONS call to retrieve the long poll URL to use. Next, make a GET request
    to the provided URL to begin listening for events. If an event occurs within an
    account you are monitoring, you will receive a response with the value new_change.
    It\u2019s important to note that this response will not come with any other details,
    but should serve as a prompt to take further action such as calling the /events
    endpoint with your last known stream_position. After sending this response, the
    server will close the connection and you will need to repeat the long poll process
    to begin listening for events again.\nIf no events occur for a period of time
    after you make the GET request to the long poll URL, you will receive a response
    with the value reconnect. When you receive this response, you\u2019ll make another
    OPTIONS call to the /events endpoint and repeat the long poll process.\nIf you
    receive no events in retry_timeout seconds, you should make another GET request
    to the real time server (i.e. URL in the response). This might be necessary in
    case you do not receive the reconnect message in the face of network errors.\nIf
    you receive max_retries error when making GET requests to the real time server,
    you should make another OPTIONS request."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//events
  tags: Documents,Events
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/events-options-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/events-options-openapi.md
- name: Box Create User
  x-api-slug: box
  description: Used to provision a new user in an enterprise. This method only works
    for enterprise admins.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//users
  tags: Documents,Users
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/users-post-openapi.md
- name: Box Get Enterprise Users
  x-api-slug: box
  description: Returns a list of all users for the Enterprise along with their user_id,
    public_name, and login.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//users
  tags: Documents,Users
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/users-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/users-get-openapi.md
- name: Box Get Current User
  x-api-slug: box
  description: Retrieves information about the user who is currently logged in i.e.
    the user for whom this auth token was generated.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//users/me
  tags: Documents,Users, Me
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/usersme-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/usersme-get-openapi.md
- name: Box Get User's Info
  x-api-slug: box
  description: Retrieves information about a user in the enterprise. Requires enterprise
    administration authorization.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//users/{USER_ID}
  tags: Documents,Users, User
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/usersuser-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/usersuser-id-get-openapi.md
- name: Box Update User, Change User's Login
  x-api-slug: box
  description: "Used to edit the settings and information about a user. This method
    only works for enterprise admins. To roll a user out of the enterprise (and convert
    them to a standalone free user), update the special enterprise attribute to be
    null.\n\nUsed to convert one of the user\u2019s confirmed email aliases into the
    user\u2019s primary login."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//users/{USER_ID}
  tags: Documents,Users, User
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/usersuser-id-put-openapi.md
- name: Box Delete User
  x-api-slug: box
  description: Deletes a user in an enterprise account.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//users/{USER_ID}
  tags: Documents,Users, User
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/usersuser-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/usersuser-id-delete-openapi.md
- name: Box Move User's Folder
  x-api-slug: box
  description: "Moves all of the owned content from within one user\u2019s folder
    into a new folder in another user\u2019s account. You can move folders across
    users as long as the you have administrative permissions and the \u2018source\u2019
    user owns the folders. To move everything from the root folder, use \u201C0\u201D
    which always represents the root folder of a Box account."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//users/{USER_ID}/folders/{FOLDER_ID}
  tags: Documents,Users, User, , Folders, Folder
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/usersuser-idfoldersfolder-id-put-openapi.md
- name: Box Get Email Aliases
  x-api-slug: box
  description: Retrieves all email aliases for this user. The collection of email
    aliases does not include the primary login for the user; use GET /users/USER_ID
    to retrieve the login email address.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//users/{USER_ID}/email_aliases
  tags: Documents,Users, User, , Email, Aliases
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/usersuser-idemail-aliases-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/usersuser-idemail-aliases-get-openapi.md
- name: Box Add Email Alias
  x-api-slug: box
  description: "Adds a new email alias to the given user\u2019s account."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//users/{USER_ID}/email_aliases
  tags: Documents,Users, User, , Email, Aliases
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/usersuser-idemail-aliases-post-openapi.md
- name: Box Delete Email Alias
  x-api-slug: box
  description: Removes an email alias from a user.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//users/{USER_ID}/email_aliases/{EMAIL_ALIAS_ID}
  tags: Documents,Users, User, , Email, Aliases, Email, Alias
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/usersuser-idemail-aliasesemail-alias-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/usersuser-idemail-aliasesemail-alias-id-delete-openapi.md
- name: Box Invite User
  x-api-slug: box
  description: Invites an existing user to join an Enterprise. The existing user can
    not be part of another Enterprise and must already have a Box account. Once invited,
    the user will receive an email and prompt to accept the invitation within the
    Box web application. This method requires the "Manage An Enterprise" scope for
    the enterprise, which can be enabled within your developer console.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//invites
  tags: Documents,Invites
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/invites-post-openapi.md
- name: Box Get status of the invite
  x-api-slug: box
  description: ""
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//invites/{INVITE_ID}
  tags: Documents,Invites, Invite
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/invitesinvite-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/invitesinvite-id-get-openapi.md
- name: Box Create Group
  x-api-slug: box
  description: Used to create a group.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//groups
  tags: Documents,Groups
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/groups-post-openapi.md
- name: Box Get Groups for an Enterprise
  x-api-slug: box
  description: Retrieves all of the groups for given enterprise. Must have permissions
    to see an enterprise's groups.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//groups
  tags: Documents,Groups
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/groups-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/groups-get-openapi.md
- name: Box Get Group
  x-api-slug: box
  description: Used to get information about a group.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//groups/{GROUP_ID}
  tags: Documents,Groups, Group
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/groupsgroup-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/groupsgroup-id-get-openapi.md
- name: Box Update Group
  x-api-slug: box
  description: Updates a specific group.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//groups/{GROUP_ID}
  tags: Documents,Groups, Group
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/groupsgroup-id-put-openapi.md
- name: Box Delete Group
  x-api-slug: box
  description: Permanently deletes a specific group.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//groups/{GROUP_ID}
  tags: Documents,Groups, Group
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/groupsgroup-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/groupsgroup-id-delete-openapi.md
- name: Box Create Membership
  x-api-slug: box
  description: Used to add a member to a Group.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//group_memberships
  tags: Documents,Group, Memberships
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/group-memberships-post-openapi.md
- name: Box Get Membership
  x-api-slug: box
  description: Fetches a specific group membership entry.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//group_memberships/{GROUP_MEMBERSHIP_ID}
  tags: Documents,Group, Memberships, Group, Membership
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/group-membershipsgroup-membership-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/group-membershipsgroup-membership-id-get-openapi.md
- name: Box Update Membership
  x-api-slug: box
  description: Used to update a group membership.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//group_memberships/{GROUP_MEMBERSHIP_ID}
  tags: Documents,Group, Memberships, Group, Membership
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/group-membershipsgroup-membership-id-put-openapi.md
- name: Box Delete Membership
  x-api-slug: box
  description: Deletes a specific group membership.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//group_memberships/{GROUP_MEMBERSHIP_ID}
  tags: Documents,Group, Memberships, Group, Membership
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/group-membershipsgroup-membership-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/group-membershipsgroup-membership-id-delete-openapi.md
- name: Box Get Memberships for Group
  x-api-slug: box
  description: Retrieves all of the members for a given group if the requesting user
    has access (see Group Object member_viewability_level).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//groups/{GROUP_ID}/memberships
  tags: Documents,Groups, Group, , Memberships
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/groupsgroup-idmemberships-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/groupsgroup-idmemberships-get-openapi.md
- name: Box Get Memberships for User
  x-api-slug: box
  description: Retrieves all of the group memberships for a given user. Note this
    is only available to group admins. To retrieve group memberships for the user
    making the API request, use the users/me/memberships endpoint.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//users/{USER_ID}/memberships
  tags: Documents,Users, User, , Memberships
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/usersuser-idmemberships-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/usersuser-idmemberships-get-openapi.md
- name: Box Get Collaborations for Group
  x-api-slug: box
  description: Retrieves all of the group collaborations for a given group. Note this
    is only available to group admins.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//groups/{GROUP_ID}/collaborations
  tags: Documents,Groups, Group, , Collaborations
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/groupsgroup-idcollaborations-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/groupsgroup-idcollaborations-get-openapi.md
- name: Box Get Enterprise Device Pins
  x-api-slug: box
  description: Gets all the device pins within a given enterprise. Must be an enterprise
    admin with the manage enterprise scope to make this call.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//enterprises/{ENTERPRISE_ID}/device_pinners
  tags: Documents,Enterprises, Enterprise, , Device, Pinners
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/enterprisesenterprise-iddevice-pinners-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/enterprisesenterprise-iddevice-pinners-get-openapi.md
- name: Box Get Device Pin
  x-api-slug: box
  description: Gets information about an individual device pin.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//device_pinners/{ID}
  tags: Documents,Device, Pinners
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/device-pinnersid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/device-pinnersid-get-openapi.md
- name: Box Delete Device Pin
  x-api-slug: box
  description: Delete individual device pin.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//device_pinners/{ID}
  tags: Documents,Device, Pinners
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/device-pinnersid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/device-pinnersid-delete-openapi.md
- name: Box Create Retention Policy
  x-api-slug: box
  description: Used to create a new retention policy.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//retention_policies
  tags: Documents,Retention, Policies
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/retention-policies-post-openapi.md
- name: Box Get Retention Policies
  x-api-slug: box
  description: Retrieves all of the retention policies for the given enterprise.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//retention_policies
  tags: Documents,Retention, Policies
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/retention-policies-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/retention-policies-get-openapi.md
- name: Box Get Retention Policy
  x-api-slug: box
  description: Used to retrieve information about a retention policy
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//retention_policies/{POLICY_ID}
  tags: Documents,Retention, Policies, Policy
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/retention-policiespolicy-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/retention-policiespolicy-id-get-openapi.md
- name: Box Update Retention Policy
  x-api-slug: box
  description: Used to update a retention policy.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//retention_policies/{POLICY_ID}
  tags: Documents,Retention, Policies, Policy
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/retention-policiespolicy-id-put-openapi.md
- name: Box Get Retention Policy Assignments
  x-api-slug: box
  description: Returns a list of all retention policy assignments associated with
    a specified retention policy.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//retention_policies/{POLICY_ID}/assignments
  tags: Documents,Retention, Policies, Policy, , Assignments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/retention-policiespolicy-idassignments-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/retention-policiespolicy-idassignments-get-openapi.md
- name: Box Create Retention Policy Assignment
  x-api-slug: box
  description: Returns a list of all retention policy assignments associated with
    a specified retention policy.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//retention_policy_assignments
  tags: Documents,Retention, Policy, Assignments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/retention-policy-assignments-post-openapi.md
- name: Box Get Retention Policy Assignment
  x-api-slug: box
  description: Used to retrieve information about a retention policy assignment.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//retention_policy_assignments/{RETENTION_POLICY_ASSIGNMENT_ID}
  tags: Documents,Retention, Policy, Assignments, Retention, Policy, Assignment
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/retention-policy-assignmentsretention-policy-assignment-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/retention-policy-assignmentsretention-policy-assignment-id-get-openapi.md
- name: Box Get File Version Retentions
  x-api-slug: box
  description: Retrieves all file version retentions for the given enterprise.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//file_version_retentions
  tags: Documents,File, Version, Retentions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/file-version-retentions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/file-version-retentions-get-openapi.md
- name: Box Get File Version Retention
  x-api-slug: box
  description: Used to retrieve information about a file version retention
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//file_version_retentions/{FILE_VERSION_RETENTION_ID}
  tags: Documents,File, Version, Retentions, File, Version, Retention
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/file-version-retentionsfile-version-retention-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/file-version-retentionsfile-version-retention-id-get-openapi.md
- name: Box Create New Legal Hold Policy
  x-api-slug: box
  description: Create a new Legal Hold Policy. Optional date filter may be passed.
    If Policy has a date filter, any Custodian assignments will apply only to file
    versions created or uploaded inside of the date range.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//legal_hold_policies
  tags: Documents,Legal, Hold, Policies
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/legal-hold-policies-post-openapi.md
- name: Box Get Legal Hold Policies
  x-api-slug: box
  description: Get a list of Legal Hold Policies that belong to your Enterprise.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//legal_hold_policies
  tags: Documents,Legal, Hold, Policies
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/legal-hold-policies-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/legal-hold-policies-get-openapi.md
- name: Box Update Existing Legal Hold Policy
  x-api-slug: box
  description: Update existing Legal Hold Policy. Only name and description can be
    modified.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//legal_hold_policies/{ID}
  tags: Documents,Legal, Hold, Policies
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/legal-hold-policiesid-put-openapi.md
- name: Box Get Legal Hold Policy
  x-api-slug: box
  description: Get details of a single Legal Hold Policy
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//legal_hold_policies/{ID}
  tags: Documents,Legal, Hold, Policies
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/legal-hold-policiesid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/legal-hold-policiesid-get-openapi.md
- name: Box Delete Legal Hold Policy
  x-api-slug: box
  description: Sends request to delete an existing Legal Hold Policy. Note that this
    is an asynchronous process - the Policy will not be fully deleted yet when the
    response comes back.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//legal_hold_policies/{ID}
  tags: Documents,Legal, Hold, Policies
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/legal-hold-policiesid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/legal-hold-policiesid-delete-openapi.md
- name: Box Get Legal hold policy assignments
  x-api-slug: box
  description: Get list of assignments for a single Policy.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//legal_hold_policies/{ID}/assignments
  tags: Documents,Legal, Hold, Policies, , Assignments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/legal-hold-policiesidassignments-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/legal-hold-policiesidassignments-get-openapi.md
- name: Box Create New Legal Hold Policy Assignment
  x-api-slug: box
  description: Create a new Assignment, which will apply the Legal Hold Policy to
    the target of the Assignment.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//legal_hold_policy_assignments
  tags: Documents,Legal, Hold, Policy, Assignments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/legal-hold-policy-assignments-post-openapi.md
- name: Box Get Legal Hold Policy Assignment
  x-api-slug: box
  description: Get details of a single assignment.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//legal_hold_policy_assignments/{ASSIGNMENT_ID}
  tags: Documents,Legal, Hold, Policy, Assignments, Assignment
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/legal-hold-policy-assignmentsassignment-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/legal-hold-policy-assignmentsassignment-id-get-openapi.md
- name: Box Delete Legal Hold Policy Assignment
  x-api-slug: box
  description: Sends request to delete an existing Assignment. Note that this is an
    asynchronous process - the Assignment will not be fully deleted yet when the response
    comes back.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//legal_hold_policy_assignments/{ASSIGNMENT_ID}
  tags: Documents,Legal, Hold, Policy, Assignments, Assignment
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/legal-hold-policy-assignmentsassignment-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/legal-hold-policy-assignmentsassignment-id-delete-openapi.md
- name: Box Get List of File Version Legal Holds
  x-api-slug: box
  description: Get list of non-deleted Holds for a single Policy.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//file_version_legal_holds
  tags: Documents,File, Version, Legal, Holds
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/file-version-legal-holds-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/file-version-legal-holds-get-openapi.md
- name: Box Get File Version Legal Hold
  x-api-slug: box
  description: Get details of a single File Version Legal Hold.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//file_version_legal_holds/{ID}
  tags: Documents,File, Version, Legal, Holds
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/file-version-legal-holdsid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/file-version-legal-holdsid-get-openapi.md
- name: Box Create Webhook
  x-api-slug: box
  description: Create Webhook
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//webhooks
  tags: Documents,Webhooks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/webhooks-post-openapi.md
- name: Box Get Webhooks
  x-api-slug: box
  description: |-
    Returns all defined webhooks for the requesting application and user, up to the limit. If no limit is supplied then Box uses the default limit of 100.
    If more than limit webhooks are defined then Box returns the webhooks in batches. When the results are batched, Box sends limit webhooks along with a next_marker field in the response object. The value of the next_marker field is a marker string that you can use in later requests to tell Box which batch to send next.
    When you send a request that includes a marker string, Box sends the next batch of webhooks, beginning after the last webhook of the previous batch. When the response contains the last of the defined webhooks, Box omits the next_marker field from its response.
    You can use limit and marker together with the marker string returned in the next_marker field to paginate lists of webhooks.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//webhooks
  tags: Documents,Webhooks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/webhooks-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/webhooks-get-openapi.md
- name: Box Get Webhook
  x-api-slug: box
  description: Get a Webhook
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//webhooks/{WEBHOOK_ID}
  tags: Documents,Webhooks, Webhook
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/webhookswebhook-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/webhookswebhook-id-get-openapi.md
- name: Box Update Webhook
  x-api-slug: box
  description: Update a Webhook
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//webhooks/{WEBHOOK_ID}
  tags: Documents,Webhooks, Webhook
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/webhookswebhook-id-put-openapi.md
- name: Box Delete Webhook
  x-api-slug: box
  description: Permanently deletes a webhook
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0//webhooks/{WEBHOOK_ID}
  tags: Documents,Webhooks, Webhook
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/webhookswebhook-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/webhookswebhook-id-delete-openapi.md
- name: Box
  x-api-slug: box
  description: Box.net provides a sophisticated API for their online document sharing
    and collaboration web application.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/box1200x630.jpg
  humanURL: http://box.com
  baseURL: https://api.box.com//2.0
  tags: Box
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/box/master/_listings/box/openapi.md
x-common:
- type: x-base
  url: https://api.box.com/
- type: x-blog
  url: http://blog.box.com/
- type: x-blog-rss
  url: http://blog.box.com/feed/
- type: x-crunchbase
  url: http://www.crunchbase.com/company/box
- type: x-developer
  url: http://developers.box.com
- type: x-github
  url: https://github.com/boxdotnet
- type: x-pricing
  url: https://developers.box.com/box-platform-pricing/
- type: x-road-map
  url: https://developers.box.com/roadmap/
- type: x-twitter
  url: https://twitter.com/BoxPlatform
- type: x-website
  url: http://box.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---