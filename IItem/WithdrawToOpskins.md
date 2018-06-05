## Withdraw items to OPSkins on-site inventory.

#### HTTP Request

`POST https://api-trade.opskins.com/IItem/WithdrawToOpskins/v1/`

#### Input Descriptions

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
item_id| int-csv | - | item id filter, separated with comma

#### Output Descriptions
Parameter | Type | Description
--------- | ---- | -----------
results | idk | Result from OPSkins API
output | object | Archived items
 - owner_uid | int | Owner UID
 - trade_items | object | Archived Items
 