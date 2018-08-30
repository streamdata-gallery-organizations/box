{
  "info": {
    "name": "Box Get Webhooks",
    "_postman_id": "e2c7e17a-c35f-45ed-98c5-dac550a7ddf2",
    "description": "Returns all defined webhooks for the requesting application and user, up to the limit. If no limit is supplied then Box uses the default limit of 100.\nIf more than limit webhooks are defined then Box returns the webhooks in batches. When the results are batched, Box sends limit webhooks along with a next_marker field in the response object. The value of the next_marker field is a marker string that you can use in later requests to tell Box which batch to send next.\nWhen you send a request that includes a marker string, Box sends the next batch of webhooks, beginning after the last webhook of the previous batch. When the response contains the last of the defined webhooks, Box omits the next_marker field from its response.\nYou can use limit and marker together with the marker string returned in the next_marker field to paginate lists of webhooks.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "documents",
      "item": [
        {
          "id": "ac7c0658-451a-4c0d-a0c1-d73d9066e85d",
          "name": "getWebhooks",
          "request": {
            "url": "http://api.box.com/2.0/webhooks?limit=%7B%7D&marker=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns all defined webhooks for the requesting application and user, up to the limit"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "99973f58-598e-491f-b53b-8bf15cf45a32"
            }
          ]
        }
      ]
    }
  ]
}