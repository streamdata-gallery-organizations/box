{
  "info": {
    "name": "Box Get File Version Retentions",
    "_postman_id": "16fb0aed-e67a-4962-a45c-f51bde4c41a7",
    "description": "Retrieves all file version retentions for the given enterprise.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "f599492f-0681-4f8e-a68b-708d756eb52d",
          "name": "getFileVersionRetentions",
          "request": {
            "url": "http://api.box.com/2.0/file_version_retentions?disposition_action=%7B%7D&disposition_after=%7B%7D&disposition_before=%7B%7D&file_id=%7B%7D&file_version_id=%7B%7D&limit=%7B%7D&marker=%7B%7D&policy_id=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves all file version retentions for the given enterprise"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "383f0333-9527-4ac1-a6a7-35bde279c5c8"
            }
          ]
        }
      ]
    }
  ]
}