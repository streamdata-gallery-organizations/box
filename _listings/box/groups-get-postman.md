{
  "info": {
    "name": "Box Get Groups for an Enterprise",
    "_postman_id": "fdd01190-942b-419c-bbbf-244f22121dd1",
    "description": "Retrieves all of the groups for given enterprise. Must have permissions to see an enterprise's groups.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "b41661e8-a684-408f-ae22-70ec2ef89c2f",
          "name": "getEnterpriseGroups",
          "request": {
            "url": "http://api.box.com/2.0/groups?fields=%7B%7D&limit=%7B%7D&offset=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves all of the groups for given enterprise"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4aabcaca-8612-4aa1-8f0a-ae35511a8361"
            }
          ]
        }
      ]
    }
  ]
}