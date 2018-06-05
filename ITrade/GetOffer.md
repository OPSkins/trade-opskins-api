## Get an individual trade offer

You must be one of the parties involved in the offer (sender/receiver).

#### HTTP Request

`GET https://api-trade.opskins.com/ITrade/GetOffer/v1/`

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
offer_id | int |  + | ID of trade offer

#### Output

Parameter | Type | Description
--------- | -----| -------- 
offer     | object    | [Standard Trade Offer Object](ITrade.md#standard-trade-offer-object)