{
  "info": {
    "name": "Box Get Legal Hold Policy Assignment",
    "_postman_id": "3e4423ec-4c23-48d5-98bc-e3a5363ad5a2",
    "description": "Get details of a single assignment.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "b2112b6a-290f-467b-83b0-c459b72f69ce",
          "name": "getLegalHoldPolicyAssignment",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "legal_hold_policy_assignments/:ASSIGNMENT_ID"
              ],
              "variable": [
                {
                  "id": "ASSIGNMENT_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get details of a single assignment"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "82390469-7aa2-491d-95d1-482d9226b09c"
            }
          ]
        }
      ]
    }
  ]
}