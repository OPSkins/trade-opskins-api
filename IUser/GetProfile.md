## Get current user's profile

#### HTTP Request

`GET https://api-trade.opskins.com/IUser/GetProfile/v1/`

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
with_extra | bool | - | Should we send sensitive user data? Defaults to `false`
    
#### Output

Parameter | Type | Description
--------- | -----| -------- 
user     | object | [Standard User Profile Object](IUser.md#standard-user-profile-object)