{
  "info": {
    "name": "Box Get Enterprise Metadata",
    "_postman_id": "42f37927-d8e4-4cc2-8a6d-429f017f86d8",
    "description": "Used to retrieve all metadata templates within a user's enterprise. Currently only the enterprise scope is supported.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "c0e03059-cdc8-46c7-8090-37154fb22c44",
          "name": "getEnterpriseMetadataTemplates",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "metadata_templates/:SCOPE"
              ],
              "variable": [
                {
                  "id": "SCOPE",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Used to retrieve all metadata templates within a user's enterprise"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "11d5339a-a1a5-4fbf-b8f3-82ef081b0d9b"
            }
          ]
        }
      ]
    }
  ]
}