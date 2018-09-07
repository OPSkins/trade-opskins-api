# API Documentation for [WAX ExpressTrade](https://trade.opskins.com)

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
All `status` codes and their titles can be found [here](https://github.com/OPSkins/trade-opskins-api/issues/19#issuecomment-403122935). In some instances, the `status` code may be an HTTP status code (e.g. 404). We recognize that mixing of these codes is not ideal and will fix this in the near future.

## OAuth
OPSkins OAuth works automatically with WAX ExpressTrade as well, see [OPSkins OAuth Docs](https://docs.opskins.com/public/en.html#oauth) for more information.

## Additional Notes
- On some endpoints you may be required to send a `twofactor_code`. Please see [this comment](https://github.com/OPSkins/trade-opskins-api/issues/16#issuecomment-399715578) if you need help.
- For transferring items from OPSkins to WAX ExpressTrade, see: [OPSkins Docs: IInventory/TransferToTradeSite/v1](https://docs.opskins.com/public/en.html#IInventory_TransferToTradeSite_v1)
