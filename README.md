# Telegraf Importer for the Huawei HG612 modem

**Note:** For this to work you will need a HG612 modem with unlocked firmware to allow Telnet access. **This is done at your own risk.**      
See: https://kitz.co.uk/routers/hg612unlock.htm for flashing instructions and firmware

## Stats collected:

* Attenuation downstream
* Attenuation upstream
* Available seconds
* Current downstream speed
* Current upstream speed
* Error seconds (downstream)
* Error seconds (upstream)
* Max downstream speed
* Max upstream speed
* Power (downstream)
* Power (upstream)
* Serious error seconds (downstream)
* Serious error seconds (upstream)
* SNR (downstream)
* SNR (upstream)
* System (modem) uptime
* Unavailable seconds (downstream)
* Unavailable seconds (upstream)

## Configure
## Docker Configuration
See here: https://github.com/djrarky/telegraf-python3#configure

### Telegraf Setup
```
[[inputs.exec]]
  ## Commands array
  commands = ["python3 location/telegraf-huawei-lte.py 'http://username:password@IP Address/'"]

  ## measurement name suffix (for separating different commands)
  name_suffix = "_mycollector"

  ## Data format to consume.
  data_format = "influx"
