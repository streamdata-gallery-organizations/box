{
  "info": {
    "name": "Box Get Comment",
    "_postman_id": "141174f6-bdb3-4210-942c-75f2b556b308",
    "description": "Used to retrieve the message and metadata about a specific comment. Information about the user who created the comment is also included.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "e434bfd8-8856-4380-8fa1-8725b525a02b",
          "name": "getComment",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "comments/:COMMENT_ID"
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
                  "id": "COMMENT_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Used to retrieve the message and metadata about a specific comment"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1a34b605-5736-4045-8978-39c14572ab2a"
            }
          ]
        }
      ]
    }
  ]
}