## Get all supported apps and their descriptions.

#### HTTP Request

`GET https://api-trade.opskins.com/ITrade/GetApps/v1/`

#### Input
_none_
    
#### Output

Parameter | Type | Description
--------- | -----| -------- 
apps | object | List of apps and descriptions
 - internal_app_id | int | Internal App ID
 - steam_app_id | int | Steam App ID
 - steam_context_id | int | Steam Context ID
 - name | string | Short name of app
 - long_name | string | Long name of app
 - img | string | Image URL of app icon
 - default | int | If property exists, this is the default app. Not outputted for other apps.

```json
{
    "status": 1,
    "time": 1528135996,
    "response": {
        "apps": [
            {
                "internal_app_id": 2,
                "steam_app_id": 730,
                "steam_context_id": 2,
                "name": "CS:GO",
                "long_name": "Counter-Strike: Global Offensive",
                "img": null,
                "default": 1
            }
        ]
    }
}
```