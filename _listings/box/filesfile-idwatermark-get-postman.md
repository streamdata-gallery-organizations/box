{
  "info": {
    "name": "Box Get Watermark on File",
    "_postman_id": "6b4de50d-5629-4022-b354-c613913a94f6",
    "description": "Used to retrieve the watermark for a corresponding Box file.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "3c85b3a8-990b-4d53-b7b4-7f3a8196cb2c",
          "name": "getFileWatermark",
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
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Used to retrieve the watermark for a corresponding Box file"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c574a9e7-2474-42da-ac48-307239155cf4"
            }
          ]
        }
      ]
    }
  ]
}