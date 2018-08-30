{
  "info": {
    "name": "Box Get File's Tasks",
    "_postman_id": "4fbf5002-f382-415b-b4c2-1506c9b0d3cd",
    "description": "Retrieves all of the tasks for given file.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "149283a8-03c4-4034-9226-7678c9e4e3e5",
          "name": "getFileTasks",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "files/:FILE_ID/tasks"
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
            "description": "Retrieves all of the tasks for given file"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a9f40ff8-5107-4241-b887-e9f6a71f2d25"
            }
          ]
        }
      ]
    }
  ]
}