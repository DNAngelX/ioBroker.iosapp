![Logo](admin/iosapp.png)
# ioBroker.iosapp

[![NPM version](https://img.shields.io/npm/v/iobroker.iosapp.svg)](https://www.npmjs.com/package/iobroker.iosapp)
[![Downloads](https://img.shields.io/npm/dm/iobroker.iosapp.svg)](https://www.npmjs.com/package/iobroker.iosapp)
![Number of Installations](https://iobroker.live/badges/iosapp-installed.svg)
![Current version in stable repository](https://iobroker.live/badges/iosapp-stable.svg)

[![NPM](https://nodei.co/npm/iobroker.iosapp.png?downloads=true)](https://nodei.co/npm/iobroker.iosapp/)

**Tests:** ![Test and Release](https://github.com/DNAngelX/ioBroker.iosapp/workflows/Test%20and%20Release/badge.svg)

## iOS App Adapter for ioBroker

The iOSAppAdapter integrates your iOS devices with ioBroker, allowing seamless communication and data exchange through WebSockets. This adapter supports device data synchronization, real-time notifications, and device status monitoring.

### Features

- **WebSocket Integration**: Establishes a WebSocket server for real-time communication between ioBroker and iOS devices.
- **Device Management**: Manage and monitor multiple iOS devices and their statuses.
- **Real-time Notifications**: Send notifications to iOS devices.
- **Persistent Messaging**: Queues messages for offline devices and delivers them when they reconnect.
- **Connection Monitoring**: Regularly pings devices to ensure active connections and updates their status accordingly.

### Configuration

To configure the iOSAppAdapter, you need to provide the following settings:

- **Username**: The username for authentication.
- **Password**: The password for authentication.
- **WebSocket Port**: The port on which the WebSocket server will listen (default: 9192).

### Object Structure

The adapter creates and manages objects under the `iosapp` namespace. The object structure is as follows:

- `iosapp.0.person.<person>.<device>.ws_device_id`: Stores the WebSocket device ID.
- `iosapp.0.person.<person>.<device>.connection`: Indicates the connection status (true/false).
- `iosapp.0.messages`: General messages sent to all devices.
- `iosapp.0.person.<person>.messages`: Messages specific to a person.
- `iosapp.0.person.<person>.<device>.messages`: Messages specific to a person's device.


## Changelog
<!--
    Placeholder for the next version (at the beginning of the line):
    ### **WORK IN PROGRESS**
-->
### 1.0.1 (2024-07-31)
* (DNAngelX) Websocket disconnection fix

### 1.0.0 (2024-07-30)
* (DNAngelX) Stable BETA Release
* (DNAngelX) Messanges fix
* (DNAngelX) changed namespace
* (DNAngelX) online state for single devices fix

### 0.2.1 (2024-07-19)
* (DNAngelX) UI Fix

### 0.2.0 (2024-07-19)
* (DNAngelX) Change Rest 2 Websockets
* Improvements in Cache Messages etc.

### 0.1.0 (2024-07-07)
* (DNAngelX) Apple Push Service APN added

### 0.0.6 (2024-07-06)
* (DNAngelX) integration checks: true

### 0.0.5 (2024-07-06)
* (DNAngelX) bugfix ws

### 0.0.3 (2024-07-06)
* (DNAngelX) bugfix ports

### 0.0.2 (2024-07-01)
* (DNAngelX) initial release

## License
MIT License

Copyright (c) 2024 DNAngelX <stolly82@web.de>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
