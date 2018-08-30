{
  "info": {
    "name": "Box Get Folder's Info",
    "_postman_id": "f31d98a4-51f4-4fa4-b0e2-66af7d6b5895",
    "description": "Retrieves the full metadata about a folder, including information about when it was last updated as well as the files and folders contained in it. The root folder of a Box account is always represented by the id ???0???.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "0a97b3ee-4699-4dba-b5b3-c574ef16c2b6",
          "name": "getFolder",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "folders/:FOLDER_ID"
              ],
              "query": [
                {
                  "key": "fields",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "FOLDER_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves the full metadata about a folder, including information about when it was last updated as well as the files and folders contained in it"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a3ae7731-d37b-491e-be24-cb38bddadb5a"
            }
          ]
        }
      ]
    }
  ]
}