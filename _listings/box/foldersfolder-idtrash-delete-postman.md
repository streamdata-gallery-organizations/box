{
  "info": {
    "name": "Box Permanently Delete",
    "_postman_id": "14d0703c-383a-4bbd-90ce-d8d4ffac594d",
    "description": "Permanently deletes an folder that is in the trash. The item will no longer exist in Box. This action cannot be undone.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "2ef7902b-15fe-46a0-a39b-fa9b713e4253",
          "name": "deleteTrashedFolder",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "folders/:FOLDER_ID/trash"
              ],
              "variable": [
                {
                  "id": "FOLDER_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Permanently deletes an folder that is in the trash"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c9100ad9-4250-4b49-8942-e4a7928e7143"
            }
          ]
        }
      ]
    }
  ]
}