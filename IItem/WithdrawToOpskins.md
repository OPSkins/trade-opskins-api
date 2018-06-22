## Withdraw items to OPSkins on-site inventory.

#### HTTP Request

`POST https://api-trade.opskins.com/IItem/WithdrawToOpskins/v1/`

#### Authentication

API key required.

#### Input Descriptions

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
item_id| int-csv | + | item id filter, separated with comma

#### Output Descriptions
Parameter | Type | Description
--------- | ---- | -----------
results | object | Result from OPSkins API
output | object | Archived items
-uid | int | OPSkins UID
-items | object | Archived items
--appid | int | Steam App ID
--contextid | int | Steam Context ID
--market_name | string | Market name
--owner_uid | int | OPSkins UID
--wear | float | Wear float value
--original_sale_id | int | Original sale ID on OPSkins
