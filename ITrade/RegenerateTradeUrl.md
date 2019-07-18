## Regenerate your account's trade URL for P2P trading, invalidating the old one.

#### HTTP Request

`POST https://api-trade.wax.io/ITrade/RegenerateTradeURL/v1/`

#### Authentication

API key required.

#### OAuth Scopes
`edit_account`

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
_none_ | | | 
    
#### Output

Parameter | Type | Description
--------- | -----| -------- 
uid       | int    | Your OPSkins User ID
token     | string | Your new trade token
long_url  | string | The actual URL someone should go to in order to send a trade offer to your account.
short_url | string | A shortened alias for `long_url` of the type ".../t/1/Lhn9d7fVL1U". This redirects to the long URL. 

