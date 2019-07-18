## Update Your Profile

#### HTTP Request

`POST https://api-trade.wax.io/IUser/UpdateProfile/v1/`

#### Authentication

API key required.

#### OAuth Scopes
`edit_account`

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
display_name | string  |  | Name to display on trade offers
inventory_is_private | boolean |  | Whether inventory is private (nobody can see it, even with token)
allow_twofactor_code_reuse | boolean |  | Allow Two Factor code reuse for certain features (Send Offer, Accept Offer)
auto_accept_gift_trades | boolean | | Auto-accept gift trade offers
anonymous_transactions | boolean | | Hide my username in WAX transaction records
    
#### Output

Parameter | Type | Description
--------- | -----| -------- 
user     | object | [Standard User Profile Object](/IUser.md#standard-user-profile-object)
