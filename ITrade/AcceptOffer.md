## Accepts offer sent by another user

#### HTTP Request

`POST https://api-trade.opskins.com/ITrade/AcceptOffer/v1/`

#### Authentication

API key required.

#### OAuth Scopes
`trades`

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
twofactor_code | string | + | 2-factor authentication code
offer_id | int | + | Trade offer Id you want to accept

    
#### Output

Parameter | Type | Description
--------- | -----| -------- 
offer     | object    | [Standard Trade Offer Object](/ITrade.md#standard-trade-offer-object)
new_items | array-object | New items for the recipient (the user that makes this API call). [Standard Item Object](/IItem.md#standard-item-object)
failed_cases | int | A count of failed case openings, `0` if none failed.
