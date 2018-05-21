{
  "info": {
    "name": "Box Get Trashed File",
    "_postman_id": "55c7e365-5b0c-4d39-813c-f1d8cc51a4d3",
    "description": "Retrieves an item that has been moved to the trash.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "632a91f2-43b0-4f8b-8c62-eb319bb41536",
          "name": "getTrashedFile",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "files/:FILE_ID/trash"
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
            "description": "Retrieves an item that has been moved to the trash"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5ee88430-cabe-450c-8a57-27d4b2b49600"
            }
          ]
        }
      ]
    }
  ]
}