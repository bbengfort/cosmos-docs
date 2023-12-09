---
weight: 99
title: Status
---

# Status

## Status

```go
rep, _ := http.Get("http://api.cosmosgame.com/v1/status")
fmt.Println(rep)
```

```python
import requests

rep = requests.get("https://api.cosmosgame.space/v1/status/")
rep.json()
```

```shell
curl "https://api.cosmosgame.space/v1/status/"
```

> The above command returns JSON structured like this:

```json
{"status":"ok","uptime":"1h4m56.081085833s","version":"0.2.0-alpha.2"}
```

The status endpoint acts as a heartbeat for a specific Cosmos server. It returns the availability of the server along with its uptime and version information.

### HTTP Request

`GET https://api.cosmosgame.space/v1/status/`
