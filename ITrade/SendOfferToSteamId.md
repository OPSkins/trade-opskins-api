   ## Sends trade offer to another user, including your and their items

#### HTTP Request

`POST https://api-trade.wax.io/ITrade/SendOfferToSteamId/v1/`

#### Authentication

API key required.

#### OAuth Scopes
`trades`

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
twofactor_code | int |  | 2-factor authentication code -- This is required if you're using OAuth and do not have `TRADES_NO_2FA` scope, or if you're authenticated on the front-end via cookies.  Not required when using an API Key to authenticate.
steam_id | string | + | Steam ID of user you want to send your trade offer to
items_to_send | csv-int | | A comma-separated list of (int) Item IDs you wish to send to recipient. Maximum `400` items.
items_to_receive | csv-int | | A comma-separated list of (int) Item IDs you wish to receive from the recipient. Maximum `400` items.
expiration_time | int | | Custom expiration time for an offer in `seconds`. Minimum 120 seconds (2 minutes). Defaults to 14 days.
message | string | | An optional message to include with your trade offer, up to 190 characters.
    
#### Output

Parameter | Type | Description
--------- | -----| -------- 
offer     | object    | [Standard Trade Offer Object](/ITrade.md#standard-trade-offer-object)
