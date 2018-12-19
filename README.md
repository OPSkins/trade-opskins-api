# API Documentation for [WAX Trade](https://trade.opskins.com)

## API Interfaces

* [ICase](ICase.md)
* [ICaseSite](ICaseSite.md)
* [IEthereum](IEthereum.md)
* [IItem](IItem.md)
* [ITest](ITest.md)
* [ITrade](ITrade.md)
* [IUser](IUser.md)

## API Response

Direct URL to API: https://api-trade.opskins.com

All *successful* API responses have return data within the "response" object.  A typical response may look like this:

```json
{
    "status": 1,
    "time": 1528334546,
    "response": {
        "offer": {
            "some_data": "here"
        }
    }
}
```

If a response is paginated, the pagination details (`current_page` and `total_pages`) occur at the top-level of the object, not inside the `response` body.

#### Response Status Codes
All `status` codes and their titles can be found [here](https://github.com/OPSkins/trade-opskins-api/issues/19#issuecomment-403122935).

## OAuth
OPSkins OAuth works automatically with WAX Trade. You can use OAuth to log users into your website via OPSkins and (if desired) perform actions on their behalf via the API. Please see [OPSkins OAuth Docs](https://docs.opskins.com/public/en.html#oauth) for more information.

## Other Notes
- On some endpoints you may be required to send a `twofactor_code`. Please see [this comment](https://github.com/OPSkins/trade-opskins-api/issues/16#issuecomment-399715578) if you need help.
- For transferring items from OPSkins to WAX Trade, see: [OPSkins Docs: IInventory/TransferToTradeSite/v1](https://docs.opskins.com/public/en.html#IInventory_TransferToTradeSite_v1)


## Dynamic Images
- On some items, you may see image URLs like so: `https://static.wax.io/d-img/...7cea75.png`
- Default image dimensions will be `300x300` (Width x Height) or lower (depending on the original image). 
- You may request a different dimension by changing the end of the URL: `/600x600`, `/900x900`, etc.
- Best fit will be chosen automatically, so you may not always get the exact dimensions you choose. 
- You can request the original (highest resolution) image with `/original`
- e.g. https://static.wax.io/d-img/dynamic-apps/img/cdff6f51e89199e8c9772535a17cea75.png/50x50
- e.g. https://static.wax.io/d-img/dynamic-apps/img/cdff6f51e89199e8c9772535a17cea75.png/600x600
- e.g. https://static.wax.io/d-img/dynamic-apps/img/cdff6f51e89199e8c9772535a17cea75.png/original
