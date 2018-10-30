## Get All Items

#### HTTP Request

`GET https://api-trade.opskins.com/IItem/GetAllItems/v1/`

#### Authentication

API key required.

#### Input Descriptions

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
app_id | int | + | Internal App ID (see [ITrade/GetApps](/ITrade/GetApps.md))
sku | csv-int | | Optional filtering by SKU
page | int | | Page number (starting with `1`, defaults to `1`) 
per_page | int | | Number of items per page (default `25`, max `100`, min `1`)
sort | int |  | [Standard Item Sorts](/IItem.md#standard-item-sorts)
no_exclusions | boolean | | By default some items are excluded, [see list below](/IItem/GetAllItems.md#default-excluded-skus). Sending `1` here will disable all SKU exclusions.

##### Default Excluded SKUs
- VGO `1`
    - `1` (WAX Key)

#### Output Descriptions
Parameter | Type | Description
--------- | ---- | -----------
items | array-object | Array of [Standard Item Object](/IItem.md#standard-item-object)

#### Output Example
```json
{
    "status": 1,
    "time": 1538684115,
    "current_page": 1,
    "total_pages": 9,
    "response": {
        "items": [
            {
                "id": 911,
                "sku": 10011,
                "wear": 0.01472946,
                "pattern_index": 362,
                "preview_urls": null,
                "eth_inspect": null,
                "trade_hold_expires": null,
                "internal_app_id": 1,
                "inspect": null,
                "tradable": true,
                "attributes": {
                    "serial_sku": 6,
                    "serial_sku_wear": 6
                },
                "name": "Bayonet | Poison Target (Factory New)",
                "category": "Covert Knife",
                "rarity": "Covert",
                "type": "Knife",
                "paint_index": null,
                "color": "#eb4b4b",
                "image": {
                    "300px": "https://files.opskins.media/file/vgo-img/item/bayonet-poison-target-factory-new-300.png",
                    "600px": "https://files.opskins.media/file/vgo-img/item/bayonet-poison-target-factory-new-600.png"
                },
                "suggested_price": 14000,
                "suggested_price_floor": 14000,
                "wear_tier_index": 1
            },
            {
                "id": 910,
                "sku": 106,
                "wear": 0.17418098,
                "pattern_index": 769,
                "preview_urls": null,
                "eth_inspect": null,
                "trade_hold_expires": null,
                "internal_app_id": 1,
                "inspect": null,
                "tradable": true,
                "attributes": {
                    "serial_sku": 78,
                    "serial_sku_wear": 44
                },
                "name": "P90 | Critical (Field-Tested)",
                "category": "Restricted SMG",
                "rarity": "Restricted",
                "type": "SMG",
                "paint_index": null,
                "color": "#8847ff",
                "image": {
                    "300px": "https://files.opskins.media/file/vgo-img/item/p90-critical-field-tested-300.png",
                    "600px": "https://files.opskins.media/file/vgo-img/item/p90-critical-field-tested-600.png"
                },
                "suggested_price": 121,
                "suggested_price_floor": 121,
                "wear_tier_index": 3
            }
        ]
    }
}
```
