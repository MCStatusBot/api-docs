# Server Logs

## Get Server uptime

```shell
curl "https://api.mcstatusbot.site/v1/logs/servers/1/uptime" \
  -H "Authorization: Custom <token>"
```

```javascript
//make sure to install axios with npm i axios
const axios = require('axios');

async function example() {
  const res = await axios.get("https://api.mcstatusbot.site/v1/logs/servers/1/uptime", { headers: { "Authorization" : "Custom <token>" } });
  console.log(res.data);
}
example();
```

```python
import requests

x = requests.get("https://api.mcstatusbot.site/v1/logs/servers/1/uptime", headers={'Authorization': 'Custom <token>'})

print(x.json)
```

> The above endpoint returns JSON structured like this:

```json
{
  "page": 1,
  "pages:": 1,
  "countPerPage":50,
  "ping": "3ms",
  "data": [
    {
      "id": 1,
      "name": "SnekMC",
      "online": true,
    },
    {
      "id": 1,
      "name": "pogMC",
      "online": false,
    }
  ]
}
```

This endpoint retrieves the uptime logs of your Minecraft server.

### HTTP Request

`GET https://api.mcstatusbot.site/v1/logs/servers/<ID>/uptime`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Server to retrieve

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
servers_per_page | 50 | change to the number of servers you would like per page.

<aside class="success">
Remember - 
</aside>