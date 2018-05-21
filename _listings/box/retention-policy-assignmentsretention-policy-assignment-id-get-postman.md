{
  "info": {
    "name": "Box Get Retention Policy Assignment",
    "_postman_id": "fc832deb-2700-45f9-8a4d-397d270c235c",
    "description": "Used to retrieve information about a retention policy assignment.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "47bac479-a664-48d8-b9c4-d103ca7697b7",
          "name": "getRetentionPolicyAssignment",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "retention_policy_assignments/:RETENTION_POLICY_ASSIGNMENT_ID"
              ],
              "variable": [
                {
                  "id": "RETENTION_POLICY_ASSIGNMENT_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Used to retrieve information about a retention policy assignment"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ea4bed5b-bf01-4f05-87c6-445b5f0618b4"
            }
          ]
        }
      ]
    }
  ]
}