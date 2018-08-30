{
  "info": {
    "name": "Box Get Folder???s Items",
    "_postman_id": "7aa4ceb9-af32-4b7c-8527-b8a19bda09d4",
    "description": "Retrieves the files and/or folders contained within this folder without any other metadata about the folder. Any attribute in the full files or folders objects can be passed in with the fields parameter to get specific attributes, and only those specific attributes back; otherwise, the mini format is returned for each item by default. Multiple attributes can be passed in separated by commas e.g. fields=name,created_at. Paginated results can be retrieved using the limit and offset parameters.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "dff7cd3c-e71b-466f-b70d-eaa73717b8f2",
          "name": "getFolderItems",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "folders/:FOLDER_ID/items"
              ],
              "query": [
                {
                  "key": "fields",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "offset",
                  "value": "%7B%7D",
                  "disabled": false
                }
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
            "description": "Retrieves the files and/or folders contained within this folder without any other metadata about the folder"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "22c24a7e-1f13-4211-91e2-cb5534491254"
            }
          ]
        }
      ]
    }
  ]
}