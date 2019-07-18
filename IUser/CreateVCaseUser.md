## Create a special case-website user

VCase Site users are restricted from most parts of the API.  They cannot own items or send regular trades.  But they gain access to a set of new API endpoints under the ICaseSite interface.

You generally only need to create a VCase Site API key once, which can be done with the following example CURL command.

`curl -d '{"site_url":"http://yoursite.com","display_name":"yoursite"}' -H "Content-Type: application/json" -X POST https://api-trade.wax.io/IUser/CreateVCaseUser/v1/`

#### HTTP Request

`POST https://api-trade.wax.io/IUser/CreateVCaseUser/v1/`

#### Authentication

No auth required.

**Creates a case-website user, which can access all endpoints under the [ICaseSite](/ICaseSite.md) interface.**

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
site_url | string | + | Must be a valid & unique full URL to your case-website.
display_name | string | + | Display name for case-website user.  This name will appear in all trade offers.

#### Output

Parameter | Type | Description
--------- | -----| -------- 
api_key | string | User API key. Keep it in a safe place and use it to access [ICaseSite](/ICaseSite.md) endpoints.
user | object | [Standard User Profile Object](/IUser.md#standard-user-profile-object) -- User ID will not be a matching OPSkins UID, it will be unique to WAX ExpressTrade and will be a negative integer.
