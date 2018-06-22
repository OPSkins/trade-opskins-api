## Get user items by id numbers.

#### HTTP Request

`GET https://api-trade.opskins.com/IItem/GetItemsById/v1/`

#### Authentication

API key required.

#### Input Descriptions

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
item_id| int-csv | + | item id filter, separated with comma

#### Output Descriptions
Parameter | Type | Description
--------- | ---- | -----------
items | array-object | Array of [Standard Item Object](/IItem.md#standard-item-object)
