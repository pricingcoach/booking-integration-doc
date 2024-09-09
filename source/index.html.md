---
title: Booking API Documentation

language_tabs:
  - java

toc_footers:
  - <a href='https://bookingapi.pricing-coach.com/swagger-ui/index.html' target="_blank">Sign Up for a Developer Key</a>

includes:
  - errors

search: true

code_clipboard: true

meta:
  - name: description
    content: Documentation for the Booking API
---

# Booking API Documentation

Welcome to the Pricing-Coach API Documentation! 

Pricing-Coach API is a communication platform that allows sending and receiving information about buildings, reservations and prices.

# PMS Send Dynamic Price

## Send Dynamic Price


It is the service that should be used to send a new reservation record. There is no need to enter any parameters when calling this service.

> Request:

```json
[
  {
  "roomName": "A Room Name",
  "price": 75,
  "date": "2024-09-20"
},
{
  "roomName": "B Room Name",
  "price": 75,
  "date": "2024-09-21"
},
...
]
```

> Response:

```json

```

### HTTP Request

`POST https://{integration endpoit information}`

### Query Parameters

Parameter | Type | Required |  Description
--------- | ------- | ------- | -----------
NO_PARAMS 

### Schema (Request)

Name | type | example | description
--------- | ------- | ----------- | -------
roomName  | string  | A Room Name |  Contains information about the room type
price | integer | 75 | Price information
date | DateTime | 2024-09-20  | Date information




### Schema (Response)

Name | type | example | description
--------- | ------- | ----------- | -------
