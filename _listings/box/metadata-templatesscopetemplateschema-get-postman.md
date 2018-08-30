{
  "info": {
    "name": "Box Get Metadata Template",
    "_postman_id": "1780c711-773c-40e1-9ff0-9eee52b8e1a5",
    "description": "Used to retrieve the schema for a given metadata template.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "4b8251a4-cb63-468e-a897-70238f5b2c8a",
          "name": "getMetadataTemplate",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "metadata_templates/:SCOPE/:TEMPLATE/schema"
              ],
              "variable": [
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
            "description": "Used to retrieve the schema for a given metadata template"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "937187bd-e8c7-4ac4-bf92-76286724764c"
            }
          ]
        }
      ]
    }
  ]
}