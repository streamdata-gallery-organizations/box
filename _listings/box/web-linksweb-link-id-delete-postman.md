{
  "info": {
    "name": "Box Delete Web Link",
    "_postman_id": "c9eea56a-5a53-4cf6-8fc4-4a779d1ece9a",
    "description": "Deletes a web link and moves it to the trash",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "240b97e1-8123-4a87-bd20-02584c7c62e0",
          "name": "deleteWebLink",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "web_links/:WEB_LINK_ID"
              ],
              "variable": [
                {
                  "id": "WEB_LINK_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes a web link and moves it to the trash"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ec22391a-3a77-40bb-a456-687b92eafc90"
            }
          ]
        }
      ]
    }
  ]
}