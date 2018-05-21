{
  "info": {
    "name": "Box Permanently Delete",
    "_postman_id": "87757396-6486-4a3f-913a-9609586549ae",
    "description": "Permanently deletes an item that is in the trash. The item will no longer exist in Box. This action cannot be undone.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "e5b2c573-764c-4a97-9710-19071400833a",
          "name": "deleteTrashedFile",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "files/:FILE_ID/trash"
              ],
              "variable": [
                {
                  "id": "FILE_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Permanently deletes an item that is in the trash"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "101b8d1f-10ab-4cdd-a663-d9123c6d71e4"
            }
          ]
        }
      ]
    }
  ]
}