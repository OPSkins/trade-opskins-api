# ICase

Endpoints to handle VGO keys & VGO cases

- [ICase/GetCaseSchema](ICase/GetCaseSchema.md)
- [ICase/GetMinimumOpenVolume](ICase/GetMinimumOpenVolume.md)
- [ICase/OpenWithKeys](ICase/OpenWithKeys.md)

## Case Status
```
1 = Error
2 = Pending
3 = Opened
```

## Standard OpenedCase Object

Parameter | Type | Description
--------- | -----| -------- 
id | int | Unique Case ID
status | int | [Case Status](/ICase.md#case-status) ID
status_text | string | [Case Status](/ICase.md#case-status) Description
case_id | int | Case Schema ID
case_site_trade_offer_id | int | Trade Offer ID
item | object | [Standard Item Object](/IItem.md#standard-item-object)

## Standard OpenedCase Object -- Example Output
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