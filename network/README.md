# Gary Bussy Network Specification

My bus has several networked devices requiring a robust setup, especially considering the automation devices baked into the build. My main intent has been to reduce the ammount of devices on Wifi for reliability and security reasons. 

## Goals

Ultimately I'd like changing locations / traveling to not be a major hassle in terms of making changes to my network. Double/Tripple NAT situations are unfortunate, but is an expectation at this point.

I really like the Gl.iNet travel router concept that offers you the option of connecting to existing newtorks, while keeping your own DCHP server. LTE modem, Tethering, Wifi, and Ethernet being the featured ways to connect when loggin into the admin panel and its very easy to switch between them. Especially the Wifi bridge, which I have yet to figure out how to setup on my Mikrotik... or do so without breaking other things.

Mikrotik RouterOS is extremely powerful, but there is a significant learning curve, so I may be switching amongst my routers for a bit.

## 4G Mast

When I visited New Mexico, I realized I needed to do something to improve my singal and landed on getting a weather resistant router that can be powered by PoE and accept directional antennas.

This feels way better than sending 30 feet of antenna coax down the mast to lose the signal I was trying to gain.

The mast is a sectioned 30-foot flagpole I found on Amazon and I have two Proxicast LPDA Antennas. It is mounted to a chamfered section of the body with a mount that is half commercial and half 3D printed in PETG.

It doesn't need any extra stowing other than full retraction before driving.

### City Mode

When I'm in the city or otherwise have decent connection, I have two omnidirectional antennas magneted on the roof of the bus. This is getting a slight change from magnetic antennas to antennas that are fixed to the front solar panels after a solar reconfiguration/upgrate is complete.


## ISP

`Calyx Institute` provides unlimited LTE data for a $150/quarter membership fee and runs on the `T-Mobile` network. They also offer a yearly plan for $400 and a more expensive plan that includes 5G
Phone is on `Visible` which is a `Verizon` pre-pay service that offers unlimited service for $25-$40/mo (more people in party pay makes it cheaper). Unlimited tethering/hotspot is offered with a bandwidth cap of 5Mb/s - makes a good backup.

## Routers & Modems

There are currently 4 routers that I rotate thru with the hope of making the `Mikrotik wAP R AC` the default for as many situations as possible.

In order of importance:
- Mikrotik wAP R AC
- GL.iNet x750 Spitz
  - Easy setup of Double NAT Wi-Fi
  - Custom OpenWRT build
- Mikrotik LtAP Mini - GPS on PCB
- Raspberry Pi 3B w/ PoE & LTE mPCIE HATs
  - Running Rooter GoldenOrb (OpenWRT)

Current modems are mPCIE configuration and can be swapped into any of the above routers

- Quectel EC25-AF(FA) `LTE4`
  - Has some issues on Mikrotik RouterOS
  - Has band 71 for rural T-Mobile data
- Mikrotik R11e-LTE6 `LTE6`
  - Came with Mikrotik SXT-LTE6 which I intend to sell
  - No GPS
  - Carrier Aggregation

**Want Sierra Wireless MC7411** - `LTE7` Has band 71, carrier aggregation and GPS for reasonable price (about $130) and will likely replace both of the above cards.


**NOTE**: It's actually really odd for an LTE card to not have GPS Mikrotik seems to be the only manufactuer who does this. Feel free to ask me about the several months worth of research I did on LTE internet not just since getting the bus, but I went pretty deep when I was in New Mexico.

## Switches

- Unifi Switch Lite 16 PoE
  - Modified with DC Boost Converter - Can accept 9~48v via Anderson Powerpole Connection
- D-Link 8 Port Unmanaged Switch
  - Supplies various items on Desk


## Wireless APs

- Mikrotik wAP R AC  `Main`
- Unifi AP AC LR `Backup`


## Wired Devices

- 4x WT32-ETH01 by WirelessTag
  - ESPHome
- Raspi 4b+ 2gb
  - Home Assistant
- Raspi 3b
  - Klipper (Ender 3 V2)
- Rando 4 Channel AHD DVR
  - Soon to be replaced?
- Mac Mini M1
  - 'Mato Mini' M1 Home Server Project
- Macbook Pro 14" `Sometimes` 

## Wireless Devices

### WiFi
- Macbook Pro 14
  - Base Model - Refurbished
  - Space Gray
- iPad Pro 2020 - 11"
- iPhone X
- HomePod Mini - Orange
- Chromecast w/ GoogleTV 4k

### Zigbee
- Aquara
  - Motion Sensor
  - Vibration Sensor
  - Door/Window Sensor
  - 2x Smart Plug w/ Energy Monitoring
- Tuya or clone
  - Smoke Alarm `Disconnected Temporarily`
  - 2x2 Wall Remote
- Unknown
  - DIN Rail Energy Monitor / Switch `Not Yet Installed`
    - For Shore/Generator - replaces 1x Aquara smart plug


