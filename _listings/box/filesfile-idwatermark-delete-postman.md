{
  "info": {
    "name": "Box Remove Watermark on File",
    "_postman_id": "d6a01e77-b46f-4746-92f8-0e3f0d0e2a41",
    "description": "Used to remove the watermark for a corresponding Box file.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "98c51a3f-6861-4ade-9b8d-fabea4194522",
          "name": "deleteFileWatermark",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "files/:FILE_ID/watermark"
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
            "description": "Used to remove the watermark for a corresponding Box file"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "133452f4-5b35-4f0e-bb42-bc738cdbf126"
            }
          ]
        }
      ]
    }
  ]
}