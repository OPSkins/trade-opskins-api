# IItem

- [IItem/GetItemsById](IItem/GetItemsById.md)
- [IItem/WithdrawToOpskins](IItem/WithdrawToOpskins.md)
- [IItem/GetItems](IItem/GetItems.md)

## Standard Item Object

Parameter | Type | Description
--------- | -----| -------- 
id | int | Item ID
internal_app_id | int | Internal App ID (see [ITrade/GetApps](/ITrade/GetApps.md))
sku | int | Item definition (meta-data) SKU #
wear | float | Wear float value, only applicable for certain apps
trade_hold_expires | int / null | Trade hold expiration date. `null` if no trade hold
name | string | Market name e.g. "MAG-7 Gold Digger (Factory New)"
category | string | Category name e.g. "Restricted Rifle"
rarity | string | Category rarity e.g. "Restricted" -- only outputted for VGO
type | string | Category type e.g. "Rifle" -- only outputted for VGO
color | string | Color hex, includes #
image | object | Generic image URLs
--300px | string | 300px image URL - https://files.opskins.media/file/vgo-img/item/dual-berettas-trigger-happy-battle-scarred-300.png
--600px | string | 600px image URL - https://files.opskins.media/file/vgo-img/item/dual-berettas-trigger-happy-battle-scarred-600.png
suggested_price | int | OPSkins 7-day suggested price (US cents)
suggested_price_floor | int | (Only for VGO) The minimum viable suggested price, does not change.
preview_urls | object | Field Inspection URLs for VGO items. Some of these properties may not be outputted if not available. If they are provided, the image or video itself may not be generated yet, so you should fallback to generic images provided in `image` object.
--thumb_image | string | https://files.opskins.media/file/vgo-img/previews/163609_thumb.jpg
--front_image | string | https://files.opskins.media/file/vgo-img/previews/163638_front.jpg
--back_image | string | https://files.opskins.media/file/vgo-img/previews/163638_back.jpg
--video | string | https://files.opskins.media/file/vgo-img/previews/163638_video.webm
inspect | string / null | Steam in-game inspection URL. Can be `null`.
eth_inspect | string / null | Etherscan.io Ethereum Transaction URL. `null` for inapplicable apps.
pattern_index | int | Pattern index (value between 1-1000) (only available for VGO, `null` for other apps)
paint_index | int / null | Paint index value for a CS:GO item. `0` or `null` for items without a paint-index.

## Example Output for Standard Item Object
```json
{
    "id": 363645,
    "sku": 10006,
    "wear": 0.583130179639101,
    "pattern_index": 549,
    "preview_urls": {
      "thumb_image": "https://files.opskins.media/file/vgo-img/previews/164325_thumb.jpg",
      "front_image": "https://files.opskins.media/file/vgo-img/previews/164342_front.jpg",
      "back_image": "https://files.opskins.media/file/vgo-img/previews/164342_back.jpg",
      "video": "https://files.opskins.media/file/vgo-img/previews/164342_video.webm"
    },
    "eth_inspect": null,
    "trade_hold_expires": null,
    "internal_app_id": 1,
    "inspect": null,
    "name": "Karambit | Poison Target (Factory New)",
    "category": "Covert Knife",
    "rarity": "Covert",
    "type": "Knife",
    "paint_index": null,
    "color": "#eb4b4b",
    "image": {
      "300px": "https://files.opskins.media/file/vgo-img/item/karambit-poison-target-factory-new-300.png",
      "600px": "https://files.opskins.media/file/vgo-img/item/karambit-poison-target-factory-new-600.png"
    },
    "suggested_price": 71436
}
```
