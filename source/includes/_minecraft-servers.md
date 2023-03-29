# Minecraft Servers

## Get All Minecraft servers

```shell
curl "https://api.mcstatusbot.site/servers" \
  -H "Authorization: Bearer<token>"
```

```javascript
//make sure to install axios with npm i axios
const axios = require("axios");

async function example() {
  const res = await axios.get("https://api.mcstatusbot.site/servers", {
    headers: { Authorization: "Bearer<token>" },
  });
  console.log(res.data);
}
example();
```

```python
import requests

x = requests.get("https://api.mcstatusbot.site/servers", headers={'Authorization': 'Bearer<token>'})

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
      "online": true
    },
    {
      "id": 1,
      "name": "pogMC",
      "online": false
    }
  ]
}
```

This endpoint retrieves all Minecraft servers you can see.

### HTTP Request

`GET https://api.mcstatusbot.site/servers`

### Query Parameters

| Parameter        | Default | Description                                                                |
| ---------------- | ------- | -------------------------------------------------------------------------- |
| include_offline  | true    | If set to false, the result will not include any servers that are offline. |
| include_online   | true    | If set to false, the result will not include any servers that are online.  |
| servers_per_page | 50      | change to the number of servers you would like per page.                   |
| my_servers_only  | false   | If set to true, the result will only include servers owned by you.         |

<aside class="success">
Remember - 
</aside>

## Get a Specific Minecraft Server

```shell
curl "https://api.mcstatusbot.site/servers/mcsv1" \
  -H "Authorization: Bearer<token>"
```

```javascript
//make sure to install axios with npm i axios
const axios = require("axios");

async function example() {
  const res = await axios.get("https://api.mcstatusbot.site/servers/mcsv1", {
    headers: { Authorization: "Bearer<token>" },
  });
  console.log(res.data);
}
example();
```

```python
import requests

x = requests.get("https://api.mcstatusbot.site/servers/mcsv1", headers={'Authorization': 'Bearer<token>'})

print(x.json)
```

> The above command returns JSON structured like this:

```json
{
  "ping": "1ms",
  "data": {
    "id": "mcsv1",
    "owner": "522534458071449620",
    "name": "SnekMC",
    "description": "A super cool server for snakecraft hosting",
    "ip": "snekmc.schost.us",
    "motd_html": "example",
    "motd_clean": "example",
    "public": true,
    "online": true,
    "members": "1",
    "maxMembers": "69",
    "lastUpadted": "1104476400",
    "timezone": "GMT",
    "Bedrock": false,
    "logs": true
  }
}
```

This endpoint retrieves a specific Minecraft server.

## Get a Minecraft Server's uptime

```shell
curl "https://api.mcstatusbot.site/servers/1/uptime" \
  -H "Authorization: Bearer<token>"
```

```javascript
//make sure to install axios with npm i axios
const axios = require("axios");

async function example() {
  const res = await axios.get(
    "https://api.mcstatusbot.site/servers/mcsv1/uptime",
    { headers: { Authorization: "Bearer<token>" } }
  );
  console.log(res.data);
}
example();
```

```python
import requests

x = requests.get("https://api.mcstatusbot.site/servers/mcsv1/uptime", headers={'Authorization': 'Bearer<token>'})

print(x.json)
```

> The above command returns JSON structured like this:

```json
{
  "ping": "1ms",
  "data": {
    "serverid": "mcsv1",
    "upTime": "12", //in minutes
    "downTime": "2", //in minutes
    "upTimePercent": "85.71",
    "downTimePercent": "14.29",
    "logsStartDate": 1679955813 //unix timestamp
  }
}
```

This endpoint retrieves a minecraft server's uptime data.

### HTTP Request

`GET http://https://api.mcstatusbot.site/servers/<ID>/uptime`

### URL Parameters

| Parameter | Description                      |
| --------- | -------------------------------- |
| ID        | The ID of the Server to retrieve |

