{
  "info": {
    "name": "Box Get Legal Hold Policies",
    "_postman_id": "fd24f1b0-36f1-445b-9b61-5a3233a27114",
    "description": "Get a list of Legal Hold Policies that belong to your Enterprise.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "f79b3183-9f69-4dc3-861c-a5015c054987",
          "name": "getLegalHoldPolicies",
          "request": {
            "url": "http://api.box.com/2.0/legal_hold_policies?limit=%7B%7D&marker=%7B%7D&policy_name=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get a list of Legal Hold Policies that belong to your Enterprise"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3fa54a1a-d950-450e-96b4-9625287f025f"
            }
          ]
        }
      ]
    }
  ]
}