## Update Commission Settings

Update commission settings for your VCaseUser. Link your OPSkins account to receive commission directly into your USD Wallet.

#### HTTP Request

`POST https://api-trade.opskins.com/ICaseSite/UpdateCommissionSettings/v1`

#### Authentication

API key required.

**Only accounts created with [IUser/CreateVCaseUser](/IUser/CreateVCaseUser.md) can access this endpoint.**

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
`network_id` | int | + | The ID of the network. `1` for OPSkins.com
`network_user_id` | int  | + | User ID on the network. For OPSkins, your OPSkins User ID.
`referral_commission_rate` | float  |  | **OPTIONAL! Want all the commission? Don't worry about this. This only matters if you send `referral_uid` with `ICaseSite/SendKeyRequest`.** Want to share commission with referring users? This property is how many percent commission referrers should receive from total commission percentage (currently `10.00`%). Default `5.00`%, Max `10.00`%, & Min `0.01`%. The 'referrer' is `referral_uid` (OPSkins UID), which can be sent when sending [ICaseSite/SendKeyRequest](/ICaseSite/SendKeyRequest.md). You have to get this from the user (they have to provide to you) and then you can send it. For example, if this is set to `5.00` %, you will get `$0.13` and the referrer `$0.12`, as the total commission amount (for each case) is 10% of a WAX Key, which is `$0.25`. So by default (`5.00`%), the referrer will get half the commission `$0.12`.

**You can find your OPSkins User ID on the WAX ExpressTrade [settings](https://trade.opskins.com/settings) page.**

#### Output

Parameter | Type | Description
--------- | -----| -------- 
`network_id` | int | Returns database value (should be same as input).
`network_user_id` | int  | Returns database value (should be same as input).
`referral_commission_rate` | float | Returns database value (should be same as input).

#### Output Example
```json
{
    "status": 1,
    "time": 1531449864,
    "response": {
        "network_id": 1,
        "network_user_id": 1234567891,
        "referral_commission_rate": 2.5
    }
}
```
