{
  "info": {
    "name": "Box Get File's Info, Get Embed Link",
    "_postman_id": "b5905966-9a04-496b-81a7-051c3c63f44c",
    "description": "Used to retrieve the metadata about a file.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "2a2b98c9-48ab-4e67-8a4f-6c87e0c90697",
          "name": "getFile",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "files/:FILE_ID"
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
            "description": "Used to retrieve the metadata about a file"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ca39040d-df1e-44d1-8b67-de26da6261eb"
            }
          ]
        }
      ]
    }
  ]
}