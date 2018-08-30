{
  "info": {
    "name": "Box View Versions",
    "_postman_id": "34d4c754-6164-4895-9aa6-cb1ed71b6012",
    "description": "If there are previous versions of this file, this method can be used to retrieve information about the older versions. (Versions are only tracked for Box users with premium accounts.)",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "062d6377-6c63-4b08-b83d-7f25ce326c4b",
          "name": "getFileVersions",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "files/:FILE_ID/versions"
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
            "description": "If there are previous versions of this file, this method can be used to retrieve information about the older versions"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1741a3d0-96f9-4837-b2c5-f1c35f30a72c"
            }
          ]
        }
      ]
    }
  ]
}