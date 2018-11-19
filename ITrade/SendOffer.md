## Sends trade offer to another user including your and their items

#### HTTP Request

`POST https://api-trade.opskins.com/ITrade/SendOffer/v1/`

#### Authentication

API key required.

#### OAuth Scopes
`trades`

#### Input

One of: `uid` + `token` **or** `trade_url` is required.

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
twofactor_code | int | + | 2-factor authentication code
uid | int | | User ID of user you want to send your trade offer to
token | string | | Trade token of user you want to send your trade offer to
trade_url | string | | Trade URL of the user you want to send your trade offer to.
items_to_send | csv-int | | A comma-separated list of (int) Item IDs you wish to send to recipient. Maximum `100` items.
items_to_receive | csv-int | | A comma-separated list of (int) Item IDs you wish to receive from the recipient. Maximum `100` items.
expiration_time | int | | Custom expiration time for an offer in `seconds`. Minimum 120 seconds (2 minutes). Defaults to 14 days.
message | string | | Trade offer message that will be displayed to the recipient
    
#### Output

Parameter | Type | Description
--------- | -----| -------- 
offer     | object    | [Standard Trade Offer Object](/ITrade.md#standard-trade-offer-object)
