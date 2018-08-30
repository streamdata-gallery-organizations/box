{
  "info": {
    "name": "Box Get status of the invite",
    "_postman_id": "a8f90108-b3a8-4afe-89a4-ee8d067cb725",
    "description": "",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "d0c8ab5a-0ceb-4295-a218-47fb40e7726b",
          "name": "getInvite",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "invites/:INVITE_ID"
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
                  "id": "INVITE_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get status of the invite"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7ea2b404-b23f-4c18-95d2-dae1f06648fc"
            }
          ]
        }
      ]
    }
  ]
}