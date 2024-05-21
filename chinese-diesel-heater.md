---
description: Mostly BLE reference for BLE Controller With Knob
---

# Chinese Diesel Heater

## Reference

[https://github.com/iotmaestro/vevor-heater-ble](https://github.com/iotmaestro/vevor-heater-ble) - BLE Schema

[https://github.com/spin877/Bruciatore\_BLE](https://github.com/spin877/Bruciatore\_BLE) - Base for ESPHome YAML

## Bluetooth Controller w/ Knob

Press & Hold GEAR

### Settings

* 00 - Time
* 01 - Auto Start Time
* 02 - Run for X time after start
* 03 - Auto start - on/off
* 04 - Voice Setting off/chinese/english/russian
* 05 - Temperature Compensation?
* 06 - Fuel Tank Size (for fuel display) 0-50L
* 07 - Fuel Pump Size (Units per pulse)
* 08 - Auto Mode on/off

### Engineering mode

While ON: Press and hold GEAR+POWER

* EN01 - Fault Codes
* EN02 - Housing Temp
* EN03 - Voltage
* EN04 - Heater Operation (Level???)
* EN05 - Cab Temp
* EN06 - Altitude
* EN07 - Pump Mode?
* EN08 - Remote Matching - hold knob button then press 1-4 on remote
* EN09 - BLE MAC (Last 4 digits)

### Reset Tank

While off - press and hold fuel button for 7 seconds



### Logic



