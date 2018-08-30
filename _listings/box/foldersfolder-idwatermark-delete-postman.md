{
  "info": {
    "name": "Box Remove Watermark on Folder",
    "_postman_id": "bfd5b0b1-c132-4b87-9c02-9963337fca7e",
    "description": "Used to remove the watermark for a corresponding Box Folder.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "ab7bb815-3f4d-4a7a-9b74-5690470bf2c0",
          "name": "deleteFolderWatermark",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "folders/:FOLDER_ID/watermark"
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
            "description": "Used to remove the watermark for a corresponding Box Folder"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b473a61f-ed70-46d5-8af4-79750ad380c9"
            }
          ]
        }
      ]
    }
  ]
}