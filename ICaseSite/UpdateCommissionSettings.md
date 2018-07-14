## Update Commission Settings

Update commission settings for your VCaseUser.

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
`referral_commission_rate` | float  |  | (Optional, default is `5.00` %) How many percent commission referrers should receive from total commission percentage (currently 5.00%). Max 5.00 (%) and Min 0.01 (%). The 'referrer' is `referral_uid` (OPSkins UID), which can be sent when sending [ICaseSite/SendKeyRequest](/ICaseSite/SendKeyRequest.md). For example, if this is set to `2.50` %, you will get `$0.07` and the referrer `$0.06`, as the total commission amount (for each case) is 5% of a Skeleton Key, which is `$0.13`. So by default (5.00%), the referrer will get all the commission `$0.13`.

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
