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

## Additional Notes
- For transferring items from OPSkins to WAX ExpressTrade, see: [OPSkins Docs: IInventory/TransferToTradeSite/v1](https://docs.opskins.com/public/en.html#IInventory_TransferToTradeSite_v1)
