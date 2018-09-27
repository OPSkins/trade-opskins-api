- [ITest](#itest)
  * [Test (v1)](#test-v1)
  * [TestAuthed (v1)](#testauthed-v1)
  * [TestBody (v1)](#testbody-v1)

# ITest

Interface used for testing

## Test (v1)

A test endpoint that doesn't require authentication and doesn't return anything information other than the default status and time fields.

`GET|POST https://api-trade.opskins.com/ITest/Test/v1/`

#### Authentication

None required.

#### Input

_none_

#### Output

```json
{
    "status": 1,
    "time": 1524696880
}
```

## TestAuthed (v1)

`GET|POST https://api-trade.opskins.com/ITest/TestAuthed/v1`

#### Authentication

API key required.

#### Input

_none_

#### OAuth Scopes
 `identity_basic`, `identity`

```json
{
    "status": 1,
    "time": 1538088235,
    "response": {
        "uid": 123456
    }
}
```

## TestBody (v1)

`GET|POST https://api-trade.opskins.com/ITest/TestBody/v1`

#### Authentication

API key required.

#### Input

Any test input.

#### Output

Everything that was sent as input.