## Get Your Inventory

#### HTTP Request

`GET https://api-trade.opskins.com/IUser/GetInventory/v1/`

#### Authentication

API key required.

#### OAuth Scopes
`items`, `trades`

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
app_id | int | + | Internal App ID (see [ITrade/GetApps](/ITrade/GetApps.md))
page | int |  | Page number in response (starting with 1, defaults to 1) 
per_page | int | | Number of items per_page in response (no more than 500)
search | string | | Additional search by item's name 
sort | int |  | Code to set how results should be sorted. See available types below
filter_in_trade | boolean | | Removes items that are part of an active trade from the response.
    
#### Output

Parameter | Type | Description
--------- | -----| -------- 
total     | int    | Total number of items (filtered, if search parameter is passed)
items | array-object | Items list, based on pagination and search filters. [Standard Item Object](/IItem.md#standard-item-object)
sort_parameters | array-object | Available sort parameters
items_in_active_offers | object-array | List of Item IDs and matching Offer IDs that are involved in active trade offers. Keys are Item IDs and values are an array of Offer IDs.
--value | int | Value expected in this method
--display_name | string | Display name

#### Sort parameter values
- `1`: By name ASC (alphabetical, `z` first)
- `2`: By name DESC (alphabetical, `a` first)
- `3`: By last_update ASC (oldest first)
- `4`: By last_update DESC (newest first)
- `5`: By suggested price ASC (lowest first)
- `6`: By suggested price DESC (highest first)



