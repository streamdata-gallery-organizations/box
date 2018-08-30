{
  "info": {
    "name": "Box Shared Items",
    "_postman_id": "78afa934-b7c8-44c6-b66d-29f8686e364c",
    "description": "Shared items are any files or folders that are represented by a shared link. Shared items are different from other API resources in that a shared resource doesn???t necessarily have to be in the account of the user accessing it. The actual shared link itself is used along with a normal access token.\nUsed to retrieve the metadata about a shared item when only given a shared link. Because of varying permission for shared links, a password may be required to retrieve the shared item. Once the item has been retrieved, you can make API requests against the actual resource /files/{id} or /folders/{id} as long as the shared link and optional password are in the header.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "3281de05-c613-4a84-801f-bc980bf7e6aa",
          "name": "getSharedItems",
          "request": {
            "url": "http://api.box.com/2.0/shared_items",
            "method": "GET",
            "header": [
              {
                "key": "BoxApi",
                "value": "{}",
                "description": "The usage is 'BoxApi: shared_link=SHARED_LINK&shared_link_password=SHARED_LINK_PASSWORD'",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Shared items are any files or folders that are represented by a shared link"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "08d61a94-51bd-4006-bad0-d6826ae96a52"
            }
          ]
        }
      ]
    }
  ]
}