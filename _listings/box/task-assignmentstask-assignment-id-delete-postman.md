{
  "info": {
    "name": "Box Delete Task Assignment",
    "_postman_id": "835e814e-ce16-481e-b049-ff93af6d1de6",
    "description": "Deletes a specific task assignment.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "ac83ab31-22a1-4a47-a02c-b73439789002",
          "name": "deleteTaskAssignment",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "task_assignments/:TASK_ASSIGNMENT_ID"
              ],
              "variable": [
                {
                  "id": "TASK_ASSIGNMENT_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes a specific task assignment"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "51660fca-519f-4cb1-a44e-b5b73b901bb4"
            }
          ]
        }
      ]
    }
  ]
}