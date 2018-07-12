## Link Third Party Account

Link a third party account to your VCaseUser, currently only used for distribution of commission. Link your OPSkins.com account to receive commission directly into your OPSkins.com wallet.

#### HTTP Request

`POST https://api-trade.opskins.com/ICaseSite/LinkThirdPartyAccount/v1`

#### Authentication

API key required.

**Only accounts created with [IUser/CreateVCaseUser](/IUser/CreateVCaseUser.md) can access this endpoint.**

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
`twofactor_code` | int | + | Two-Factor Authentication code.
`third_party_id` | int | + | The ID of the third party. `1` for OPSkins.com
`third_party_user_identifier` | int  | + | User identifier for the third party. If for OPSkins, your OPSkins User ID.

**You can find your OPSkins User ID on the WAX ExpressTrade [settings](https://trade.opskins.com/settings) page.**

#### Output

Parameter | Type | Description
--------- | -----| -------- 
`third_party_id` | int | Returns current database value (should be same as input).
`third_party_user_identifier` | int  | Returns current database value (should be same as input).

#### Output Example
```json
{
    "status": 1,
    "time": 1531351121,
    "response": {
        "third_party_id": 1,
        "third_party_user_identifier": 1234567891
    }
}
```