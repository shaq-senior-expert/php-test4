# PHP Assessment Test

### Problem 4:

## test - task4.html

#1. Endpoint URL for adding a lot of apples:

POST /api/lots

Request Payload:
{
  "seller": "Delicious Apples LTD",
  "cultivar": "Red Dacca",
  "origin_country": "Costa Rica",
  "harvest_date": "2018-07-27",
  "weight": 500
}

Response Payload:
{
  "id": "12345",
  "seller": "Delicious Apples LTD",
  "cultivar": "Red Dacca",
  "origin_country": "Costa Rica",
  "harvest_date": "2018-07-27",
  "weight": 500,
  "auction_status": "Not started"
}

Response Status Code:

201 Created


#2. Endpoint URL for updating the lot with a new harvesting date:

PATCH /api/lots/12345

Request Payload:
{
  "harvest_date": "2018-06-14"
}

Response Payload:
{
  "id": "12345",
  "seller": "Delicious Apples LTD",
  "cultivar": "Red Dacca",
  "origin_country": "Costa Rica",
  "harvest_date": "2018-06-14",
  "weight": 500,
  "auction_status": "Not started"
}

Response Status Code:
200 OK


#3. Endpoint URL for validating the minimum weight of a lot:

POST /api/lots/validate

Request Payload:
{
  "seller": "Delicious Apples LTD",
  "cultivar": "Red Dacca",
  "origin_country": "Costa Rica",
  "harvest_date": "2018-07-27",
  "weight": 500
}

Response Payload:
{
  "error": "Minimum lot weight allowed is 1000kg"
}

Response Status Code:
400 Bad Request

