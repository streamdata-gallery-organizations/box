{
  "info": {
    "name": "Box Get Legal hold policy assignments",
    "_postman_id": "494b0612-ca2c-4c2f-871f-d761d9d88e46",
    "description": "Get list of assignments for a single Policy.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "a70929f9-c7ea-4fc1-983a-817ea20e71a4",
          "name": "getLegalHoldPolicyAssignments",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "legal_hold_policies/:ID/assignments"
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
            "description": "Get list of assignments for a single Policy"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c83b5e3a-24cd-41d5-b847-bdf99d701d0f"
            }
          ]
        }
      ]
    }
  ]
}