{
  "info": {
    "name": "Box User Events, Enterprise Events",
    "_postman_id": "77e224c6-d401-4d6a-8770-35bd4fc7d516",
    "description": "Use this to get events for a given user. A chunk of event objects is returned for the user based on the parameters passed in. Parameters indicating how many chunks are left as well as the next stream_position are also returned.\n\nTo retrieve Enterprise Events specify 'stream_type=admin_logs'. Retrieves up to a year' events for all users in an enterprise. Upper and lower bounds as well as filters can be applied to the results.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "84c13b1a-984b-4fa8-b62b-1494ee00af38",
          "name": "getUserEvents",
          "request": {
            "url": "http://api.box.com/2.0/events?created_after=%7B%7D&created_before=%7B%7D&event_type=%7B%7D&limit=%7B%7D&stream_position=%7B%7D&stream_type=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Use this to get events for a given user"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c5032023-9f74-46b4-92ae-d51c8bb2f0ec"
            }
          ]
        }
      ]
    }
  ]
}