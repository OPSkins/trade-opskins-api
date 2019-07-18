## Get Case Odds

#### HTTP Request

`GET https://api-trade.wax.io/ICase/GetCaseOdds/v1`

#### Authentication

No auth required.

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
cases | int-csv |  | A comma-separated list of case IDs. If sent, output is limited to these specific cases.

#### Output

Parameter | Type | Description
--------- | -----| -------- 
cases     | array-object | An array of objects containing each case
--id    | int | Case ID
--name | string | Case Name
--total_weight  | string | Total weight of case in kilograms
--total_percent | string | Total percent, `relative_percent`'s added together.
--odds | array-object | An array containing object lists of odds per `sku`
----sku | int | Item `sku` for VGO, `def_id` for other apps/items
----weight | string | Weight correponding to `total_weight`
----relative_weight | string | Weight relative to all other items in the case
----relative_percent | string | % chance of receiving this item, can be displayed to user. (`relative_weight` * 100)

#### Example Output https://api-trade.wax.io/ICase/GetCaseOdds/v1?cases=1

```json
{
  "status": 1,
  "time": 1545432800,
  "response": {
    "cases": [
      {
        "id": 1,
        "name": "Weapon Case 1",
        "total_weight": "258917554",
        "total_percent": "99.99999999999986",
        "odds": [
          {
            "sku": 100,
            "weight": "780000",
            "relative_weight": "0.00301254197697",
            "relative_percent": "0.30125419769723"
          },
          {
            "sku": 101,
            "weight": "780000",
            "relative_weight": "0.00301254197697",
            "relative_percent": "0.30125419769723"
          },
          {
            "sku": 102,
            "weight": "10385844",
            "relative_weight": "0.04011255258498",
            "relative_percent": "4.01125525849823"
          },
          {
            "sku": 103,
            "weight": "10385844",
            "relative_weight": "0.04011255258498",
            "relative_percent": "4.01125525849823"
          },
          {
            "sku": 104,
            "weight": "10385844",
            "relative_weight": "0.04011255258498",
            "relative_percent": "4.01125525849823"
          },
          {
            "sku": 105,
            "weight": "12177681",
            "relative_weight": "0.04703304512138",
            "relative_percent": "4.70330451213825"
          },
          {
            "sku": 106,
            "weight": "12177681",
            "relative_weight": "0.04703304512138",
            "relative_percent": "4.70330451213825"
          },
          {
            "sku": 107,
            "weight": "12177681",
            "relative_weight": "0.04703304512138",
            "relative_percent": "4.70330451213825"
          },
          {
            "sku": 108,
            "weight": "12177681",
            "relative_weight": "0.04703304512138",
            "relative_percent": "4.70330451213825"
          },
          {
            "sku": 109,
            "weight": "12177681",
            "relative_weight": "0.04703304512138",
            "relative_percent": "4.70330451213825"
          },
          {
            "sku": 110,
            "weight": "23580231",
            "relative_weight": "0.09107235347975",
            "relative_percent": "9.10723534797490"
          },
          {
            "sku": 111,
            "weight": "23580231",
            "relative_weight": "0.09107235347975",
            "relative_percent": "9.10723534797490"
          },
          {
            "sku": 112,
            "weight": "23580231",
            "relative_weight": "0.09107235347975",
            "relative_percent": "9.10723534797490"
          },
          {
            "sku": 113,
            "weight": "23580231",
            "relative_weight": "0.09107235347975",
            "relative_percent": "9.10723534797490"
          },
          {
            "sku": 114,
            "weight": "23580231",
            "relative_weight": "0.09107235347975",
            "relative_percent": "9.10723534797490"
          },
          {
            "sku": 115,
            "weight": "23580231",
            "relative_weight": "0.09107235347975",
            "relative_percent": "9.10723534797490"
          },
          {
            "sku": 116,
            "weight": "23580231",
            "relative_weight": "0.09107235347975",
            "relative_percent": "9.10723534797490"
          },
          {
            "sku": 10000,
            "weight": "10000",
            "relative_weight": "0.00003862233304",
            "relative_percent": "0.00386223330381"
          },
          {
            "sku": 10001,
            "weight": "10000",
            "relative_weight": "0.00003862233304",
            "relative_percent": "0.00386223330381"
          },
          {
            "sku": 10002,
            "weight": "10000",
            "relative_weight": "0.00003862233304",
            "relative_percent": "0.00386223330381"
          },
          {
            "sku": 10003,
            "weight": "10000",
            "relative_weight": "0.00003862233304",
            "relative_percent": "0.00386223330381"
          },
          {
            "sku": 10004,
            "weight": "10000",
            "relative_weight": "0.00003862233304",
            "relative_percent": "0.00386223330381"
          },
          {
            "sku": 10005,
            "weight": "10000",
            "relative_weight": "0.00003862233304",
            "relative_percent": "0.00386223330381"
          },
          {
            "sku": 10006,
            "weight": "10000",
            "relative_weight": "0.00003862233304",
            "relative_percent": "0.00386223330381"
          },
          {
            "sku": 10007,
            "weight": "10000",
            "relative_weight": "0.00003862233304",
            "relative_percent": "0.00386223330381"
          },
          {
            "sku": 10008,
            "weight": "10000",
            "relative_weight": "0.00003862233304",
            "relative_percent": "0.00386223330381"
          },
          {
            "sku": 10009,
            "weight": "10000",
            "relative_weight": "0.00003862233304",
            "relative_percent": "0.00386223330381"
          },
          {
            "sku": 10010,
            "weight": "10000",
            "relative_weight": "0.00003862233304",
            "relative_percent": "0.00386223330381"
          },
          {
            "sku": 10011,
            "weight": "10000",
            "relative_weight": "0.00003862233304",
            "relative_percent": "0.00386223330381"
          },
          {
            "sku": 10012,
            "weight": "10000",
            "relative_weight": "0.00003862233304",
            "relative_percent": "0.00386223330381"
          },
          {
            "sku": 10013,
            "weight": "10000",
            "relative_weight": "0.00003862233304",
            "relative_percent": "0.00386223330381"
          },
          {
            "sku": 10014,
            "weight": "10000",
            "relative_weight": "0.00003862233304",
            "relative_percent": "0.00386223330381"
          },
          {
            "sku": 10015,
            "weight": "10000",
            "relative_weight": "0.00003862233304",
            "relative_percent": "0.00386223330381"
          },
          {
            "sku": 10016,
            "weight": "10000",
            "relative_weight": "0.00003862233304",
            "relative_percent": "0.00386223330381"
          },
          {
            "sku": 10017,
            "weight": "10000",
            "relative_weight": "0.00003862233304",
            "relative_percent": "0.00386223330381"
          },
          {
            "sku": 10018,
            "weight": "10000",
            "relative_weight": "0.00003862233304",
            "relative_percent": "0.00386223330381"
          },
          {
            "sku": 10019,
            "weight": "10000",
            "relative_weight": "0.00003862233304",
            "relative_percent": "0.00386223330381"
          },
          {
            "sku": 10020,
            "weight": "10000",
            "relative_weight": "0.00003862233304",
            "relative_percent": "0.00386223330381"
          },
          {
            "sku": 10021,
            "weight": "10000",
            "relative_weight": "0.00003862233304",
            "relative_percent": "0.00386223330381"
          },
          {
            "sku": 10022,
            "weight": "10000",
            "relative_weight": "0.00003862233304",
            "relative_percent": "0.00386223330381"
          },
          {
            "sku": 10023,
            "weight": "10000",
            "relative_weight": "0.00003862233304",
            "relative_percent": "0.00386223330381"
          },
          {
            "sku": 10024,
            "weight": "10000",
            "relative_weight": "0.00003862233304",
            "relative_percent": "0.00386223330381"
          }
        ]
      }
    ]
  }
}
```
