# Other apis

## get minecraft server id from ip

```shell
curl "https://api.mcstatusbot.site/id/snekmc.schost.us" \
  -H "Authorization: Custom <token>"
```

```javascript
//make sure to install axios with npm i axios
const axios = require("axios");

async function example() {
  const res = await axios.get(
    "https://api.mcstatusbot.site/id/snekmc.schost.us",
    {
      headers: { Authorization: "Custom <token>" },
    }
  );
  console.log(res.data);
}
example();
```

```python
import requests

x = requests.get("https://api.mcstatusbot.site/id/snekmc.schost.us", headers={'Authorization': 'Custom <token>'})

print(x)
```

> The above endpoint returns JSON structured like this:

```json
{
  "ping": "3ms",
  "data": {
    "id": "mcsv1", //will be null if the server hasnt been added to this bot
  }
}
```

This endpoint retrieves the id of a minecraft server.

### HTTP Request

`GET http://https://api.mcstatusbot.site/id/<IP>`

### URL Parameters

| Parameter | Description                    |
| --------- | ------------------------------ |
| IP        | The IP of the minecraft Server |



## get minecraft server staus from ip

```shell
curl "https://api.mcstatusbot.site/status/snekmc.schost.us" \
  -H "Authorization: Custom <token>"
```

```javascript
//make sure to install axios with npm i axios
const axios = require("axios");

async function example() {
  const res = await axios.get(
    "https://api.mcstatusbot.site/status/snekmc.schost.us",
    {
      headers: { Authorization: "Custom <token>" },
    }
  );
  console.log(res.data);
}
example();
```

```python
import requests

x = requests.get("https://api.mcstatusbot.site/status/snekmc.schost.us", headers={'Authorization': 'Custom <token>'})

print(x)
```

> The above endpoint returns JSON structured like this:

```json
{
  "ping": "3ms",
  "data": {
    "id": null, //will be null if the server hasnt been added to this bot
    "online": true,
    "players": "2",
    "maxPlayers": "69",
    "latency": 124,
    "icon": "https://api.mcstatusbot.site/icon/snekmc.schost.us.png",
    "bedrock": false
  }
}
```

This endpoint retrieves the status of any minecraft server.

### HTTP Request

`GET http://https://api.mcstatusbot.site/status/<IP>`

### URL Parameters

| Parameter | Description                    |
| --------- | ------------------------------ |
| IP        | The IP of the minecraft Server |
