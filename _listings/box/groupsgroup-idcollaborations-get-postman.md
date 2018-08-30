{
  "info": {
    "name": "Box Get Collaborations for Group",
    "_postman_id": "ca56f693-81e9-488f-ae52-4b0628815a05",
    "description": "Retrieves all of the group collaborations for a given group. Note this is only available to group admins.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "314aabaf-d7a2-43fe-bed9-41bfe8050318",
          "name": "getGroupCollaborations",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "groups/:GROUP_ID/collaborations"
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
            "description": "Retrieves all of the group collaborations for a given group"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ee81b900-df81-4942-b108-c3efbbbea5f4"
            }
          ]
        }
      ]
    }
  ]
}