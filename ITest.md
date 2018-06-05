- [ITest](#itest)
  * [Test (v1)](#test-v1)
  * [TestAuthed (v1)](#testauthed-v1)
  * [TestBody (v1)](#testbody-v1)

# ITest

Interface used for testing

## Test (v1)

`GET|POST https://api-trade.opskins.com/ITest/Test/v1/`

`GET|POST https://api-trade.opskins.com/ITest/TestAuthed/v1`

A test endpoint that doesn't require authentication and doesn't return anything information other than the default status and time fields.

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
_none_ | | | 

#### Output

```json
{
    "status": 1,
    "time": 1524696880
}
```

## TestAuthed (v1)

TODO

## TestBody (V1)

TODO