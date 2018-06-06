# IItem

- [IItem/GetItemsById](IItem/GetItemsById.md)
- [IItem/WithdrawToOpskins](IItem/WithdrawToOpskins.md)

## Standard Item Object

Parameter | Type | Description
--------- | -----| -------- 
id | int | Item ID
internal_app_id | int | Trade/Internal App ID (see [ITrade/GetApps](/ITrade/GetApps.md))
sku | int | Item definition (meta-data) SKU #
wear | float | Wear float value, only applicable for certain apps
trade_hold_expires | int / null | Trade hold expiration date. `null` if no trade hold
name | string | Market name
category | string | Category name e.g. "Restricted Rifle"
color | string | Color hex #
image | object | Generic image URLs
--300px | string | 300px image URL
--600px | string | 600px image URL
suggested_price | int | OPSkins 7-day suggested price (US cents)
preview_urls | object | Instant Field Inspection™ URLs.
inspect | string / null | Steam inspection URL. Can be `null`.
eth_inspect | string / null | Etherscan.io Ethereum Transaction URL. `null` for inapplicable apps.
pattern_index | int | Pattern index (value between 1-1000) (only available for App ID `1`, `null` for other apps)
wear_tier | string | Wear tier title (only outputted for App ID `1`)
paint_index | int | Paint index value for a CS:GO item (property __not outputted__ for App ID `1`). Is `0` for items without a paint-index.
