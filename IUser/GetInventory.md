## Get user's inventory.

#### HTTP Request

`GET https://api-trade.opskins.com/IUser/GetInventory/v1/`

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
app_id | int | - | Internal App ID (see [ITrade/GetApps](/ITrade/GetApps.md))
page | int | - | page number in response (starting with 1, default to 1) 
per_page | int | - | number of items per_page in response (no more then 100)
search | string | - | additional search by item's name 
sort | int | - | Code to set how results should be sorted. See available types below
    
#### Output

Parameter | Type | Description
--------- | -----| -------- 
total     | int    | Total number of items (filtered, if search parameter is passed)
items | array-object | items list, based on pagination and search filters. [Standard Item Object](/IItem.md#standard-item-object)
sort_parameters | array-object | Available sort parameters
--value | int | value, expected in this method
--display_name | string | Display name

#### Sort parameter values
- `1`: By name ASC
- `2`: By name DESC
- `3`: By last_update ASC
- `4`: By last_update DESC
- `5`: By suggested price ASC
- `6`: By suggested price DESC



