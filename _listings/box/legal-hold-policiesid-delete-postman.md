{
  "info": {
    "name": "Box Delete Legal Hold Policy",
    "_postman_id": "c3417176-a6da-4b86-80a6-c3f132a5b9f4",
    "description": "Sends request to delete an existing Legal Hold Policy. Note that this is an asynchronous process - the Policy will not be fully deleted yet when the response comes back.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "c9bc2d78-3f17-433b-8ad4-aca80d557117",
          "name": "deleteLegalHoldPolicy",
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
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Sends request to delete an existing Legal Hold Policy"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c500a7fc-e809-4c72-b1b5-34692faa8412"
            }
          ]
        }
      ]
    }
  ]
}