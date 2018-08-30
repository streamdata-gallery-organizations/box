{
  "info": {
    "name": "Box Delete Group",
    "_postman_id": "3ecace94-e916-409f-92d2-112dd052245d",
    "description": "Permanently deletes a specific group.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "de1627c7-07dd-43fc-9ff2-18a1e07316ba",
          "name": "deleteGroup",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "groups/:GROUP_ID"
              ],
              "variable": [
                {
                  "id": "GROUP_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Permanently deletes a specific group"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "44ddee2d-e4f5-4bce-ac5c-209ba917c268"
            }
          ]
        }
      ]
    }
  ]
}