# Servers

## Get All Public Minecraft servers

```shell
curl "https://mcstatusbot.site/api/v1/servers" \
  -H "Authorization: Custom <token>"
```

```javascript
//make sure to install axios with npm i axios
const axios = require('axios');

async function example() {
  const res = await axios.get("https://mcstatusbot.site/api/v1/servers", { headers: { "Authorization" : "Custom <token>" } });
  console.log(res.data);
}
example();
```

```python
import requests

x = requests.get("https://mcstatusbot.site/api/v1/servers", headers={'Authorization': 'Custom <token>'})

print(x.json)
```

> The above endpoint returns JSON structured like this:

```json
{
  "page": 1,
  "pages:": 1,
  "countPerPage": 50,
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

This endpoint retrieves all Minecraft servers you can see.

### HTTP Request

`GET https://mcstatusbot.site/api/v1/servers`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_private | false | If set to true, the result will also include private servers shared with you.
include_offline | true | If set to false, the result will not include any servers that are offline.
include_online | true | If set to false, the result will not include any servers that are online.
servers_per_page | 50 | change to the number of servers you would like per page.
my_servers_only | false | If set to true, the result will only include servers owned by you.

<aside class="success">
Remember - 
</aside>

## Get a Specific Minecraft Server

```shell
curl "https://mcstatusbot.site/api/v1/servers/1" \
  -H "Authorization: Custom <token>"
```

```javascript
//make sure to install axios with npm i axios
const axios = require('axios');

async function example() {
  const res = await axios.get("https://mcstatusbot.site/api/v1/servers/1", { headers: { "Authorization" : "Custom <token>" } });
  console.log(res.data);
}
example();
```

```python
import requests

x = requests.get("https://mcstatusbot.site/api/v1/servers/1", headers={'Authorization': 'Custom <token>'})

print(x.json)
```

> The above command returns JSON structured like this:

```json
{
  "ping": "1ms",
  "data": {
    "id": 1,
    "owner": "000000000",
    "name": "SnekMC",
    "ip": "",
    "port": "25565",
    "domain": "snekmc.schost.us",
    "motd_html": "example",
    "motd_clean": "example",
    "public": true,
    "online": true,
    "members": "1",
    "maxMembers": "69",
    "lastUpadted": "1104476400",
    "bluemapurl": "NONE",
    "timezone": "GMT",
    "Bedrock": false,
    "logs": true,
  }
}
```

This endpoint retrieves a specific Server.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET http://https://mcstatusbot.site/api/v1/servers/<ID>/uptime`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Server to retrieve

## Get a Minecraft Server's uptime

```shell
curl "https://mcstatusbot.site/api/v1/servers/1/uptime" \
  -H "Authorization: Custom <token>"
```

```javascript
//make sure to install axios with npm i axios
const axios = require('axios');

async function example() {
  const res = await axios.get("https://mcstatusbot.site/api/v1/servers/1/uptime", { headers: { "Authorization" : "Custom <token>" } });
  console.log(res.data);
}
example();
```

```python
import requests

x = requests.get("https://mcstatusbot.site/api/v1/servers/1/uptime", headers={'Authorization': 'Custom <token>'})

print(x.json)
```

> The above command returns JSON structured like this:

```json
{
  "ping": "1ms",
  "data": {
    "serverid": 1,
    "upTime": "12", //in minutes 
    "downTime": "2", //in minutes 
    "upTimePercent": "85.71",
    "downTimePercent": "14.29",
    "logsStartDate":"" //unix timestamp
  }
}
```

This endpoint retrieves a specific Server.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET http://https://mcstatusbot.site/api/v1/servers/<ID>/uptime`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Server to retrieve

