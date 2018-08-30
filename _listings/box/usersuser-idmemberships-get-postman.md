{
  "info": {
    "name": "Box Get Memberships for User",
    "_postman_id": "be208cf2-edf9-4882-babe-9ae9098e2393",
    "description": "Retrieves all of the group memberships for a given user. Note this is only available to group admins. To retrieve group memberships for the user making the API request, use the users/me/memberships endpoint.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "77298f80-b33e-443c-a7ee-ef8debbfe6c9",
          "name": "getUserGroupMembership",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "users/:USER_ID/memberships"
              ],
              "query": [
                {
                  "key": "fields",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "offset",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "USER_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves all of the group memberships for a given user"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "68b30910-bac0-47c7-9f60-8611eb4c0fde"
            }
          ]
        }
      ]
    }
  ]
}