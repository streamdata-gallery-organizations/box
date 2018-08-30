{
  "info": {
    "name": "Box Get Retention Policy Assignments",
    "_postman_id": "7b51cf3e-6398-43b1-9476-f3dd87162c28",
    "description": "Returns a list of all retention policy assignments associated with a specified retention policy.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "f516802a-dc21-494f-9e31-c0fe029aea61",
          "name": "getRetentionPolicyAssignments",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "retention_policies/:POLICY_ID/assignments"
              ],
              "query": [
                {
                  "key": "type",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "POLICY_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of all retention policy assignments associated with a specified retention policy"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "052ff6d8-7e0b-4d86-8c03-0ebb8b61ea89"
            }
          ]
        }
      ]
    }
  ]
}