{
  "info": {
    "name": "Box Download File",
    "_postman_id": "5c16ba2c-8f68-4e2f-89ac-c990486404b9",
    "description": "Retrieves the actual data of the file. An optional version parameter can be set to download a previous version of the file.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "eb595113-2653-4d13-b5a0-cc0104aa5b7f",
          "name": "getFileContent",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "files/:FILE_ID/content"
              ],
              "query": [
                {
                  "key": "version",
                  "value": "%7B%7D",
                  "disabled": false
                }
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
            "header": [
              {
                "key": "BoxApi",
                "value": "{}",
                "description": "The shared link for this item",
                "disabled": false
              },
              {
                "key": "Range",
                "value": "{}",
                "description": "The range value in bytes",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves the actual data of the file"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b4047c1e-587c-490f-949a-5c9164bb7caa"
            }
          ]
        }
      ]
    }
  ]
}