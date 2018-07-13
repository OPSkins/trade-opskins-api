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
`referral_commission_rate` | float  |  | (Optional, default is `5.00` (%)) How many percent commission referrers should receive from your cut. Max 5.00 (%) and Min 0.01 (%).

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