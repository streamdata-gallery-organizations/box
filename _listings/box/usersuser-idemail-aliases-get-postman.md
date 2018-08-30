{
  "info": {
    "name": "Box",
    "_postman_id": "5649b13f-d05f-406d-8d19-86b72dbce48a",
    "description": "The Box Content API gives you access to secure content management and content experience features for use in your own app. It strives to be RESTful and is organized around the main resources you&rsquo;re familiar with from the Box web interface.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "ed6390a3-8fe0-4026-a431-8fbbaf5ef60f",
          "name": "getEmailAliases",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "users/:USER_ID/email_aliases"
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
            "description": "Retrieves all email aliases for this user"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e6273946-6262-4738-941f-ed42deec89cb"
            }
          ]
        }
      ]
    }
  ]
}