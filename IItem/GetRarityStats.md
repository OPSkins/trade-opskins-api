## Get item rarity stats per Definition ID (SKU) (currently only for VGO)

#### HTTP Request

`GET https://api-trade.opskins.com/IItem/GetRarityStats/v1?key=apikey&app_id=1&sku=100`

#### Authentication

API key required.

#### Input Descriptions

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
app_id | int | + | Internal App ID (see [ITrade/GetApps](/ITrade/GetApps.md))
def_id | int-csv | + | Definition IDs (SKUs) separated by commas

**Note: If an item was never unboxed yet (very rare items), no stats will be outputted.** 

#### Output Descriptions
Parameter | Type | Description
--------- | ---- | -----------
items | object | Object containing rarity data per Definition ID
--(def_id) | string | Definition ID (same as `item_def_id`)
----item_def_id | int | Definition ID
----item_def_sub_id | int/null | Sub-Definition ID, for VGO this is the Wear Tier Index (1,2,3,4,5)
----latest_serial | int | The latest serial number (per Def ID only) given for an item of this type.
----sub_items | object | Object containing rarity data per Definition ID & Sub Definition ID
------(def_sub_id) | string | Sub-Definition ID (same as `item_def_sub_id`)
--------item_def_id | int | Definition ID
--------item_def_sub_id | int | Sub-Definition ID
--------latest_serial | int | The latest serial number given for an item of this type. This is what is displayed as "Total Unboxed" on WAX ExpressTrade & OPSkins Marketplace.

#### Output Example
```json
{
    "status": 1,
    "time": 1536707797,
    "response": {
        "items": {
            "102": {
                "item_def_id": 102,
                "item_def_sub_id": null,
                "latest_serial": 2,
                "sub_items": {
                    "2": {
                        "item_def_id": 102,
                        "item_def_sub_id": 2,
                        "latest_serial": 1
                    },
                    "5": {
                        "item_def_id": 102,
                        "item_def_sub_id": 5,
                        "latest_serial": 1
                    }
                }
            }
        }
    }
}
```