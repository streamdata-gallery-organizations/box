{
  "info": {
    "name": "Box Delete Membership",
    "_postman_id": "7140b25e-adb7-4b67-a3ec-10fbb72b0eb4",
    "description": "Deletes a specific group membership.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "617ccec4-5836-4cc9-9e2a-6141f7c370aa",
          "name": "deleteGroupMembership",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.box.com",
              "path": [
                "2.0",
                "group_memberships/:GROUP_MEMBERSHIP_ID"
              ],
              "variable": [
                {
                  "id": "GROUP_MEMBERSHIP_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes a specific group membership"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "166d9a28-d6a1-47d0-90e7-a3a5cb0593db"
            }
          ]
        }
      ]
    }
  ]
}