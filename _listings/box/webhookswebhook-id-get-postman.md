{
  "info": {
    "name": "Box Get Webhook",
    "_postman_id": "83c36d63-ba3c-4ec3-a053-98c9c9f9e075",
    "description": "Get a Webhook",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "e79bd737-09b3-41c4-939c-467cb75e6ac1",
          "name": "getWebhook",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "webhooks/:WEBHOOK_ID"
              ],
              "variable": [
                {
                  "id": "WEBHOOK_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get a Webhook"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "35c932b5-7a6a-4be8-869c-f6893199b0fa"
            }
          ]
        }
      ]
    }
  ]
}