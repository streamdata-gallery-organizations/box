{
  "info": {
    "name": "Box Get User's Info",
    "_postman_id": "51a95665-9861-4ac0-afc5-a7f82314386e",
    "description": "Retrieves information about a user in the enterprise. Requires enterprise administration authorization.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "296f425a-8ae7-4ac2-9a1f-8482de53b897",
          "name": "getUser",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "users/:USER_ID"
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
                  "id": "USER_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves information about a user in the enterprise"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "07b5ca2e-0c33-412d-b9da-95e4e9a04409"
            }
          ]
        }
      ]
    }
  ]
}