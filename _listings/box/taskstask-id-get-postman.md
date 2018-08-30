{
  "info": {
    "name": "Box Get Task",
    "_postman_id": "1ca7a84e-b43f-4116-a08c-e38fd114cf10",
    "description": "Fetches a specific task.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "37acc9e5-64f4-4021-b313-f92942b65ea6",
          "name": "getTask",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "tasks/:TASK_ID"
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
                  "id": "TASK_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Fetches a specific task"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1b4fd421-358f-428f-8abe-f98137a37ead"
            }
          ]
        }
      ]
    }
  ]
}