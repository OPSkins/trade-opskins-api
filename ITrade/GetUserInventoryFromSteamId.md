## Get trade offer recipient's inventory.

#### HTTP Request

`GET https://api-trade.wax.io/ITrade/GetUserInventoryFromSteamId/v1/`

#### Authentication
API key required.

#### OAuth Scopes
`items`, `trades`

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
steam_id | string |  + | Steam ID of user whose inventory you want to see 
app_id | int | + | Internal App ID (see [ITrade/GetApps](/ITrade/GetApps.md))
page | int |  | Page number in response (starting with 1, default to 1) 
per_page | int |  | Number of items per_page in response (no more than 500)
search | string |  | Additional search by item's name 
sort | int |  | [Standard Item Sorts](/IItem.md#standard-item-sorts)
    
#### Output

Parameter | Type | Description
--------- | -----| -------- 
total     | int    | Total number of items (filtered, if search parameter is passed)
items | object | [Standard Item Object](/IItem.md#standard-item-object)
user_data | object | [Standard User Public Profile Object](/IUser.md#standard-user-public-profile-object)
sort_parameters | array-object | Available sort parameters
