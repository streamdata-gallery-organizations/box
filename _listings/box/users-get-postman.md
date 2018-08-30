{
  "info": {
    "name": "Box Get Enterprise Users",
    "_postman_id": "ef3c67b6-b9fc-49c0-a05d-f3f2d7d55d76",
    "description": "Returns a list of all users for the Enterprise along with their user_id, public_name, and login.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "d38759f6-91d7-4bdb-a2e7-0e9a778944f7",
          "name": "getEnterpriseUsers",
          "request": {
            "url": "http://api.box.com/2.0/users?fields=%7B%7D&filter_term=%7B%7D&limit=%7B%7D&offset=%7B%7D&user_type=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of all users for the Enterprise along with their user_id, public_name, and login"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c17deda9-fdbe-42a6-ae2d-082e07a2b427"
            }
          ]
        }
      ]
    }
  ]
}