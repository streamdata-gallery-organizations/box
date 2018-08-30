{
  "info": {
    "name": "Box Get All Metadata on Folder",
    "_postman_id": "468c8785-0b0f-45b3-8e3d-929189a23a74",
    "description": "Used to retrieve all metadata associated with a given folder",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "c5cb41d5-a1aa-4131-9ed0-a800ff0602ca",
          "name": "getAllFolderMetadata",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "folders/:FOLDER_ID/metadata"
              ],
              "variable": [
                {
                  "id": "FOLDER_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Used to retrieve all metadata associated with a given folder"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4a2ab24c-2bea-47fd-bfe6-1fb108e372d0"
            }
          ]
        }
      ]
    }
  ]
}