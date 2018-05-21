{
  "info": {
    "name": "Box",
    "_postman_id": "a8c1dd9b-8262-4844-b9e9-eb2545b53141",
    "description": "The Box Content API gives you access to secure content management and content experience features for use in your own app. It strives to be RESTful and is organized around the main resources you&rsquo;re familiar with from the Box web interface.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "eaf58220-1d28-4d08-a978-ac5f78eee663",
          "name": "deleteUserEmailAlias",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "users/:USER_ID/email_aliases/:EMAIL_ALIAS_ID"
              ],
              "variable": [
                {
                  "id": "EMAIL_ALIAS_ID",
                  "value": "{}",
                  "type": "string"
                },
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
            "description": "Removes an email alias from a user"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f73b5d9c-a358-430a-946d-c308ffab85de"
            }
          ]
        }
      ]
    }
  ]
}