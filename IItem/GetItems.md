## Get all item meta data (only for VGO)

#### HTTP Request

`GET https://api-trade.opskins.com/IItem/GetItems/v1/`

- All enabled items: `GetItems/v1?key=apikey`

- Filter by SKU: `GetItems/v1?key=apikey&sku_filter=100`

- Filter by SKU & Wear Tier: `GetItems/v1?key=apikey&sku_filter=100&wear_tier_index=1`

- Multiple SKU: `GetItems/v1?key=apikey&sku_filter=100,102&wear_tier_index=1`

#### Input Descriptions

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
sku_filter| int-csv |  | Optional SKU filter, separated with comma
--wear_tier_index | int |  | Optional alongside sku_filter

#### Output Descriptions
Parameter | Type | Description
--------- | ---- | -----------
items | object | Object containing item meta data
--(sku) | string | SKU number
----(wear_tier_index) | string | Wear tier index
------(meta data properties) | mix | `name`, `category`, `rarity`, `type`, `color`, `image`, `suggested_price`, and `paint_index` from [Standard Item Object](/IItem.md#standard-item-object)

#### Output Example
```json
{
  "status": 1,
  "time": 1524850074,
  "response": {
      "items": {
          "10006": {
              "1": {
                  "name": "Karambit | Poison Target (Factory New)",
                  "category": "Covert Knife",
                  "rarity": "Covert",
                  "type": "Knife",
                  "color": "#eb4b4b",
                  "image": {
                    "300px": "https://files.opskins.media/file/vgo-img/item/karambit-poison-target-factory-new-300.png",
                    "600px": "https://files.opskins.media/file/vgo-img/item/karambit-poison-target-factory-new-600.png"
                  },
                  "suggested_price": 71436,
                  "paint_index": null
             }
          }
      }
  }
}
```

#### VGO Wear Tier Index Map
These mappings will never change, you may store and use as you please.
Items without tiers, e.g. keys, have a wear tier index of `0`.
```json
{
  "wear_tier_index_map": {
     "": 0,
     "Factory New": 1,
     "Minimal Wear": 2,
     "Field-Tested": 3,
     "Well-Worn": 4,
     "Battle-Scarred": 5
  },
  "wear_tier_index_to_float_map": {
     "1": {
        "min": 0,
        "max": 0.06999999999999
     },
     "2": {
        "min": 0.07,
        "max": 0.14999999999999
     },
     "3": {
        "min": 0.15,
        "max": 0.37999999999999
     },
     "4": {
        "min": 0.38,
        "max": 0.44999999999999
     },
     "5": {
        "min": 0.45,
        "max": 1
     }
  }
}
```