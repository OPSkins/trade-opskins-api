## Cancels a trade offer

If cancelled by the sender it will go into `STATE_CANCELLED` (6) and if cancelled by the receiver it will go into `STATE_DECLINED` (7).

#### HTTP Request

`POST https://api-trade.opskins.com/ITrade/CancelOffer/v1/`

#### Authentication

API key required.

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
offer_id | int |  + | Offer ID that you're a party to (sender or receiver)

    
#### Output

Parameter | Type | Description
--------- | -----| -------- 
offer     | object    | [Standard Trade Offer Object](/ITrade.md#standard-trade-offer-object)
