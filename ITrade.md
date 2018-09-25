## ITrade

Endpoints which allow Peer-to-Peer Trading.
- [ITrade/AcceptOffer](ITrade/AcceptOffer.md)
- [ITrade/CancelOffer](ITrade/CancelOffer.md)
- [ITrade/GetApps](ITrade/GetApps.md)
- [ITrade/GetOffer](ITrade/GetOffer.md)
- [ITrade/GetOffers](ITrade/GetOffers.md)
- [ITrade/GetTradeUrl](ITrade/GetTradeUrl.md)
- [ITrade/GetUserInventory](ITrade/GetUserInventory.md)
- [ITrade/GetUserInventoryFromSteamId](ITrade/GetUserInventoryFromSteamId.md)
- [ITrade/RegenerateTradeUrl](ITrade/RegenerateTradeUrl.md)
- [ITrade/SendOffer](ITrade/SendOffer.md)
- [ITrade/SendOfferToSteamId](ITrade/SendOfferToSteamId.md)


## Offer States
- STATE_ACTIVE = `2`             -- The offer is active and the recipient can accept it to exchange the items
- STATE_ACCEPTED = `3`           -- The recipient accepted the offer and items were exchanged
- STATE_EXPIRED = `5`            -- The offer expired from inactivity
- STATE_CANCELED = `6`           -- The sender canceled the offer
- STATE_DECLINED = `7`           -- The recipient declined the offer
- STATE_INVALID_ITEMS = `8`      -- One of the items in the offer is no longer available so the offer was canceled automatically
- STATE_PENDING_CASE_OPEN = `9`  -- The trade offer was initiated by a VCase site and it's awaiting eth confirmations.  User's keys have been removed, but may be restored on error later.
- STATE_EXPIRED_CASE_OPEN = `10` -- The trade offer was initiated by a VCase site and there was an error opening case due to back-end issues.  No items should have been exchanged.
- STATE_FAILED_CASE_OPEN = `12`  -- The trade offer was initiated by a VCase site and we were unable to generate items on the blockchain, so the user's keys have been refunded.

If a case opening succeeds from a vcase site, the offer will go into `STATE_ACCEPTED` and the items generated from the case opening will appear in the trade offer as if they came from the vcase site user.  The end-result is that the user will see their keys exchanged for items in the trade offer on success.

## Standard Trade Offer Object

Parameter | Type | Description
--------- | -----| -------- 
offer    | object | Holds offer and item data
--id    | int | Offer ID
--sender| object | Offer sender's information
----uid  | int | Sender's UID
----steam_id | string | Senders's SteamID
----display_name | string | Sender's display name
----avatar | string | Sender's avatar image URL
----verified | bool | Is this user verified on OPSkins by support?
----items| object | Items which sender offered for trade in the offer. [Standard Item Object](/IItem.md#standard-item-object)
--recipient| object | Offer recipient's information
----uid  | int | Recipient's uid
----steam_id | string | Recipient's SteamID
----display_name | string | Recipient's display name
----avatar | string | Recipient's avatar image URL
----verified | bool | Is this user verified on OPSkins by support?
----items| object | Recipient's items which sender wanted to receive in the offer. [Standard Item Object](/IItem.md#standard-item-object)
--state | int | Offer state int -- [Offer States](/ITrade.md#offer-states)
--state_name | string | State's display name e.g "Active"
--time_created | int | Offer creation unix timestamp
--time_updated | int | Last update unix timestamp
--time_expires | int | Offer expiration unix timestamp
--message | string | Message from sender to receiver. Max `190` characters.
--is_gift | boolean | Whether or not this offer is a gift (you are not losing any items).
--is_case_opening | boolean | Whether or not this offer is from a vCase website.
--sent_by_you | bool | Whether or not the offer was sent by you. Not outputted on no-auth endpoints.
