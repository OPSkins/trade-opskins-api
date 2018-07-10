## Get Key Count

Returns the number of keys a specific user has on ExpressTrade

#### HTTP Request

`GET https://api-trade.opskins.com/ICaseSite/GetKeyCount/v1`

#### Authentication

API key required.

**Only accounts created with [IUser/CreateVCaseUser](/IUser/CreateVCaseUser.md) can access this endpoint.**

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
`trade_url` or `steam_id` | string | + | The trade URL or the Steam ID64 of the user 
    
#### Output

Parameter | Type | Description
--------- | -----| -------- 
key_count | string  | Number of keys this user owns.  Parsable into an int.
