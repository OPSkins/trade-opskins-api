## Get Case Schema

#### HTTP Request

`GET https://api-trade.opskins.com/ICase/GetCaseSchema/v1`

#### Authorization

No auth required.

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
cases | int-csv |  | A comma-separated list of case ids. If sent, output is limited to these specific cases.

#### Output

Parameter | Type | Description
--------- | -----| -------- 
cases     | array-object | cases list
--id    | int | Case ID
--name  | string | Case name
--image | object | Case image URLS
----300px | string | URL to 300px image
--skus  | array | An array of item SKU in the case