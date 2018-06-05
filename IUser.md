## IUser

- [IUser/GetInventory](IUser/GetInventory.md)
- [IUser/GetProfile](IUser/GetProfile.md)
- [IUser/UpdateProfile](IUser/UpdateProfile.md)


## Standard User Profile Object

Parameter | Type | Description
--------- | -----| -------- 
user     | object | Holds user info
--id | int | OPSkins.com User ID
--steam_id | string | Steam ID64
--display_name | string | Display name
--avatar | string | URL to avatar
--twofactor_enabled | boolean | Whether or not user has Two-Factor Auth enabled.
--api_key_exists | boolean | See whether user has API Key
--sms_phone | string/null | (Optional via `with_extra`) Phone number used for SMS verification
--contact_email | string/null | (Optional via `with_extra`) Email address
--inventory_is_private | boolean | (Optional via `with_extra`) Set whether inventory is private (nobody can see it, even with token)
- allow_twofactor_code_reuse | boolean | Allow Two Factor code reuse for certain features (Send Offer, Accept Offer)

## Standard User Public Profile Object

Parameter | Type | Description
--------- | -----| -------- 
user_data | object | Holds user info
--username | string | Display name
--avatar | string | URL to avatar
