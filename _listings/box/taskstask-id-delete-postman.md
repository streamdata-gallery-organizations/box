{
  "info": {
    "name": "Box Delete Task",
    "_postman_id": "1ecfda69-340a-46c0-804f-f08e2a8d4e0e",
    "description": "Permanently deletes a specific task.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "fa7bea6d-2e44-4eef-ab02-6664c4b5885e",
          "name": "deleteTask",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "tasks/:TASK_ID"
              ],
              "variable": [
                {
                  "id": "TASK_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Permanently deletes a specific task"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "70f00776-3058-499e-b3fd-b9286f7f55e3"
            }
          ]
        }
      ]
    }
  ]
}