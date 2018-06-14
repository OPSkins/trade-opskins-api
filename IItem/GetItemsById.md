## Get user items by id numbers.

#### HTTP Request

`GET https://api-trade.opskins.com/IItem/GetItemsById/v1/`

#### Input Descriptions

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
item_id| int-csv | - | item id filter, separated with comma

#### Output Descriptions
Parameter | Type | Description
--------- | ---- | -----------
items | object | [Standard Item Object](/IItem.md#standard-item-object)
