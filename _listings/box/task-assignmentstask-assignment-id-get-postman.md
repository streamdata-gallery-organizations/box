{
  "info": {
    "name": "Box Get Task Assignment",
    "_postman_id": "b8c36405-615d-43c6-bc0b-ae9312f1bfe1",
    "description": "Fetches a specific task assignment.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "7ad225fe-f405-451d-a4f8-beedea5dea5a",
          "name": "getTaskAssignment",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "task_assignments/:TASK_ASSIGNMENT_ID"
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
                  "id": "TASK_ASSIGNMENT_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Fetches a specific task assignment"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c765d85e-b41f-412b-925a-626349a1975b"
            }
          ]
        }
      ]
    }
  ]
}