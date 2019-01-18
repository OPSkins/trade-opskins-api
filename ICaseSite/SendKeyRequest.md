## Send Key Request

Sends a trade offer to the user requesting some number of keys for uncasing items on a case site.

- Ensure that `remaining_opens` for the case id is greater than 0 via `ICase/GetCaseSchema`, or you will get an HTTP 400 error with the code 314 (TOO_MANY_REDEMPTIONS).

- Case opening offers will be auto-accepted on behalf of users if they have accepted an offer from your site within the past 24 hours.

#### HTTP Request

`POST https://api-trade.opskins.com/ICaseSite/SendKeyRequest/v1`

#### Authentication

API key required.

- **Only accounts created with [IUser/CreateVCaseUser](/IUser/CreateVCaseUser.md) can access this endpoint.**

- **OPSkins User ID can be found on the WAX ExpressTrade [settings](https://trade.opskins.com/settings) page.**

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
`trade_url` or `steam_id` | string | + | The trade URL or the Steam ID64 of the user
case_id   | int  | + | The Case ID user wants to open
amount    | int  |  | Number of these cases that should be opened. Defaults to 1.
expiration_time | int | | Custom expiration time for the trade offer in `seconds`. Minimum 120 seconds (2 minutes). Defaults to 14 days.
message | string | | Trade offer message that will be displayed to the recipient
referral_uid | int | | (Optional) You can choose to send this if someone has referred someone else to your site. This should be an OPSkins UID (of the referrer). If this is set, when commission for the cases in this offer is distributed, commission will be split between your site, the referrer, and the case-opening user (rebate, if set below). You may set a custom split rate under [ICaseSite/UpdateCommissionSettings](/ICaseSite/UpdateCommissionSettings.md) with `referral_commission_rate`. If this is the same as `network_user_id` in [ICaseSite/UpdateCommissionSettings](/ICaseSite/UpdateCommissionSettings.md), the referral commission will be merged into the site's commission.
rebate_commission_rate | float | | (Optional) You can choose to share commission with the case-opening User. Default `0.00`%, Max `10.00`%, & Min `0.01`%. If this is set, when commission for the cases in this offer is distributed, commission will be split between your site, the User, and referrer (only if set). This works similarly to `referral_commission_rate` in [ICaseSite/UpdateCommissionSettings](/ICaseSite/UpdateCommissionSettings.md). If the case opening UID is the same as `referral_uid` above, referral commission will be merged into the rebate commission, or if it is the same as `network_user_id` in [ICaseSite/UpdateCommissionSettings](/ICaseSite/UpdateCommissionSettings.md), the rebate will be merged into the site's commission.

#### Output

Parameter | Type | Description
--------- | -----| -------- 
offer | object | [Standard Trade Offer Object](/ITrade.md#standard-trade-offer-object)
offer_url | string | Full URL to the trade offer. The recipient of this offer can click this link to view the offer and accept it.
