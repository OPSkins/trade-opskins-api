## Reports a trade offer

#### HTTP Request

`POST https://api-trade.opskins.com/IUser/UserReports/v1`

#### Authentication

API key required.

#### Input

Parameter   | Type    | Required   | Description
---------   | -----   | :--------: | -----------
message     | string  | +        | Message included in the report
report_type | integer | +        | Reason - spam = 1, phishing = 2, error = 3;
offer_id    | integer | +        | Id of the reported offer

#### Output

Parameter | Type    | Description
--------- | -----   | --------
success   | boolean | true if everything went well
