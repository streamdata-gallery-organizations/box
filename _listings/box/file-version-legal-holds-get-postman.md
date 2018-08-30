{
  "info": {
    "name": "Box Get List of File Version Legal Holds",
    "_postman_id": "bc0cf97a-c6b4-40e7-b7f9-7d0b56e9ac4d",
    "description": "Get list of non-deleted Holds for a single Policy.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "46e2c09d-19af-4d01-a065-b0fc1e822dff",
          "name": "getFileVersionLegalHoldPolicies",
          "request": {
            "url": "http://api.box.com/2.0/file_version_legal_holds?policy_id=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get list of non-deleted Holds for a single Policy"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9c1f31b0-60f6-447a-9d66-b8269d1a6fc6"
            }
          ]
        }
      ]
    }
  ]
}