## Get user items by id numbers.

#### HTTP Request

`POST https://api-trade.opskins.com/ITrade/GetItemsById/v1/`

#### Input Descriptions

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
item_id| int-csv | - | item id filter, separated with comma

#### Output Descriptions
Parameter | Type | Description
--------- | ---- | -----------
items | object | [Standard Item Object](/IItem.md#standard-item-object)