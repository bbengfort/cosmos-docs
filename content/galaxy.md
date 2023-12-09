---
weight: 20
title: Galaxies
---

# Galaxies (Games)

## List Galaxies (games)

```go
rep, _ := http.Get("https://api.cosmosgame.com/v1/galaxy")
fmt.Println(rep)
```

```python
import requests

rep = requests.get("https://api.cosmosgame.space/v1/galaxy/")
rep.json()
```

```shell
curl "https://api.cosmosgame.space/v1/galaxy/"
```

List all active galaxies or galaxies that are in a specific state.

### HTTP Request

`GET https://api.cosmosgame.space/v1/galaxy/`

## Create Galaxy (game)

```go
var data *models.Galaxy
rep, _ := http.Post("https://api.cosmosgame.com/v1/galaxy", data)
fmt.Println(rep)
```

```python
import requests

data = {}
rep = requests.get("https://api.cosmosgame.space/v1/galaxy/", data)
rep.json()
```

```shell
curl -X POST -d {} -H Content-Type: application/json "https://api.cosmosgame.space/v1/galaxy/"
```

Create a new galaxy (game) and join as the admin player.

### HTTP Request

`POST https://api.cosmosgame.space/v1/galaxy/`

## Galaxy (game) Detail

```go
rep, _ := http.Get("https://api.cosmosgame.com/v1/galaxy/:id")
fmt.Println(rep)
```

```python
import requests

rep = requests.get("https://api.cosmosgame.space/v1/galaxy/:id")
rep.json()
```

```shell
curl "https://api.cosmosgame.space/v1/galaxy/:id"
```

Get the details of the current galaxy (game) state.

### HTTP Request

`GET https://api.cosmosgame.space/v1/galaxy/:id`