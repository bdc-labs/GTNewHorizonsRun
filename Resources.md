# Useful resources

## Spreadsheets

- [Tips & Tricks - TheShadowofX & Threefold](https://docs.google.com/spreadsheets/d/1rsB5OOAkFgJ_lzhtVzWZc2aNCSo0e6lRhJG8Po7NZtY/edit?gid=2104320957#gid=2104320957)
- [Large Turbine Calculator](https://docs.google.com/spreadsheets/d/15qeGeniW1WiUFQ_8JnJdvCiHBM9HutpN_msiI20N1r0/edit?gid=655714366#gid=655714366)

## Crops

- [IC2 crops List](https://gtnh.miraheze.org/wiki/IC2_Crops_List)
- [IC2 crop breeding calculator](https://bombcar.github.io/)
- [Renewable resources](https://gtnh.miraheze.org/wiki/Renewable_Resources)
- [Thaumcraft research cheatsheet](https://gtnh.miraheze.org/wiki/Thaumcraft_Research_Cheatsheet)

## OpenComputers

[VS Code setup](https://gist.github.com/Gimpeh/19241ee7c3c9338ed4fb56d9dba1dd9c)

Install JSON parser:

```shell
wget https://raw.githubusercontent.com/sziberov/OpenComputers/master/lib/json.lua && mv json.lua /lib/
```

Example JSON handling:

```lua
local internet = require("internet")
local json = require("json")


local webhookUrl = "WEBHOOK_URL"

local postData = {
  content = "Hello, Discord!"
}

local headers = {
  ["Content-Type"] = "application/json",
  ["User-Agent"] = "Mozilla/5.0 (X11; U; Linux i686) Gecko/20071127 Firefox/2.0.0.11"
}


local postJSON = json:encode(postData)
local response = internet.request(webhookUrl, postJSON, headers)
```