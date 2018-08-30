{
  "info": {
    "name": "Box Get File's Comments",
    "_postman_id": "ddb8ba26-2ebc-4bd8-85c3-d78355cb5d4e",
    "description": "Retrieves the comments on a particular file, if any exist.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "bca2ca84-4a1b-4142-a5ee-68d1eb34ea9a",
          "name": "getFileComments",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "files/:FILE_ID/comments"
              ],
              "query": [
                {
                  "key": "fields",
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
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves the comments on a particular file, if any exist"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8ba60e85-f1d4-4f46-8a8d-2931771b829c"
            }
          ]
        }
      ]
    }
  ]
}