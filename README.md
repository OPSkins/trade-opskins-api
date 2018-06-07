# API Documentation for [trade.opskins.com](https://trade.opskins.com)

Direct URL to API: [api-trade.opskins.com](https://api-trade.opskins.com)

All API responses are within the "response" object.  A typical response may look like this:

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

## API Interfaces

* [IItem](IItem.md)
* [ITest](ITest.md)
* [ITrade](ITrade.md)
* [IUser](IUser.md)

For transferring items from OPSkins.com to ExpressTrade, please see [OPSkins Docs: IInventory/TransferToTradeSite/v1](https://docs.opskins.com/public/en.html#IInventory_TransferToTradeSite_v1)
