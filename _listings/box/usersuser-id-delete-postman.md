{
  "info": {
    "name": "Box Delete User",
    "_postman_id": "5fef96bc-3589-4478-b027-a52d1117ab1f",
    "description": "Deletes a user in an enterprise account.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "d95707d2-b552-4e58-9703-e7c4de32ad14",
          "name": "deleteUser",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "users/:USER_ID"
              ],
              "query": [
                {
                  "key": "force",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "notify",
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
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes a user in an enterprise account"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fa74af46-20ed-45ee-9ec9-37bcf907985c"
            }
          ]
        }
      ]
    }
  ]
}