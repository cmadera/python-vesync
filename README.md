# Vesync API in Python
Adds functions to interface with the Vesync API for Etekcity Smart Wifi Outlets.

This library allows you to get a list of devices and turn them on or off

## Usage
```python
from vesync.api import VesyncApi
import json

api = VesyncApi("USERNAME","PASSWORD")
devices = api.get_devices()
for x in devices:
        device = eval(json.dumps(x))
        print(device["deviceName"] + "=" + device["cid"] + "=" + device["deviceStatus"])

api.turn_on("cid")
api.turn_off("cid")

```

## Contributions
Pull requests are welcome.

## Disclaimer
Not affiliated with the Etekcity Corporation.
