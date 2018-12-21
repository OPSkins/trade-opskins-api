# ICase

Endpoints to handle cases

- [ICase/GetCaseSchema](ICase/GetCaseSchema.md)
- [ICase/GetCaseOdds](ICase/GetCaseOdds.md)
- [ICase/GetMinimumOpenVolume](ICase/GetMinimumOpenVolume.md)
- [ICase/OpenWithKeys](ICase/OpenWithKeys.md) (Disabled)

## Case Status

- STATE_ERROR = `1`
- STATE_PENDING = `2`
- STATE_OPENED = `3`

## Standard OpenedCase Object

Parameter | Type | Description
--------- | -----| -------- 
id | int | Unique Case ID
status | int | [Case Status](/ICase.md#case-status) ID
status_text | string | [Case Status](/ICase.md#case-status) Description
case_id | int | Case Schema ID
case_site_trade_offer_id | int | Trade Offer ID
referral_uid | int | Referral OPSkins UID
rebate_commission_rate | float | Rebate commission rate
item | object | [Standard Item Object](/IItem.md#standard-item-object)

## Example Output for Standard OpenedCase Object
```json
{
  "id": 1,
  "status": 3,
  "status_text": "Opened",
  "case_id": 1,
  "case_site_trade_offer_id": 3215,
  "referral_uid": 123,
  "rebate_commission_rate": 2.50,
  "item": {
  
  }
}
```
