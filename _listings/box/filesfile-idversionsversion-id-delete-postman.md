{
  "info": {
    "name": "Box Delete Old Version",
    "_postman_id": "1101920a-83fe-4b96-b97b-02abd86b36e2",
    "description": "Discards a specific file version to the trash. (Depending on the enterprise settings for this user, the item will either be actually deleted from Box or moved to the trash.)",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "60839ef1-cd50-45a9-9ce2-1418a553d313",
          "name": "deleteFileVersion",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "files/:FILE_ID/versions/:VERSION_ID"
              ],
              "variable": [
                {
                  "id": "FILE_ID",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "VERSION_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "header": [
              {
                "key": "If-Match",
                "value": "{}",
                "description": "The etag of the file",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Discards a specific file version to the trash"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b4c9eeb7-05f1-4540-a245-03c79fe3ec04"
            }
          ]
        }
      ]
    }
  ]
}