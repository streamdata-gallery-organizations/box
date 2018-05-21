{
  "info": {
    "name": "Box Get Assignments",
    "_postman_id": "f583320b-25de-469e-a0f4-058b03121813",
    "description": "Retrieves all of the assignments for a given task.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "4ffd3983-2865-4959-b469-0937b54487f1",
          "name": "getTaskAssignments",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "tasks/:TASK_ID/assignments"
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
            "description": "Retrieves all of the assignments for a given task"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2968dc5b-4be7-4cc5-8d3e-28ddd69ad3af"
            }
          ]
        }
      ]
    }
  ]
}