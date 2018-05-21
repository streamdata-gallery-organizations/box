{
  "info": {
    "name": "Box Searching for Content",
    "_postman_id": "91a6a31b-b3ab-4b3b-b77f-6a39bbfafaa8",
    "description": "The search endpoint provides a powerful way of finding items that are accessible by a single user or an entire enterprise. Leverage the parameters listed below to generate targeted advanced searches.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "37060d06-385c-4cad-82e3-353eff13e045",
          "name": "search",
          "request": {
            "url": "http://api.box.com/2.0/search?ancestor_folder_ids=%7B%7D&content_types=%7B%7D&created_at_range=%7B%7D&file_extensions=%7B%7D&limit=%7B%7D&mdfilters=%7B%7D&offset=%7B%7D&owner_user_ids=%7B%7D&query=%7B%7D&scope=%7B%7D&size_range=%7B%7D&trash_content=%7B%7D&type=%7B%7D&updated_at_range=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "The search endpoint provides a powerful way of finding items that are accessible by a single user or an entire enterprise"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "52a61657-f372-4a3b-93a6-8096ef27832b"
            }
          ]
        }
      ]
    }
  ]
}