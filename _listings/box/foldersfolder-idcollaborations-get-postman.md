{
  "info": {
    "name": "Box Get Folder Collaborations",
    "_postman_id": "5b257fd3-6377-467a-bd62-ae51897ba951",
    "description": "Use this to get a list of all the collaborations on a folder i.e. all of the users that have access to that folder.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "201701be-4983-4529-ab2a-f9e63d7c9c41",
          "name": "getFolderCollaborations",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "folders/:FOLDER_ID/collaborations"
              ],
              "query": [
                {
                  "key": "fields",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "offset",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "FOLDER_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Use this to get a list of all the collaborations on a folder i"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2b09bfe9-8dc6-41a8-9fd8-b0617d92c0e9"
            }
          ]
        }
      ]
    }
  ]
}