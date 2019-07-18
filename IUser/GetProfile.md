## Get Your Profile

#### HTTP Request

`GET https://api-trade.wax.io/IUser/GetProfile/v1/`

#### Authentication

API key required.

#### OAuth Scopes
`identity_basic`, `identity`

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
with_extra | bool |  | Should we send sensitive user data? Defaults to `false`
    
#### Output

Parameter | Type | Description
--------- | -----| -------- 
user     | object | [Standard User Profile Object](/IUser.md#standard-user-profile-object)
