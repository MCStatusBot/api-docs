---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - javascript
  - python

toc_footers:
  - <a href='https://dash.mcstatusbot.site/settings/token'>Get an API Token</a>
  - <a href='https://github.com/slatedocs/slate'>Documentation Powered by Slate</a>

includes:
  - minecraft-servers
  - discord-guilds
  - other
  - errors

search: true

code_clipboard: true

meta:
  - name: description
    content: Documentation for the MC Status Bot API
---

# Introduction

<aside class="notice">
these docs are still a work in progress so some information might be missing or wrong
</aside>

Welcome to the MC Status Bot API! You can use our API to get your servers status, motd (message of the day), metrics, and more.

the api base url looks like `https://api.mcstatusbot.site/`.

by using the api you agree to follow our terms of service and privacy policy

We have language bindings in Shell, JavaScript, and Python! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.


# Authentication

> Example code using authorization:

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here" \
  -H "Authorization: Bearer <token>"
```

```javascript
//make sure to install axios with npm i axios
const axios = require('axios');

async function example() {
  const res = await axios.get("api_endpoint_here", { headers: { "Authorization" : "Bearer <token>" } });
  console.log(res.data);
}
example();
```

```python
import requests

x = requests.get("api_endpoint_here", headers={'Authorization': 'Bearer <token>'})

print(x.json)
```


> Make sure to replace `<token>` with your API Token.

MC Status Bot uses API Tokens to allow access to the API. You can register a new API Token in settings on our dashboard [https://dash.mcstatusbot.site/settings/tokens](https://dash.mcstatusbot.site/settings/tokens) by clicking the generate API Token button.
your session tokens will also show up these can not be used with the api as you can't apply restrications to them.

The API Token must be included with all your requests under the [Authorization Header](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Authorization) prefixed with `Bearer` as the auth-scheme so it looks like the following:

`Authorization: Bearer <token>`

Our API token sort of follows Discord's format where it's your ID encoded in base64, the creation timestamp of the token encoded in base64, and the token separated by a dot (.).

# RateLimits

you have a default rate limit of 100 requests per endpoint per minute. this is increased with each of our plans.

<aside class="notice">
You must replace <code>&lt;token&gt;</code> with your API Token.
</aside>



