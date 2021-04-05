# simple-pyThingsboard
This is the simple python thingsboard library which push data to thingsboard

# Example Python Code
```py
import time

# Importing the library
from cenz_thingsboard import thingsboard_MQTT
# or
from cenz_thingsboard import thingsboard_HTTPs

# pick one
tb = thingsboard_MQTT(SERVER="demo.thingsboard.io", ACCESS_TOKEN="qwertyuiopdfghcvbfgt")
tb = thingsboard_HTTPs(SERVER="demo.thingsboard.io", ACCESS_TOKEN="qwertyuiopdfghcvbfgt")
tb = thingsboard_HTTPs(SERVER="demo.thingsboard.io", ACCESS_TOKEN="qwertyuiopdfghcvbfgt", HTTPs = "http", PORT = 80)

# sending data
payload = {}
payload["time"] = time.asctime( time.localtime(time.time()) )
payload["test"] = 10010
tb.push(payload)
```
