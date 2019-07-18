## Withdraw items to OPSkins on-site inventory.

#### HTTP Request

`POST https://api-trade.wax.io/IItem/WithdrawToOpskins/v1/`

#### Authentication

API key required.

#### OAuth Scopes
`manage_items`

#### Input Descriptions

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
item_id| int-csv | + | item id filter, separated with comma

#### Output Descriptions
Parameter | Type | Description
--------- | ---- | -----------
results | object | Full result from internal OPSkins API call
output | object | Results from WAX ExpressTrade API
-uid | int | OPSkins UID
-items | object | Items transferred
--appid | int | Steam App ID
--contextid | int | Steam Context ID
--market_name | string | Market name
--owner_uid | int | OPSkins UID
--wear | float | Wear float value
--original_sale_id | int | Original sale ID on OPSkins (when deposited to WAX ExpressTrade)
