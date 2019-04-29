# IItem
- [IItem/GetAllItems](IItem/GetAllItems.md)
- [IItem/GetItemsById](IItem/GetItemsById.md)
- [IItem/WithdrawToOpskins](IItem/WithdrawToOpskins.md)
- [IItem/GetItems](IItem/GetItems.md)
- [IItem/GetItemDefinitions](IItem/GetItemDefinitions.md)
- [IItem/GetRarityStats](IItem/GetRarityStats.md)
- [IItem/InstantSellRecentItems](IItem/InstantSellRecentItems.md)
## Standard Item Sorts
- `1` By name ASC (alphabetical, `z` first)
- `2` By name DESC (alphabetical, `a` first)
- `3` By last_update ASC (oldest first by update)
- `4` By last_update DESC (newest first by update)
- `5` By suggested price ASC (lowest first)
- `6` By suggested price DESC (highest first)
- `7` By id ASC (oldest first by creation)
- `8` By id DESC (newest first by creation)
## Standard Item Object
Parameter | Type | Description
--------- | -----| -------- 
id | int | Item ID
internal_app_id | int | Internal App ID (see [ITrade/GetApps](/ITrade/GetApps.md))
def_id | int | Unique Definition ID, this is a unique & unchanging identifier for each item, regardless of app_id. Not to be confused with sku, which is not unique per wear-tier for VGO items. VGO item `def_id` range is 900,000,000 ~ 999,999,999.
sku | int | Item SKU #, mainly utilized for VGO items. For all other items that don't have a `sku`, this will be the same as `def_id`.
wear | float | Wear float value, only applicable for certain apps
tradable | bool | Is item tradable? Items may be temporarily untradable during certain operations, e.g. transfers.
is_trade_restricted | bool | If true, item cannot be traded to other users until owner is whitelisted.
trade_hold_expires | int / null | Trade hold expiration date. `null` if no trade hold
name | string | Simpler name for an item (compared to full `market_name`). May change without notice.
market_name | string | Full market name e.g. `AK-47 Anubis (Minimal Wear)`. May change without notice.
category | string | Category name e.g. `Covert Rifle`
rarity | string | Category rarity e.g. `Covert` -- only outputted for VGO
type | string | Category type e.g. `Rifle` -- only outputted for VGO
color | string | Color hex, includes #
image | object | Generic image URLs
--300px | string | 300px image URL - https://files.opskins.media/file/vgo-img/item/ak-47-anubis-minimal-wear-300.png (available for all VGO items)
--600px | string | 600px image URL - https://files.opskins.media/file/vgo-img/item/ak-47-anubis-minimal-wear-600.png (available for all VGO items)
--900px | string | 900px image URL - https://files.opskins.media/file/vgo-img/item/ak-47-anubis-minimal-wear-900.png (not available for all VGO items yet)
--1800px | string | 1800px image URL - https://files.opskins.media/file/vgo-img/item/ak-47-anubis-minimal-wear-1800.png (not available for all VGO items yet)
--2500px | string | 2500px image URL - https://files.opskins.media/file/vgo-img/item/ak-47-anubis-minimal-wear-2500.png (not available for all VGO items yet)
suggested_price | int | OPSkins 7-day suggested price (US cents)
suggested_price_floor | int | The minimum viable suggested price, does not change based on market sales, so this may be considered as a 'stable' price.
preview_urls | object | Inspection URLs for items. Some of these properties may not be outputted if not available. If they are provided, the image or video itself may not be generated yet, so you should fallback to generic images provided in `image` object.
--3d_viewer | string | https://3d.opskins.media/?skin=ak-47-anubis-minimal-wear&id=4569737
--thumb_image | string | https://files.opskins.media/file/vgo-img/previews/4569737_thumb.jpg
--front_image_low | string | https://files.opskins.media/file/vgo-img/previews/4569737_front.jpg
--front_image | string | https://files.opskins.media/file/vgo-img/previews/4569730_front.jpg
--back_image | string | https://files.opskins.media/file/vgo-img/previews/4569730_back.jpg
--video | string | https://files.opskins.media/file/vgo-img/previews/4569730_video.webm
assets | object | VGO 3D assets (not available for inapplicable apps). Assets may be `csgo_compatible_files` (legacy, must be rendered inside CSGO) or `unity3d_compatible_files` (standard/modern pbr textures, can be integrated into different games). The `main_texture_processed` is available for `unity3d_compatible_files` only (`null` for `csgo_compatible_files`).
--type | string | unity3d_compatible_files
--3d_model | string | https://files.opskins.media/file/vgo-img/assets/3d-models/ak-47.obj
--raw_textures | string | https://files.opskins.media/file/vgo-img/assets/raw-textures/ak_47_anubis.zip
--main_texture_processed | string | https://files.opskins.media/file/vgo-img/previews/4569737_texture.jpg
inspect | string / null | Steam in-game inspection URL. Can be `null`.
eth_inspect | string / null | Etherscan.io Ethereum Transaction URL. `null` for inapplicable apps.
pattern_index | int | Pattern index (value between 1-1000) (only available for VGO, `null` for other apps)
paint_index | int / null | Paint index value for a CS:GO item. `0` or `null` for items without a paint-index.
wear_tier_index | int | Wear Tier Index for a VGO item, not set for other apps.
time_created | int | Unix timestamp of when this item was created
time_updated | int | Unix timestamp of when this item was last updated
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
    "assets": {
        "type": "unity3d_compatible_files",
        "3d_model": "https://files.opskins.media/file/vgo-img/assets/3d-models/ak-47.obj",
        "raw_textures": "https://files.opskins.media/file/vgo-img/assets/raw-textures/ak_47_anubis.zip",
        "main_texture_processed": "https://files.opskins.media/file/vgo-img/previews/4569737_texture.jpg"
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
        "300px": "https://files.opskins.media/file/vgo-img/item/ak-47-anubis-factory-new-300.png",
        "600px": "https://files.opskins.media/file/vgo-img/item/ak-47-anubis-factory-new-600.png",
        "900px": "https://files.opskins.media/file/vgo-img/item/ak-47-anubis-factory-new-900.png",
        "1800px": "https://files.opskins.media/file/vgo-img/item/ak-47-anubis-factory-new-1800.png",
        "2500px": "https://files.opskins.media/file/vgo-img/item/ak-47-anubis-factory-new-2500.png"
    },
    "suggested_price": 18660,
    "suggested_price_floor": 18660,
    "wear_tier_index": 2
}
```
