{
  "info": {
    "name": "Box Pending Collaborations",
    "_postman_id": "ad269b35-af1d-428f-b01b-ceb5adfc6dc0",
    "description": "Used to retrieve all pending collaboration invites for this user.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "9ed0611c-bb0d-4f78-b787-1ba50a46c1a4",
          "name": "getPendingCollaborations",
          "request": {
            "url": "http://api.box.com/2.0/collaborations?fields=%7B%7D&status=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Used to retrieve all pending collaboration invites for this user"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "880aeaf9-bacb-41cb-882b-96be4defbd28"
            }
          ]
        }
      ]
    }
  ]
}