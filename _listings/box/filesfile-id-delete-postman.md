{
  "info": {
    "name": "Box Delete File",
    "_postman_id": "fa2cf9be-7e13-4536-bc6c-e6e9505ac5ae",
    "description": "Discards a file to the trash. The etag of the file can be included as an ‘If-Match’ header to prevent race conditions.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "6219a764-bf68-4686-b394-b71732bc0ecb",
          "name": "deleteFile",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "files/:FILE_ID"
              ],
              "variable": [
                {
                  "id": "FILE_ID",
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
                "description": "The etag of the file",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Discards a file to the trash"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "21898abe-4c42-4d2b-bee4-fe870a22cc48"
            }
          ]
        }
      ]
    }
  ]
}