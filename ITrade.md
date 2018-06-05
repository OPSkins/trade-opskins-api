## ITrade

Endpoints which allows Peer-to-Peer Trading.
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


### Offer states constants:
- STATE_ACTIVE = 2;                             /** The offer is active and the recipient can accept it to exchange the items */
- STATE_ACCEPTED = 3;                           /** The recipient accepted the offer and items were exchanged */
- STATE_EXPIRED = 5;                            /** The offer expired from inactivity */
- STATE_CANCELED = 6;                           /** The sender canceled the offer */
- STATE_DECLINED = 7;                           /** The recipient declined the offer */
- STATE_INVALID_ITEMS = 8;                      /** One of the items in the offer is no longer available/eligible so the offer was canceled automatically */


## Standard Trade Offer Object

Parameter | Type | Description
--------- | -----| -------- 
offer    | object | Holds offer and item data
  - id    | int | offer id
  - sender| object | Offer sender's information
  -- uid  | int | Sender's uid
  -- steam_id | string | Senders's SteamID
  -- display_name | string | Sender's display name
  -- avatar | string | Sender's avatar image url
  -- items| object | Items which sender offered for trade in the offer. [Standard Item Object](IItem.md#standard-item-object)
  - recipient| object | Offer recipient's information
  -- uid  | int | Recipient's uid
  -- steam_id | string | Recipient's SteamID
  -- display_name | string | Recipient's display name
  -- avatar | string | Recipient's avatar image url
  -- items| object | Recipient's items which sender wanted to receive in the offer. [Standard Item Object](IItem.md#standard-item-object)
  - state | int | Offer state code (See available state constants in [ITrade](ITrade.md))
  - state_name | string | State's display name
  - time_created | int | Offer creation timestamp
  - time_updated | int | Last update timestamp
  - time_expires | int | Offer expiration timestamp
  - message | string | Message from sender to receiver
  - sent_by_you | bool | Whether or not offer was sent by you, not outputted on non-authenticated endpoints.