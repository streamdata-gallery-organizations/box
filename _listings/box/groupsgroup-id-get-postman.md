{
  "info": {
    "name": "Box Get Group",
    "_postman_id": "73c4267d-6e29-4396-b87b-3a6b4d5c103c",
    "description": "Used to get information about a group.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "7aa4daa3-0ccc-43c4-bd28-9eff06e232c8",
          "name": "getGroup",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "groups/:GROUP_ID"
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
                  "id": "GROUP_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Used to get information about a group"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "31e553e3-8ac2-4d46-aefa-1ecf01e948f7"
            }
          ]
        }
      ]
    }
  ]
}