## Get Server logs

```shell
curl "https://api.mcstatusbot.site/servers/mcsv1/logs" \
  -H "Authorization: Bearer<token>"
```

```javascript
//make sure to install axios with npm i axios
const axios = require("axios");

async function example() {
  const res = await axios.get(
    "https://api.mcstatusbot.site/servers/mcsv1/logs",
    { headers: { Authorization: "Bearer<token>" } }
  );
  console.log(res.data);
}
example();
```

```python
import requests

x = requests.get("https://api.mcstatusbot.site/servers/mcsv1/logs", headers={'Authorization': 'Bearer<token>'})

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
      "players": "1",
      "maxPlayers": "69",
      "online": true,
      "error": "NONE",
      "latency": 22, //in ms
      "time": 1679955813
    },
    {
      "players": "0",
      "maxPlayers": "0",
      "online": true,
      "error": "TIMEOUT",
      "latency": 220, //in ms
      "time": 1679955813
    }
  ]
}
```

This endpoint retrieves the logs of your Minecraft server.

### HTTP Request

`GET https://api.mcstatusbot.site/logs/servers/<ID>/logs`

### URL Parameters

| Parameter | Description                      |
| --------- | -------------------------------- |
| ID        | The ID of the Server to retrieve |

### Query Parameters

| Parameter        | Default | Description                                              |
| ---------------- | ------- | -------------------------------------------------------- |
| servers_per_page | 50      | change to the number of servers you would like per page. |

<aside class="success">
Remember - server is pinged every 5 minutes its up to you to guess what to fill the gaps with
</aside>




## Get a Minecraft Server's icon

```shell
curl "https://api.mcstatusbot.site/servers/mcsv1/icon.png" \
  -H "Authorization: Bearer<token>"
```

```javascript
//make sure to install axios with npm i axios
const axios = require("axios");

async function example() {
  const res = await axios.get(
    "https://api.mcstatusbot.site/servers/mcsv1/icon.png",
    {
      headers: { Authorization: "Bearer<token>" },
    }
  );
  console.log(res.data);
}
example();
```

```python
import requests

x = requests.get("https://api.mcstatusbot.site/servers/mcsv1/icon.png", headers={'Authorization': 'Bearer<token>'})

print(x)
```

> The above command returns a png image.

This endpoint retrieves a specific Server's icon in png format.

### HTTP Request

`GET http://https://api.mcstatusbot.site/servers/<ID>/icon.png`

### URL Parameters

| Parameter | Description                      |
| --------- | -------------------------------- |
| ID        | The ID of the Server to retrieve |

## Get a Minecraft Server's chart image

```shell
curl "https://api.mcstatusbot.site/servers/mcsv1/graph/uptime.png" \
  -H "Authorization: Bearer<token>"
```

```javascript
//make sure to install axios with npm i axios
const axios = require("axios");

async function example() {
  const res = await axios.get(
    "https://api.mcstatusbot.site/servers/mcsv1/graph/uptime.png",
    { headers: { Authorization: "Bearer<token>" } }
  );
  console.log(res.data);
}
example();
```

```python
import requests

x = requests.get("https://api.mcstatusbot.site/servers/mcsv1/graph/uptime.png", headers={'Authorization': 'Bearer<token>'})

print(x.json)
```

> The above command returns a png image.

This endpoint retrieves a specific Server's graph image.

### HTTP Request

`GET https://api.mcstatusbot.site/servers/<ID>/<GRAPH_TYPE>.png`

### URL Parameters

| Parameter  | Description                                      |
| ---------- | ------------------------------------------------ |
| ID         | The ID of the Server to retrieve                 |
| GRAPH_TYPE | the graph type uptime, playersonline, mostactive |

### Query Parameters

| Parameter | Default | Description                                                                     |
| --------- | ------- | ------------------------------------------------------------------------------- |
| guildid   | none    | set to the id of the discord guild you would like to take the graph theme from. |
