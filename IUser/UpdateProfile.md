## Update User Profile Data

Updates the current user's public profile data.

#### HTTP Request

`POST https://api-trade.opskins.com/IUser/UpdateProfile/v1/`

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
display_name | string  | - | Name to display on trade offers
inventory_is_private | boolean | - | Whether inventory is private (nobody can see it, even with token)
allow_twofactor_code_reuse | boolean | - | Allow Two Factor code reuse for certain features (Send Offer, Accept Offer)
    
#### Output

Parameter | Type | Description
--------- | -----| -------- 
user     | object | [Standard User Profile Object](IUser.md#standard-user-profile-object)