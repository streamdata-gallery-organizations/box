{
  "info": {
    "name": "Box Get Metadata on Folder",
    "_postman_id": "552f6735-5629-4d81-ad70-d51bc251a449",
    "description": "Used to retrieve the metadata template instance for a corresponding Box folder.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "ce0e0868-3d71-406b-b3b2-552e3fdcd9d9",
          "name": "getFolderMetadata",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "folders/:FOLDER_ID/metadata/:SCOPE/:TEMPLATE"
              ],
              "variable": [
                {
                  "id": "FOLDER_ID",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "SCOPE",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "TEMPLATE",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Used to retrieve the metadata template instance for a corresponding Box folder"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ee8ad7f1-712c-422c-97c8-0e76cb483ba6"
            }
          ]
        }
      ]
    }
  ]
}