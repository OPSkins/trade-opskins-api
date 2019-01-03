## Get All Item Definitions

#### HTTP Request

`GET https://api-trade.opskins.com/IItem/GetItemDefinitions/v1/`

- All items for an app (limit `1000` per page): `GetItemDefinitions/v1?app_id=1`
- Filter by `def_id`: `GetItemDefinitions/v1?app_id=1&def_id_filter=900000001,900000002`

#### Authentication

None required.

#### Input Descriptions

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
app_id | int | + | Internal App ID (see [ITrade/GetApps](/ITrade/GetApps.md))
def_id_filter | csv-int |  | Optional `def_id` comma-separated filter
index_by | string | | Optionally index the output by `market_name`, `def_id`, or `sku`, send it as literal string
page | int |  | Page number in response (starting with 1, defaults to 1) 
per_page | int | | Number of items per_page in response (no more than `1000` (default))

#### Output Descriptions

Parameter | Type | Description
--------- | ---- | -----------
definitions | array-object or object | An array of objects or object list if `index_by` option is used
--def_id | int | Unique Definition ID, this is a unique & unchanging identifier for each item, regardless of `app_id`. Not to be confused with `sku`, which is *not unique per wear-tier* for VGO items. VGO item `def_id` starts at `900,000,000` for no particular reason.
--sku | int | SKU for item. Mainly utilized for VGO items, for all other items, this will be the same as `def_id`.
--internal_app_id | int | Internal App ID
--name | string | Name, non-unique, most likely the same as `market_name` however
--market_name | string | Market name, unique per `app_id`
--color | string | Color with hex # for VGO (ID 1), for all others, no # 🙁 -- usually corresponds to the `rarity` of the item
--image | string | Generic image URL
--suggested_price | int | Market suggested price
--suggested_price_floor | int | The minimum viable suggested price, does not change.
--attributes | object | Generic (non-unique) item attributes, all app-specific properties will be in here

#### Output Example
- Array of objects:
```json
{
    "status": 1,
    "time": 1544467201,
    "current_page": 1,
    "total_pages": 1,
    "response": {
        "definitions": [
            {
                "def_id": 900000001,
                "internal_app_id": 1,
                "name": "WAX Key",
                "market_name": "WAX Key",
                "color": "#777777",
                "image": "https://files.opskins.media/file/vgo-img/item/wax-key-300.png",
                "suggested_price": 250,
                "suggested_price_floor": 250,
                "attributes": {
                    "category": "WAX Key",
                    "image_generic_300": "https://files.opskins.media/file/vgo-img/item/wax-key-300.png",
                    "image_generic_600": "https://files.opskins.media/file/vgo-img/item/wax-key-600.png",
                    "image_generic_900": "https://files.opskins.media/file/vgo-img/item/wax-key-900.png",
                    "image_generic_1800": "https://files.opskins.media/file/vgo-img/item/wax-key-1800.png",
                    "image_generic_2500": "https://files.opskins.media/file/vgo-img/item/wax-key-2500.png",
                    "paint_index": null,
                    "rarity": null,
                    "suggested_price_floor": 250,
                    "type": "WAX Key",
                    "wear_tier_index": 0
                }
            }
        ]
    }
}
```

- Indexed by `def_id`:

```json
{
    "status": 1,
    "time": 1544467222,
    "current_page": 1,
    "total_pages": 1,
    "response": {
        "definitions": {
            "900000001": {
                "def_id": 900000001,
                "internal_app_id": 1,
                "name": "WAX Key",
                "market_name": "WAX Key",
                "color": "#777777",
                "image": "https://files.opskins.media/file/vgo-img/item/wax-key-300.png",
                "suggested_price": 250,
                "suggested_price_floor": 250,
                "attributes": {
                    "category": "WAX Key",
                    "image_generic_300": "https://files.opskins.media/file/vgo-img/item/wax-key-300.png",
                    "image_generic_600": "https://files.opskins.media/file/vgo-img/item/wax-key-600.png",
                    "image_generic_900": "https://files.opskins.media/file/vgo-img/item/wax-key-900.png",
                    "image_generic_1800": "https://files.opskins.media/file/vgo-img/item/wax-key-1800.png",
                    "image_generic_2500": "https://files.opskins.media/file/vgo-img/item/wax-key-2500.png",
                    "paint_index": null,
                    "rarity": null,
                    "suggested_price_floor": 250,
                    "type": "WAX Key",
                    "wear_tier_index": 0
                }
            },
            "900000002": {
                "def_id": 900000002,
                "internal_app_id": 1,
                "name": "AK-47 | Overdrive (Factory New)",
                "market_name": "AK-47 | Overdrive (Factory New)",
                "color": "#eb4b4b",
                "image": "https://files.opskins.media/file/vgo-img/item/ak-47-overdrive-factory-new-300.png",
                "suggested_price": 23252,
                "suggested_price_floor": 23252,
                "attributes": {
                    "category": "Covert Rifle",
                    "image_generic_300": "https://files.opskins.media/file/vgo-img/item/ak-47-overdrive-factory-new-300.png",
                    "image_generic_600": "https://files.opskins.media/file/vgo-img/item/ak-47-overdrive-factory-new-600.png",
                    "image_generic_900": "https://files.opskins.media/file/vgo-img/item/ak-47-overdrive-factory-new-900.png",
                    "image_generic_1800": "https://files.opskins.media/file/vgo-img/item/ak-47-overdrive-factory-new-1800.png",
                    "image_generic_2500": "https://files.opskins.media/file/vgo-img/item/ak-47-overdrive-factory-new-2500.png",
                    "paint_index": null,
                    "rarity": "Covert",
                    "suggested_price_floor": 23252,
                    "type": "Rifle",
                    "wear_tier_index": 1
                }
            }
        }
    }
}
```
