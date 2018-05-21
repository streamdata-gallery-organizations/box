{
  "info": {
    "name": "Box Get Retention Policies",
    "_postman_id": "b1152522-9daa-40cb-8dba-2fabf060f828",
    "description": "Retrieves all of the retention policies for the given enterprise.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "d5a5e24f-9c9f-4c61-ad1b-929042db2b00",
          "name": "getRetentionPolicies",
          "request": {
            "url": "http://api.box.com/2.0/retention_policies?created_by_user_id=%7B%7D&policy_name=%7B%7D&policy_type=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves all of the retention policies for the given enterprise"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "55453d79-6e45-4ecb-88f8-49a64d52f118"
            }
          ]
        }
      ]
    }
  ]
}