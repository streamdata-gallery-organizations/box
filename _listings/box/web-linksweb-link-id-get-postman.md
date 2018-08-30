{
  "info": {
    "name": "Box Get Web Link",
    "_postman_id": "21e28189-ee2a-4f28-8282-472da3ea787a",
    "description": "Use to get information about the web link.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "3f554ad5-02f7-449e-94b4-4a92b4629b48",
          "name": "getWebLink",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "web_links/:WEB_LINK_ID"
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
                  "id": "WEB_LINK_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Use to get information about the web link"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d8060306-9f1b-4018-8873-5733f12b2d1d"
            }
          ]
        }
      ]
    }
  ]
}