![Logo](admin/ubuntu.png)
ioBroker Ubuntu-Monitor Adapter
==============

[![NPM version](http://img.shields.io/npm/v/iobroker.ubuntu.svg)](https://www.npmjs.com/package/iobroker.ubuntu)
[![Downloads](https://img.shields.io/npm/dm/iobroker.ubuntu.svg)](https://www.npmjs.com/package/iobroker.ubuntu)
**Tests:** Linux/Mac: [![Travis-CI](http://img.shields.io/travis/indiBit/ioBroker.ubuntu/master.svg)](https://travis-ci.org/indiBit/ioBroker.ubuntu)

[![NPM](https://nodei.co/npm/iobroker.ubuntu.png?downloads=true)](https://nodei.co/npm/iobroker.ubuntu/)

Ubuntu-Monitor implementation for integration into ioBroker (forked from Intel NUC-Monitor). It is the same implementation as for iobroker.nuc, but with adjusted commands for reading values from Ubuntu.

## Important Information
Works only with node >= 0.12

## Installation
After installation you have to configure all required modules via administration page.

After start of iobroker.ubuntu, all selected modules generates
an object tree in ioBroker within ubuntu.<instance>.<modulename>
e.g. ubuntu.0.cpu

Be sure, that python and build-essential are installed:

```
sudo apt-get update
sudo apt-get install -y build-essential python
```

Following Objects are available after selection:

## CPU

- cpu_frequency
- load1
- load5
- load15

## Memory

- memory_available
- memory_free
- memory_total

## Disk (sda1, sda2, sdb1, sdb2, sdc1, sdc2)

- disk_available
- disk_total
- disk_used
- disk_used_percent

## Network
- net_received
- net_send

## Swap
- swap_total
- swap_used

## Temperature
You may need to install lm-sensors to get tempature values
```
sudo apt install -y lm-sensors
sudo sensors-detect
sudo service kmod start
```
Not supportet in virtual environments
- soc_temp

## Uptime
- uptime

## Configuration
On configuration page you can select following modules:

- CPU
- Memory
- Network
- Swap
- Temperature
- Uptime

## Logfiles / Configuration Settings

## Features

## Todo
 - Make an Optionfield for the Network Settings to switch between the old end new Networknames under Debian.
 
## Tested Hardware
 - Ubuntu 18.04.1

## Changelog

### 0.1.0 (2019-01-20)
 - Initial fork from nuc. Alpha Version.

## License

Copyright (c) 2015-2016 husky-koglhof <husky.koglhof@icloud.com>
Copyright (c) 2017 t.enkelmann@web.de
Copyright (c) 2019 sebastian@indibit.de

MIT License
