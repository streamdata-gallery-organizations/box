{
  "info": {
    "name": "Box Delete Legal Hold Policy Assignment",
    "_postman_id": "9ffbcb7d-6afc-4709-9194-40ffad1b61ba",
    "description": "Sends request to delete an existing Assignment. Note that this is an asynchronous process - the Assignment will not be fully deleted yet when the response comes back.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "2d6abbfb-95be-418a-908b-3744ab1566e6",
          "name": "deleteLegalHoldPolicyAssignment",
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
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Sends request to delete an existing Assignment"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e10612fa-e6a0-4b5f-b777-8c04e4dcdd3c"
            }
          ]
        }
      ]
    }
  ]
}