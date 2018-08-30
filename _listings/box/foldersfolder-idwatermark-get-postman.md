{
  "info": {
    "name": "Box Get Watermark on Folder",
    "_postman_id": "c271f00a-4470-4c90-bb6e-17747ca4a0e8",
    "description": "Used to retrieve the watermark for a corresponding Box folder.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "befc0d00-7118-4a4b-9483-ebd682e9968f",
          "name": "getFolderWatermark",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "folders/:FOLDER_ID/watermark"
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
            "description": "Used to retrieve the watermark for a corresponding Box folder"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "962d8ccf-0747-416a-a297-d7cecd5bdd40"
            }
          ]
        }
      ]
    }
  ]
}