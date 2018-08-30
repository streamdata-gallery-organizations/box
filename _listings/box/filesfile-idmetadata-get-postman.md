{
  "info": {
    "name": "Box Get all Metadata on File",
    "_postman_id": "73bdb86f-a033-42dc-ae05-529d5d6265c7",
    "description": "Used to retrieve all metadata associated with a given file",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "15ab8446-99c5-43a6-a035-36898194b8a2",
          "name": "getAllFileMetadata",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "files/:FILE_ID/metadata"
              ],
              "variable": [
                {
                  "id": "FILE_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Used to retrieve all metadata associated with a given file"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "918191d0-9901-4677-a353-ad1de5d0e684"
            }
          ]
        }
      ]
    }
  ]
}