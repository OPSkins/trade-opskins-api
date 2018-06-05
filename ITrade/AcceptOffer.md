## Accepts offer sent by another user

#### HTTP Request

`POST https://api-trade.opskins.com/ITrade/AcceptOffer/v1/`

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
twofactor_code | string | + | 2-factor authentication code
offer_id | int | + | Trade offer Id you want to accept

    
#### Output

Parameter | Type | Description
--------- | -----| -------- 
offer     | object    | [Standard Trade Offer Object](/ITrade.md#standard-trade-offer-object)
new items | array-object | items, new for the recipient (user that makes this API call). [Standard Item Object](/IItem.md#standard-item-object)