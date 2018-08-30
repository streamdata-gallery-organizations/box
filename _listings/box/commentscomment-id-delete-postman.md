{
  "info": {
    "name": "Box Delete Comment",
    "_postman_id": "b4e5b272-38fe-420f-b4e9-da9dd2b1fb4d",
    "description": "Permanently deletes a comment.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "eb2b06bb-33e6-4bb0-b5af-a4d7e8e2ec35",
          "name": "deleteComment",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "comments/:COMMENT_ID"
              ],
              "variable": [
                {
                  "id": "COMMENT_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Permanently deletes a comment"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d2049904-0e2f-474d-9cb4-e0cf64477e75"
            }
          ]
        }
      ]
    }
  ]
}