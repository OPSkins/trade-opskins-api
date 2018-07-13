## Get trade offer recipient's inventory.

#### HTTP Request

`GET https://api-trade.opskins.com/ITrade/GetUserInventory/v1/`

#### Authentication

None required.

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
uid | int | + | User ID of user whose inventory you want to see 
app_id | int | + | Internal App ID (see [ITrade/GetApps](/ITrade/GetApps.md))
page | int |   | Page number in response (starting with 1, defaults to 1) 
per_page | int |   | Number of items per_page in response (no more than 100)
search | string |   | Additional search by item's name 
    
#### Output

Parameter | Type | Description
--------- | -----| -------- 
total     | int    | Total number of items (filtered, if search parameter is passed)
items | object | [Standard Item Object](/IItem.md#standard-item-object)
user_data | object | [Standard User Public Profile Object](/IUser.md#standard-user-public-profile-object)



