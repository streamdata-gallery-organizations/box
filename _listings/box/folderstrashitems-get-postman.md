{
  "info": {
    "name": "Box Get Trashed Items",
    "_postman_id": "dfe8998f-609c-4724-ab98-adf445b60406",
    "description": "Retrieves the files and/or folders that have been moved to the trash. Any attribute in the full files or folders objects can be passed in with the fields parameter to get specific attributes, and only those specific attributes back; otherwise, the mini format is returned for each item by default. Multiple attributes can be passed in separated by commas e.g. fields=name,created_at. Paginated results can be retrieved using the limit and offset parameters.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "61ed3ed1-2451-4e05-a3e2-ec7f5683f510",
          "name": "getTrashedItems",
          "request": {
            "url": "http://api.box.com/2.0/folders/trash/items?fields=%7B%7D&limit=%7B%7D&offset=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves the files and/or folders that have been moved to the trash"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5e03f14a-9f8a-4b31-a52d-18f760b41682"
            }
          ]
        }
      ]
    }
  ]
}