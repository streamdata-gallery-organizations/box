{
  "info": {
    "name": "Box Get File's Collaborations",
    "_postman_id": "fd9781cf-2344-4a0a-bc98-24cabc51839d",
    "description": "Use this to get a list of all the collaborations on a file",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "ee617517-6cd9-40e9-b726-3db221478d96",
          "name": "getFileCollaborations",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "files/:FILE_ID/collaborations"
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
            "description": "Use this to get a list of all the collaborations on a file"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "988fe7d5-25ce-40b1-835a-fb2b0fc548bb"
            }
          ]
        }
      ]
    }
  ]
}