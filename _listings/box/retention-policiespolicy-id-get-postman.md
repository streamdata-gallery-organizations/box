{
  "info": {
    "name": "Box Get Retention Policy",
    "_postman_id": "63130e28-287f-482f-b7db-51e6471868bc",
    "description": "Used to retrieve information about a retention policy",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "a8773d87-af38-42df-97a8-78e8c229c68c",
          "name": "getRetentionPolicy",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "retention_policies/:POLICY_ID"
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
            "description": "Used to retrieve information about a retention policy"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "32c3b5d4-b070-4522-bce5-585aca855b55"
            }
          ]
        }
      ]
    }
  ]
}