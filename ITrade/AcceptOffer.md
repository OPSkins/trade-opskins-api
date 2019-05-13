## Accepts offer sent by another user

#### HTTP Request

`POST https://api-trade.opskins.com/ITrade/AcceptOffer/v1/`

#### Authentication

API key required.

#### OAuth Scopes
- `trades`
- `open_cases` (restricted to only case-opening offers)

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
twofactor_code | int |  | 2-factor authentication code -- This is required if you're using OAuth and do not have `TRADES_NO_2FA` scope, or if you're authenticated on the front-end via cookies.  Not required when using an API Key to authenticate.
offer_id | int | + | Trade offer Id you want to accept

    
#### Output

Parameter | Type | Description
--------- | -----| -------- 
offer     | object    | [Standard Trade Offer Object](/ITrade.md#standard-trade-offer-object)
new_items | array-object | New items for the recipient (the user that makes this API call). [Standard Item Object](/IItem.md#standard-item-object)
failed_cases | int | A count of failed case openings, `0` if none failed.
