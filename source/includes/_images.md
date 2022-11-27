# Images api

## Get Server images

```shell
curl "https://mcstatusbot.site/api/v1/images/server/1" \
  -H "Authorization: Custom <token>"
```

```javascript
//make sure to install axios with npm i axios
const axios = require('axios');

async function example() {
  const res = await axios.get("https://mcstatusbot.site/api/v1/images/server/1", { headers: { "Authorization" : "Custom <token>" } });
  console.log(res.data);
}
example();
```

```python
import requests

x = requests.get("https://mcstatusbot.site/api/v1/images/server/1", headers={'Authorization': 'Custom <token>'})

print(x.json)
```

> The above endpoint returns JSON structured like this:

```json
{
  "ping": "3ms",
  "data": {
      "serverid": 1,
      "icon": "https://mcstatusbot.site/api/v1/images/server/1/icon.png",
      "charts": {
        "uptime":"https://mcstatusbot.site/api/v1/images/charts/server/1/uptime.png",
        "playersonline":"https://mcstatusbot.site/api/v1/images/charts/server/1/playersonline.png",
        "mostactive": "https://mcstatusbot.site/api/v1/images/charts/server/1/mostactive.png"
      },
    }
}
```

This endpoint retrieves links to the Minecraft Server icon and uptime, playersonline and mostactive charts.

### HTTP Request

`GET https://mcstatusbot.site/api/v1/images/server/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Server to retrieve


<aside class="notice">
This endpoint is really not needed you can see how it returnes the endpoints listed below but it has some validation aspects so use it or don't use it
</aside>



## Get Server Icon

```shell
curl "https://mcstatusbot.site/api/v1/images/server/1/icon.png" \
  -H "Authorization: Custom <token>"
```

```javascript
//make sure to install axios with npm i axios
const axios = require('axios');

async function example() {
  const res = await axios.get("https://mcstatusbot.site/api/v1/images/server/1/icon.png", { headers: { "Authorization" : "Custom <token>" } });
  console.log(res.data);
}
example();
```

```python
import requests

x = requests.get("https://mcstatusbot.site/api/v1/images/server/1/icon.png", headers={'Authorization': 'Custom <token>'})

print(x.json)
```

> The above endpoint returns a PNG image

This endpoint returns a png image of the Minecraft Server's icon.

### HTTP Request

`GET https://mcstatusbot.site/api/v1/images/server/<ID>/icon.png`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Server to retrieve



## Get Server uptime chart

```shell
curl "https://mcstatusbot.site/api/v1/images/charts/server/1/uptime.png" \
  -H "Authorization: Custom <token>"
```

```javascript
//make sure to install axios with npm i axios
const axios = require('axios');

async function example() {
  const res = await axios.get("https://mcstatusbot.site/api/v1/images/charts/server/1/uptime.png", { headers: { "Authorization" : "Custom <token>" } });
  console.log(res.data);
}
example();
```

```python
import requests

x = requests.get("https://mcstatusbot.site/api/v1/images/charts/server/1/uptime.png", headers={'Authorization': 'Custom <token>'})

print(x.json)
```

> The above endpoint returns a PNG image



This endpoint returns a png image of the Minecraft Server's uptime chart.

### HTTP Request

`GET https://mcstatusbot.site/api/v1/images/charts/server/<ID>/uptime.png`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Server to retrieve



## Get Server PlayersOnline chart

```shell
curl "https://mcstatusbot.site/api/v1/images/charts/server/1/playersonline.png" \
  -H "Authorization: Custom <token>"
```

```javascript
//make sure to install axios with npm i axios
const axios = require('axios');

async function example() {
  const res = await axios.get("https://mcstatusbot.site/api/v1/images/charts/server/1/playersonline.png", { headers: { "Authorization" : "Custom <token>" } });
  console.log(res.data);
}
example();
```

```python
import requests

x = requests.get("https://mcstatusbot.site/api/v1/images/charts/server/1/playersonline.png", headers={'Authorization': 'Custom <token>'})

print(x.json)
```

> The above endpoint returns a PNG image

This endpoint returns a png image of the Minecraft Server's PlayersOnline chart.

### HTTP Request

`GET https://mcstatusbot.site/api/v1/images/charts/server/<ID>/mostactive.png`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Server to retrieve


## Get Server MostActive chart

```shell
curl "https://mcstatusbot.site/api/v1/images/charts/server/1/mostactive.png" \
  -H "Authorization: Custom <token>"
```

```javascript
//make sure to install axios with npm i axios
const axios = require('axios');

async function example() {
  const res = await axios.get("https://mcstatusbot.site/api/v1/images/charts/server/1/mostactive.png", { headers: { "Authorization" : "Custom <token>" } });
  console.log(res.data);
}
example();
```

```python
import requests

x = requests.get("https://mcstatusbot.site/api/v1/images/charts/server/1/mostactive.png", headers={'Authorization': 'Custom <token>'})

print(x.json)
```

> The above endpoint returns a PNG image

This endpoint returns a png image of the Minecraft Server's MostActive chart.

### HTTP Request

`GET https://mcstatusbot.site/api/v1/images/charts/server/<ID>/mostactive.png`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Server to retrieve