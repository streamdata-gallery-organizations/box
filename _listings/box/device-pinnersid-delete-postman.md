{
  "info": {
    "name": "Box Delete Device Pin",
    "_postman_id": "812372eb-53e4-49cd-9de6-9a30f8bdbfa5",
    "description": "Delete individual device pin.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "ba8b07d2-5438-490e-a461-38e48eaa85cd",
          "name": "deleteDevicePin",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "device_pinners/:ID"
              ],
              "variable": [
                {
                  "id": "ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Delete individual device pin"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "522f94ed-f774-4ea0-8d04-49125b8bf12d"
            }
          ]
        }
      ]
    }
  ]
}