{
  "info": {
    "name": "Box Get Membership",
    "_postman_id": "65182b47-7108-4260-9a1e-fc47b991d13b",
    "description": "Fetches a specific group membership entry.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "aeba2305-1618-4738-a6fb-e9bbe0c87c2d",
          "name": "getGroupMembership",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "group_memberships/:GROUP_MEMBERSHIP_ID"
              ],
              "query": [
                {
                  "key": "fields",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "GROUP_MEMBERSHIP_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Fetches a specific group membership entry"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5d1ef95c-3ebf-4bf0-b2db-91497c3cf914"
            }
          ]
        }
      ]
    }
  ]
}