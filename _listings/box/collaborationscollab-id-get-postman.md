{
  "info": {
    "name": "Box Get Collaboration",
    "_postman_id": "2ecdddc1-c5b7-4e80-b011-2983e518f8d0",
    "description": "Used to get information about a single collaboration. All collaborations for a single folder can be retrieved through GET /folders/{id}/collaborations. A complete list of the user???s pending collaborations can also be retrieved.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "0d3a528b-bdfb-4026-9f04-418dabb11ba1",
          "name": "getCollaboration",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "collaborations/:COLLAB_ID"
              ],
              "query": [
                {
                  "key": "fields",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "status",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "COLLAB_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Used to get information about a single collaboration"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "de27206a-7cb0-4edc-9030-2eb76e4b7a1d"
            }
          ]
        }
      ]
    }
  ]
}