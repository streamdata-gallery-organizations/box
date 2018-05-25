{
  "info": {
    "name": "Box Get Thumbnail",
    "_postman_id": "9591a993-a042-44b4-91a6-6c1b1f52fad0",
    "description": "Retrieves a thumbnail, or smaller image representation, of this file. Sizes of 32x32,64x64, 128x128, and 256x256 can be returned in the .png format and sizes of 32x32, 94x94, 160x160, and 320x320 can be returned in the .jpg format. Thumbnails can be generated for the image and video file formats listed here.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "db57602b-287e-4187-8619-19d854a61d8d",
          "name": "getFileThumbnail",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "files/:FILE_ID/thumbnail.:EXTENSION"
              ],
              "query": [
                {
                  "key": "max_height",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "max_width",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "min_height",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "min_width",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "EXTENSION",
                  "value": "{}",
                  "type": "string"
                },
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
            "description": "Retrieves a thumbnail, or smaller image representation, of this file"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e0e971fa-6475-4f1d-9cc4-cd4f4b666185"
            }
          ]
        }
      ]
    }
  ]
}