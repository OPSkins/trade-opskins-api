## Sends trade offer to another user including your and their items

#### HTTP Request

`POST https://api-trade.opskins.com/ITrade/SendOffer/v1/`

#### Authentication

API key required.

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
twofactor_code | string | + | 2-factor authentication code
uid | int | + | User ID of user you want to send your trade offer to
token | string | + | Trade token of user you want to send your trade offer to
items | string | + | A comma-separated list of item ids you wish to include in trade offer. There should be both yours and recipients items. 100 maximum per each side.
message | string | | Trade offer message that will be displayed to the recipient

    
#### Output

Parameter | Type | Description
--------- | -----| -------- 
offer     | object    | [Standard Trade Offer Object](/ITrade.md#standard-trade-offer-object)
