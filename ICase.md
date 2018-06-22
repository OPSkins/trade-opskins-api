# ICase

Endpoints to handle cases

- [ICase/GetCaseSchema](ICase/GetCaseSchema.md)
- [ICase/GetMinimumOpenVolume](ICase/GetMinimumOpenVolume.md)
- [ICase/OpenWithKeys](ICase/OpenWithKeys.md)

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
item | object | [Standard Item Object](/IItem.md#standard-item-object)

## Example Output for Standard OpenedCase Object
```json
{
  "id": 1,
  "status": 3,
  "status_text": "Opened",
  "case_id": 1,
  "case_site_trade_offer_id": 3215,
  "item": {
  
  }
}
```