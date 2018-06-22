## Send Key Request

Sends a trade offer to the user requesting some number of keys for uncasing items on a case website.

#### HTTP Request

`POST https://api-trade.opskins.com/ICaseSite/SendKeyRequest/v1`

#### Authentication

API key required.

**Only accounts created with [IUser/CreateVCaseUser](/IUser/CreateVCaseUser.md) can access this endpoint.**

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
`trade_url` or `steam_id` | string | + | The trade URL or the Steam ID64 of the user
case_id   | int  | + | The Case ID user wants to open
affiliate_eth_address | string | + | The eth address that should receive the commission when the items are uncased.
amount    | int  |  | Number of these cases that should be opened. Defaults to 1.

#### Output

Parameter | Type | Description
--------- | -----| -------- 
offer | object | [Standard Trade Offer Object](/ITrade.md#standard-trade-offer-object)
offer_url | string | Full URL to the trade offer. The recipient of this offer can click this link to view the offer and accept it.