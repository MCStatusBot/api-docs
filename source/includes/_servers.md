# Servers


## Get All Public Minecraft servers

```shell
curl "https://api.mcstatusbot.site/v1/servers" \
  -H "Authorization: Custom <token>"
```

```javascript
//make sure to install axios with npm i axios
const axios = require('axios');

async function example() {
  const res = await axios.get("https://api.mcstatusbot.site/v1/servers", { headers: { "Authorization" : "Custom <token>" } });
  console.log(res.data);
}
example();
```

```python
import requests

x = requests.get("https://api.mcstatusbot.site/v1/servers", headers={'Authorization': 'Custom <token>'})

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

`GET https://api.mcstatusbot.site/v1/servers`

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
curl "https://api.mcstatusbot.site/v1/servers/1" \
  -H "Authorization: Custom <token>"
```

```javascript
//make sure to install axios with npm i axios
const axios = require('axios');

async function example() {
  const res = await axios.get("https://api.mcstatusbot.site/v1/servers/1", { headers: { "Authorization" : "Custom <token>" } });
  console.log(res.data);
}
example();
```

```python
import requests

x = requests.get("https://api.mcstatusbot.site/v1/servers/1", headers={'Authorization': 'Custom <token>'})

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




## Get a Minecraft Server's uptime

```shell
curl "https://api.mcstatusbot.site/v1/servers/1/uptime" \
  -H "Authorization: Custom <token>"
```

```javascript
//make sure to install axios with npm i axios
const axios = require('axios');

async function example() {
  const res = await axios.get("https://api.mcstatusbot.site/v1/servers/1/uptime", { headers: { "Authorization" : "Custom <token>" } });
  console.log(res.data);
}
example();
```

```python
import requests

x = requests.get("https://api.mcstatusbot.site/v1/servers/1/uptime", headers={'Authorization': 'Custom <token>'})

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


### HTTP Request

`GET http://https://api.mcstatusbot.site/v1/servers/<ID>/uptime`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Server to retrieve




## Get a Minecraft Server's icon

```shell
curl "https://api.mcstatusbot.site/v1/servers/1/icon.png" \
  -H "Authorization: Custom <token>"
```

```javascript
//make sure to install axios with npm i axios
const axios = require('axios');

async function example() {
  const res = await axios.get("https://api.mcstatusbot.site/v1/servers/1/icon.png", { headers: { "Authorization" : "Custom <token>" } });
  console.log(res.data);
}
example();
```

```python
import requests

x = requests.get("https://api.mcstatusbot.site/v1/servers/1/icon.png", headers={'Authorization': 'Custom <token>'})

print(x.json)
```

> The above command returns a png image.



This endpoint retrieves a specific Server's icon in png format.


### HTTP Request

`GET http://https://api.mcstatusbot.site/v1/servers/<ID>/icon.png`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Server to retrieve




## Get a Minecraft Server's chart image

```shell
curl "https://api.mcstatusbot.site/v1/servers/mcsv1/graph/uptime.png" \
  -H "Authorization: Custom <token>"
```

```javascript
//make sure to install axios with npm i axios
const axios = require('axios');

async function example() {
  const res = await axios.get("https://api.mcstatusbot.site/v1/servers/mcsv1/graph/uptime.png", { headers: { "Authorization" : "Custom <token>" } });
  console.log(res.data);
}
example();
```

```python
import requests

x = requests.get("https://api.mcstatusbot.site/v1/servers/mcsv1/graph/uptime.png", headers={'Authorization': 'Custom <token>'})

print(x.json)
```

> The above command returns a png image.

This endpoint retrieves a specific Server's graph image.


### HTTP Request

`GET https://api.mcstatusbot.site/v1/servers/<ID>/<GRAPH_TYPE>.png`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Server to retrieve
GRAPH_TYPE | the graph type uptime, playersonline, mostactive

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
guildid | none | set to the id of the discord guild you would like to take the graph theme from.
