{
  "info": {
    "name": "Box Get Enterprise Device Pins",
    "_postman_id": "2d2cd031-2ed8-4cd8-8527-45b70c4f439d",
    "description": "Gets all the device pins within a given enterprise. Must be an enterprise admin with the manage enterprise scope to make this call.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "937590f9-594b-4c2a-8cd1-ec1b63b916aa",
          "name": "getEnterpriseDevicePins",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "enterprises/:ENTERPRISE_ID/device_pinners"
              ],
              "query": [
                {
                  "key": "direction",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "marker",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "ENTERPRISE_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets all the device pins within a given enterprise"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "46334940-d990-4d6f-a75e-6ccc04b89b0c"
            }
          ]
        }
      ]
    }
  ]
}