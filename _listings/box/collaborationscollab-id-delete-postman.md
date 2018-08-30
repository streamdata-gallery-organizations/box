{
  "info": {
    "name": "Box Delete Collaboration",
    "_postman_id": "438a3e43-bad5-46c1-8911-b217a6c6ac3c",
    "description": "Used to delete a single collaboration.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "72add73d-7c82-405f-82b2-326f1be7a848",
          "name": "deleteCollaboration",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "collaborations/:COLLAB_ID"
              ],
              "variable": [
                {
                  "id": "COLLAB_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Used to delete a single collaboration"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a263c383-285c-46ff-99ba-53fca024233a"
            }
          ]
        }
      ]
    }
  ]
}