## Get user's trade offers

#### HTTP Request

`GET https://api-trade.opskins.com/ITrade/GetOffers/v1/`

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
uid | int |  - | ID of other user, involved in offers
state | string |  - | A comma-separated list of offer states to filter by (See available states in [ITrade](ITrade.md)). 
type | string |  - | One of `sent`, `received`
page | int | - | page number in response (starting with 1, default to 1) 
per_page | int | - | number of items per_page in response (no more then 100)
ids | int-csv | - | Trade offer IDs list filter
    
#### Output

Parameter | Type | Description
--------- | -----| -------- 
offer     | object    | [Standard Trade Offer Object](ITrade.md#standard-trade-offer-object)