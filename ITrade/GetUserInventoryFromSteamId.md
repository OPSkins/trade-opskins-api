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
page | int |  | page number in response (starting with 1, default to 1) 
per_page | int |  | number of items per_page in response (no more then 100)
search | string |  | additional search by item's name 
    
#### Output

Parameter | Type | Description
--------- | -----| -------- 
total     | int    | Total number of items (filtered, if search parameter is passed)
items | object | 
user_data | object | [Standard User Public Profile Object](/IUser.md#standard-user-public-profile-object)

