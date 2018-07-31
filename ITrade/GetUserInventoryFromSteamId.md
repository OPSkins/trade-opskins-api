## Get trade offer recipient's inventory.

#### HTTP Request

`GET https://api-trade.opskins.com/ITrade/GetUserInventoryFromSteamId/v1/`

#### Authentication
API key required.

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
steam_id | int |  + | Steam ID of user whose inventory you want to see 
app_id | int | + | Internal App ID (see [ITrade/GetApps](/ITrade/GetApps.md))
page | int |  | Page number in response (starting with 1, default to 1) 
per_page | int |  | Number of items per_page in response (no more than 500)
search | string |  | Additional search by item's name 
sort | int |  | Code to set how results should be sorted. See available types below or in the output response
    
#### Output

Parameter | Type | Description
--------- | -----| -------- 
total     | int    | Total number of items (filtered, if search parameter is passed)
items | object | [Standard Item Object](/IItem.md#standard-item-object)
user_data | object | [Standard User Public Profile Object](/IUser.md#standard-user-public-profile-object)
sort_parameters | array-object | Available sort parameters

#### Sort parameter values
- `1`: By name ASC (alphabetical, `z` first)
- `2`: By name DESC (alphabetical, `a` first)
- `3`: By last_update ASC (oldest first)
- `4`: By last_update DESC (newest first)
- `5`: By suggested price ASC (lowest first)
- `6`: By suggested price DESC (highest first)
