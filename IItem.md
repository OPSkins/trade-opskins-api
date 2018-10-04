# IItem

- [IItem/GetItemsById](IItem/GetItemsById.md)
- [IItem/WithdrawToOpskins](IItem/WithdrawToOpskins.md)
- [IItem/GetItems](IItem/GetItems.md)
- [IItem/GetRarityStats](IItem/GetRarityStats.md)

## Standard Item Object

Parameter | Type | Description
--------- | -----| -------- 
id | int | Item ID
internal_app_id | int | Internal App ID (see [ITrade/GetApps](/ITrade/GetApps.md))
sku | int | Item definition (meta-data) SKU #
wear | float | Wear float value, only applicable for certain apps
trade_hold_expires | int / null | Trade hold expiration date. `null` if no trade hold
name | string | Market name e.g. `AK-47 Anubis (Minimal Wear)`
category | string | Category name e.g. `Covert Rifle`
rarity | string | Category rarity e.g. `Covert` -- only outputted for VGO
type | string | Category type e.g. `Rifle` -- only outputted for VGO
color | string | Color hex, includes #
image | object | Generic image URLs
--300px | string | 300px image URL - https://files.opskins.media/file/vgo-img/item/ak-47-anubis-minimal-wear-300.png
--600px | string | 600px image URL - https://files.opskins.media/file/vgo-img/item/ak-47-anubis-minimal-wear-600.png
suggested_price | int | OPSkins 7-day suggested price (US cents)
suggested_price_floor | int | (Only for VGO) The minimum viable suggested price, does not change.
preview_urls | object | Field Inspection URLs for VGO items. Some of these properties may not be outputted if not available. If they are provided, the image or video itself may not be generated yet, so you should fallback to generic images provided in `image` object.
--3d_viewer | string | https://3d.opskins.media/?skin=ak-47-anubis-minimal-wear&id=4569737
--thumb_image | string | https://files.opskins.media/file/vgo-img/previews/4569737_thumb.jpg
--front_image_low | string | https://files.opskins.media/file/vgo-img/previews/4569737_front.jpg
--front_image | string | https://files.opskins.media/file/vgo-img/previews/4569730_front.jpg
--back_image | string | https://files.opskins.media/file/vgo-img/previews/4569730_back.jpg
--video | string | https://files.opskins.media/file/vgo-img/previews/4569730_video.webm
inspect | string / null | Steam in-game inspection URL. Can be `null`.
eth_inspect | string / null | Etherscan.io Ethereum Transaction URL. `null` for inapplicable apps.
pattern_index | int | Pattern index (value between 1-1000) (only available for VGO, `null` for other apps)
paint_index | int / null | Paint index value for a CS:GO item. `0` or `null` for items without a paint-index.
wear_tier_index | int | Wear Tier Index for a VGO item, not set for other apps.
attributes | object | Item's attributes

## Example Output for Standard Item Object
```json
{
  "id": 6104524,
  "sku": 151,
  "wear": 0.10575609654188,
  "pattern_index": 700,
  "preview_urls": {
    "3d_viewer": "https://3d.opskins.media/?skin=ak-47-anubis-minimal-wear&id=4569737",
    "thumb_image": "https://files.opskins.media/file/vgo-img/previews/4569737_thumb.jpg",
    "front_image_low": "https://files.opskins.media/file/vgo-img/previews/4569737_front.jpg",
    "front_image": "https://files.opskins.media/file/vgo-img/previews/4569730_front.jpg",
    "back_image": "https://files.opskins.media/file/vgo-img/previews/4569730_back.jpg",
    "video": "https://files.opskins.media/file/vgo-img/previews/4569730_video.webm"
  },
  "eth_inspect": null,
  "trade_hold_expires": null,
  "internal_app_id": 1,
  "inspect": null,
  "tradable": true,
  "attributes": {
    "serial_sku": 290,
    "serial_sku_wear": 25
  },
  "name": "AK-47 | Anubis (Minimal Wear)",
  "category": "Covert Rifle",
  "rarity": "Covert",
  "type": "Rifle",
  "paint_index": null,
  "color": "#eb4b4b",
  "image": {
    "300px": "https://files.opskins.media/file/vgo-img/item/ak-47-anubis-minimal-wear-300.png",
    "600px": "https://files.opskins.media/file/vgo-img/item/ak-47-anubis-minimal-wear-600.png"
  },
  "suggested_price": 18660,
  "suggested_price_floor": 18660,
  "wear_tier_index": 2
}
```
