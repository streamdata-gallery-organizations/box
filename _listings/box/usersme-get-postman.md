{
  "info": {
    "name": "Box Get Current User",
    "_postman_id": "d224a198-e287-4ea1-a8a5-4f592a2af505",
    "description": "Retrieves information about the user who is currently logged in i.e. the user for whom this auth token was generated.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "404c528f-6765-4261-a881-d5cc88dce2fd",
          "name": "getCurrentUser",
          "request": {
            "url": "http://api.box.com/2.0/users/me?fields=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves information about the user who is currently logged in i"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4245a4d7-9c11-44f4-96e2-c8ffb94e3ea1"
            }
          ]
        }
      ]
    }
  ]
}