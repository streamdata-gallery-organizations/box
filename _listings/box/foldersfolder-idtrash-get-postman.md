{
  "info": {
    "name": "Box Get Trashed Folder",
    "_postman_id": "c90761d8-98a3-493d-a168-a6710fb32f2f",
    "description": "Retrieves an folder that has been moved to the trash.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "e813b726-56af-4b3a-bd8d-3cd708659866",
          "name": "getTrashedFolder",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "folders/:FOLDER_ID/trash"
              ],
              "query": [
                {
                  "key": "fields",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "FOLDER_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves an folder that has been moved to the trash"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "95323a28-ee6e-433c-baa2-f5b78fdafa49"
            }
          ]
        }
      ]
    }
  ]
}