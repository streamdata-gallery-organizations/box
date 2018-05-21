{
  "info": {
    "name": "Box Delete Folder",
    "_postman_id": "6138eee3-0540-42df-b919-5397cac0cbfc",
    "description": "Used to delete a folder. A recursive parameter must be included in order to delete folders that have items inside of them. An optional If-Match header can be included to ensure that client only deletes the folder if it knows about the latest version.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "0d44cc97-1cd1-49b5-8239-46221e9b33c6",
          "name": "deleteFolder",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "folders/:FOLDER_ID"
              ],
              "query": [
                {
                  "key": "recursive",
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
            "method": "DELETE",
            "header": [
              {
                "key": "If-Match",
                "value": "{}",
                "description": "This is in the ‘etag’ field of the folder object",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Used to delete a folder"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6cf8f7f8-36c6-4874-a6ec-b8857ca46c0b"
            }
          ]
        }
      ]
    }
  ]
}