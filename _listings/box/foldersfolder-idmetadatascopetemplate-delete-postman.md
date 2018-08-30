{
  "info": {
    "name": "Box Delete Metadata on Folder",
    "_postman_id": "efe6e2cc-5c62-4326-bfff-dfa9a8f5ad11",
    "description": "Used to delete the template instance. To delete custom key:value pairs within a template instance, you should refer to the updating metadata section.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "1d122b6e-bfd1-440b-8faa-c6538cb1a128",
          "name": "deleteFolderMetadata",
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
              "id": "269ea448-887f-44ab-86cb-1532ad882106"
            }
          ]
        }
      ]
    }
  ]
}