![Logo](admin/intel.png)
ioBroker Intel NUC-Monitor Adapter
==============

[![NPM version](http://img.shields.io/npm/v/iobroker.nuc.svg)](https://www.npmjs.com/package/iobroker.nuc)
[![Downloads](https://img.shields.io/npm/dm/iobroker.nuc.svg)](https://www.npmjs.com/package/iobroker.nuc)

[![NPM](https://nodei.co/npm/iobroker.nuc.png?downloads=true)](https://nodei.co/npm/iobroker.nuc/)

Intel NUC-Monitor implementation for integration into ioBroker (forked from RPI-Monitor). It is the same implementation as for iobroker.rpi2, but without GPIOs.

## Important Information
Works only with node >= 0.12

## Installation
After installation you have to configure all required modules via administration page.

After start of iobroker.nuc, all selected modules generates
an object tree in ioBroker within nuc.<instance>.<modulename>
e.g. nuc.0.cpu

Be sure, that python and build-essential are installed:

```
sudo apt-get update
sudo apt-get install -y build-essential python
```

Following Objects are available after selection:

#### **CPU**

- cpu_frequency
- load1
- load5
- load15

#### **Memory**

- memory_available
- memory_free
- memory_total

#### **Network (eth0)**
- net_received
- net_send

#### **SDCard**
- sdcard_boot_total
- sdcard_boot_used
- sdcard_root_total
- sdcard_root_used

#### **Swap**
- swap_total
- swap_used

#### **Temperature**
- soc_temp

#### **Uptime**
- uptime

#### **WLAN**
- wifi_received
- wifi_send

## Configuration
On configuration page you can select following modules:

- CPU
- Memory
- Network
- SDCard
- Swap
- Temperature
- Uptime
- WLAN

## Logfiles / Configuration Settings

## Features

## Todo
 - Make an Optionfield for the Network Settings to switch between the old end new Networknames under Debian.
 
## Tested Hardware
 - Intel NUC

## Changelog

### 0.1.0 (2017-10-16)
 - Initial fork from rpi2. Alpha Version.

## License

Copyright (c) 2015-2016 husky-koglhof <husky.koglhof@icloud.com>
Copyright (c) 2017 t.enkelmann@web.de

MIT License
