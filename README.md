# Purpose

Associate a Broadlink RM4 Mini with an AP without needing the Broadlink app

# Usage

```sh
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
git submodule update --init

# * Connect a new RM4 mini to a decent USB charger. Samsung fast chargers don't
#   work; the device will blink but never announce an AP
#
# * Wail until the RM4 Mini announces a Broadlink_Wifi_Device AP
# 
# * Connect to that AP
#
# * Run the following command where $SSID and $PASSWORD are the credentials for
#   a 2.4 GHz AP to which you want the RM4 Mini to associate
./python-broadlink/cli/broadlink_cli --joinwifi $SSID $PASSSWORD

# * Confirm that Broadlink_Wifi_Device AP has now disappeared
#
# * If using homeassistant, refer to this guide to start teaching commands:
#   https://www.youtube.com/watch?v=0WzRyjs8Ws0
```