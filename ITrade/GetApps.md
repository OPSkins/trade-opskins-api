## Get all supported apps and their descriptions.

#### HTTP Request

`GET https://api-trade.opskins.com/ITrade/GetApps/v1/`

#### Authentication

No auth required.

#### Input
_none_
    
#### Output

Parameter | Type | Description
--------- | -----| -------- 
apps | object | List of apps and descriptions
--internal_app_id | int | Internal App ID
--steam_app_id | int | Steam App ID
--steam_context_id | int | Steam Context ID
--name | string | Short name of app
--long_name | string | Long name of app
--img | string | Image URL of app icon
--default | int | If property exists, this is the default app. Not outputted for other apps.

```json
{
    "status": 1,
    "time": 1528135996,
    "response": {
        "apps": [
            {
                "internal_app_id": 1,
                "steam_app_id": 1912,
                "steam_context_id": 1,
                "name": "VGO",
                "long_name": "VGO",
                "img": "https://opskins.com/images/games/logo-small-vgo.jpg",
                "default": 1
            }
        ]
    }
}
```
