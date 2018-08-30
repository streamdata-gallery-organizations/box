{
  "info": {
    "name": "Box Get Device Pin",
    "_postman_id": "38703662-bc48-4e66-a177-a2b13bb782ee",
    "description": "Gets information about an individual device pin.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "64dcef29-0782-4011-88ff-554af13b5168",
          "name": "getDevicePin",
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
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets information about an individual device pin"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0327b6c0-e028-43c4-a746-393940b0b238"
            }
          ]
        }
      ]
    }
  ]
}