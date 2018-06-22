## Get Trade Status

Returns the Trade Status and Opened Case results from an offer created by a case website.

#### HTTP Request

`GET https://api-trade.opskins.com/ICaseSite/GetTradeStatus/v1`

#### Authentication

API key required.

**Only accounts created with [IUser/CreateVCaseUser](/IUser/CreateVCaseUser.md) can access this endpoint.**

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
offer_id  | int  | + | The trade offer ID that was created by the requesting user.

#### Output

Parameter | Type | Description
--------- | -----| -------- 
offer    | object | [Standard Trade Offer Object](/ITrade.md#standard-trade-offer-object)
cases    | object | [Standard OpenedCase Object](/ICase.md#standard-openedcase-object)