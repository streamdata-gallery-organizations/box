{
  "info": {
    "name": "Box Get File Version Legal Hold",
    "_postman_id": "5e1011bc-415b-4193-8609-1f5aafff9d2a",
    "description": "Get details of a single File Version Legal Hold.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "67736efe-b311-4ebb-848a-40dc3ad5d638",
          "name": "getFileVersionLegalHoldPolicy",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "file_version_legal_holds/:ID"
              ],
              "variable": [
                {
                  "id": "ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get details of a single File Version Legal Hold"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d784cf9a-a53e-4405-9f9d-38d1d0d611de"
            }
          ]
        }
      ]
    }
  ]
}