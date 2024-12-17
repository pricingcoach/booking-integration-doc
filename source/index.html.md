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

## Send Dynamic Price Example 1


It is the service that should be used to send a new reservation record. There is no need to enter any parameters when calling this service.

> Request:

```json
[
  {
  "roomName": "A Room Name",
  "price": 75,
  "startDate": "2024-08-20",
  "endDate": "2024-09-20"
},
{
  "roomName": "B Room Name",
  "price": 75,
  "startdate": "2024-08-21",
  "endDate":"2024-09-21"
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
startDate | DateTime | 2024-08-20  | Date information
endDate   | DateTime | 2024-09-20  | Date information




### Schema (Response)

Name | type | example | description
--------- | ------- | ----------- | -------


## Send Dynamic Price Example 2


It is the service that should be used to send a new reservation record. There is no need to enter any parameters when calling this service.

> Request:

```json
{
    "rooms": [
        {
            "room_code": "DLX-01",
            "channels": [
                "10", "11"
            ],
            "dates": [
                {
                    "date": "2024-12-01",
                    "price": "400",
                },
                {
                    "date": "2024-12-02",
                    "price": "410",
                }
            ]
        },
        ...
    ]
}
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
rooms  | Object  | 
room_code | String | DLX-01 | Room Type information
channels | String List | ["1", "2"]  | Channels information
dates | Object List
date | DateTime | 2024-12-01 | Date Information
price | Double | 400  | Price information


### Schema (Response)

Name | type | example | description
--------- | ------- | ----------- | -------

## Send Dynamic Price Example 3

It is the service that should be used to send a new reservation record. There is no need to enter any parameters when calling this service.

> Request:

```json
{
    "baslama_tarih": "2024-12-01",
    "bitis_tarih": "2024-12-02",
    "kanallar": ["10", "11"],
    "oda_tip_fiyatlar": [
        {
            "oda_tip_id": 21,
            "oda_tip_ad": "DLX_01",
            "fiyat": 400
        }
        ...
    ]
}
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
baslama_tarih  | DateTime  | 2024-12-01 | Başlangıç Tarihi
bitis_tarih  | DateTime  | 2024-12-02 | Bitiş Tarihi
kanallar  | String List  | ["10", "11"] | Kanal Bilgisi
oda_tip_fiyatlar  | Object List
oda_tip_id  | Integer  | 21 | Oda tipi id bilgisi
oda_tip_ad  | String  | DLX_01 | Oda tipi ad bilgisi
fiyat  | Double  | 400 | Oda fiyat bilgisi


### Schema (Response)

Name | type | example | description
--------- | ------- | ----------- | -------