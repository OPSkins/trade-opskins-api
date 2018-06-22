## Create a special case-website user

#### HTTP Request

`GET https://api-trade.opskins.com/IUser/CreateVCaseUser/v1/`

#### Authentication

No auth required.

**Creates a case-website user, which can access all endpoints under the [ICaseSite](/ICaseSite.md) interface.**

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
site_url | string | + | Must be a valid & unique full URL to your case-website.
display_name | string | + | Display name for case-website user.

#### Output

Parameter | Type | Description
--------- | -----| -------- 
api_key | string | User API key. Keep it in a safe place and use it to access [ICaseSite](/ICaseSite.md) endpoints.
user | object | [Standard User Profile Object](/IUser.md#standard-user-profile-object) -- User ID will not be a matching OPSkins UID, it will be unique to WAX ExpressTrade and will be a negative integer.