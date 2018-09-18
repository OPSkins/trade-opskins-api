   ## Sends trade offer to another user, including your and their items

#### HTTP Request

`POST https://api-trade.opskins.com/ITrade/SendOfferToSteamId/v1/`

#### Authentication

API key required.

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
twofactor_code | int | + | 2FA Auth Code
steam_id | int | + | Steam ID of user you want to send your trade offer to
items | string | + | A comma-separated list of item ids you wish to include in trade offer. There should be both yours and recipients items. 200 maximum per each side.
message | string | | An optional message to include with your trade offer, up to 190 characters.

> **Note: items is turned into array with unique values.  If you pass `1,2,3,3,3,4` we will interpret it as `1,2,3,4` without failure.**

    
#### Output

Parameter | Type | Description
--------- | -----| -------- 
offer     | object    | [Standard Trade Offer Object](/ITrade.md#standard-trade-offer-object)
