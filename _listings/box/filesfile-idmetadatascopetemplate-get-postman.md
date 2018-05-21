{
  "info": {
    "name": "Box Get Metadata on File",
    "_postman_id": "c575df76-55b2-4403-b3f7-ec81791fee37",
    "description": "Used to retrieve the metadata template instance for a corresponding Box file.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "b79ae2df-8623-490e-97fe-aabf2a03601e",
          "name": "getFileMetadata",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "files/:FILE_ID/metadata/:SCOPE/:TEMPLATE"
              ],
              "variable": [
                {
                  "id": "FILE_ID",
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
            "description": "Used to retrieve the metadata template instance for a corresponding Box file"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1cd775ac-561f-4ad9-8510-b5b90db24725"
            }
          ]
        }
      ]
    }
  ]
}