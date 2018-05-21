{
  "info": {
    "name": "Box Get Collections",
    "_postman_id": "35607abd-b127-4fb2-b684-f3ef5bd5bb93",
    "description": "Retrieves the collections for the given user. Currently, only the favorites collection is supported.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "86fb367d-3f66-43ea-b3c6-ec49105f2883",
          "name": "getCollections",
          "request": {
            "url": "http://api.box.com/2.0/collections",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves the collections for the given user"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8a14d2a9-11be-4e7e-9c42-76eb72d96b26"
            }
          ]
        }
      ]
    }
  ]
}