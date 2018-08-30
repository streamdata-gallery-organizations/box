{
  "info": {
    "name": "Box Delete Metadata on File",
    "_postman_id": "2dd4d34d-68ae-4314-8c07-5642535da21e",
    "description": "Used to delete the template instance. To delete custom key:value pairs within a template instance, you should refer to the updating metadata section.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "dce93b4f-427a-4381-924d-47503b000ec0",
          "name": "deleteFileMetadata",
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
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Used to delete the template instance"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f505dcdb-4f77-4530-b33f-081b7f52d95e"
            }
          ]
        }
      ]
    }
  ]
}