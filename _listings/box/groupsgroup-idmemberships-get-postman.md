{
  "info": {
    "name": "Box Get Memberships for Group",
    "_postman_id": "382a5c64-499b-4786-986a-40112f82152d",
    "description": "Retrieves all of the members for a given group if the requesting user has access (see Group Object member_viewability_level).",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "efccb106-5e18-45da-89ba-3a0ec9c78cc7",
          "name": "getGroupMemberships",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "groups/:GROUP_ID/memberships"
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
                  "id": "GROUP_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves all of the members for a given group if the requesting user has access (see Group Object member_viewability_level)"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "986a949e-0cce-46a1-92e5-a4a0612494ed"
            }
          ]
        }
      ]
    }
  ]
}