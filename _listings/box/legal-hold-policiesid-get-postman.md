{
  "info": {
    "name": "Box Get Legal Hold Policy",
    "_postman_id": "524e8134-d39d-4fc9-8eef-aa0976802de6",
    "description": "Get details of a single Legal Hold Policy",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "ad014397-06ab-44e2-bdd8-ecb4d05a8aca",
          "name": "getLegalHoldPolicy",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "legal_hold_policies/:ID"
              ],
              "variable": [
                {
                  "id": "ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get details of a single Legal Hold Policy"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6c65bd07-959b-48a2-9956-6a94f8161e30"
            }
          ]
        }
      ]
    }
  ]
}