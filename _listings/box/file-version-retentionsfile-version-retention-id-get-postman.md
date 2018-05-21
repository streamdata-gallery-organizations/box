{
  "info": {
    "name": "Box Get File Version Retention",
    "_postman_id": "e6084503-eef9-4dc4-b085-3306aef6dcd5",
    "description": "Used to retrieve information about a file version retention",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "13a85e9d-b051-4715-8419-a979b0f56cce",
          "name": "getFileVersionRetention",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "file_version_retentions/:FILE_VERSION_RETENTION_ID"
              ],
              "variable": [
                {
                  "id": "FILE_VERSION_RETENTION_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Used to retrieve information about a file version retention"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "99cf8177-479a-4eea-8705-095b0fa795e7"
            }
          ]
        }
      ]
    }
  ]
}