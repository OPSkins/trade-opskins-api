## Get Case Schema

#### HTTP Request

`GET https://api-trade.opskins.com/ICase/GetCaseSchema/v1`

#### Authentication

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
----600px | string | URL to 600px image
----900px | string | URL to 900px image
----1800px | string | URL to 1800px image
----2500px | string | URL to 2500px image
--skus  | array | An array of item SKU in the case
