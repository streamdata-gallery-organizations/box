{
  "info": {
    "name": "Box Get Collection Items",
    "_postman_id": "bb6bfa8e-8c4c-4b8a-9e9f-0b5ce0ec6008",
    "description": "Retrieves the files and/or folders contained within this collection. Collection item lists behave a lot like getting a folder???s items.\nPaginated results can be retrieved using the limit and offset parameters.\nSub-object fields can be requested via the ?fields parameter",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "ebce7586-2361-4a6e-a448-72cc3a5ed98f",
          "name": "getCollectionItems",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "collections/:COLLECTION_ID/items"
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
                  "id": "COLLECTION_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves the files and/or folders contained within this collection"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "650f194d-7cef-44fa-9f30-62661e2ade77"
            }
          ]
        }
      ]
    }
  ]
}