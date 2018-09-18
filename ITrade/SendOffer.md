## Sends trade offer to another user including your and their items

#### HTTP Request

`POST https://api-trade.opskins.com/ITrade/SendOffer/v1/`

#### Authentication

API key required.

#### Input

One of: `uid` + `token` **or** `trade_url` is required.

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
twofactor_code | string | + | 2-factor authentication code
uid | int | | User ID of user you want to send your trade offer to
token | string | | Trade token of user you want to send your trade offer to
trade_url | string | | Trade URL of the user you want to send your trade offer to.
items | string | + | A comma-separated list of item ids you wish to include in trade offer. There should be both yours and recipients items. 100 maximum per each side.
message | string | | Trade offer message that will be displayed to the recipient
expiration_time | int | | Custom expiration time for an offer in `seconds`. Minimum 120 seconds (2 minutes). Defaults to 14 days.

> **Note: items is turned into array with unique values.  If you pass `1,2,3,3,3,4` we will interpret it as `1,2,3,4` without failure.**
    
#### Output

Parameter | Type | Description
--------- | -----| -------- 
offer     | object    | [Standard Trade Offer Object](/ITrade.md#standard-trade-offer-object)
