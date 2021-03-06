
<!--
# license: Licensed to the Apache Software Foundation (ASF) under one
#         or more contributor license agreements.  See the NOTICE file
#         distributed with this work for additional information
#         regarding copyright ownership.  The ASF licenses this file
#         to you under the Apache License, Version 2.0 (the
#         "License"); you may not use this file except in compliance
#         with the License.  You may obtain a copy of the License at
#
#           http://www.apache.org/licenses/LICENSE-2.0
#
#         Unless required by applicable law or agreed to in writing,
#         software distributed under the License is distributed on an
#         "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
#         KIND, either express or implied.  See the License for the
#         specific language governing permissions and limitations
#         under the License.
-->

# cordova-plugin

This plugin defines a global `device` object, which describes the device's hardware and software.
Although the object is in the global scope, it is not available until after the `deviceready` event.

Straight copy from apache cordova sample - used to extend

```js
plugman install --platform android --project . --plugin cordova-plugin

plugman uninstall --platform android --project .--plugin cordova-plugin
```

```js
document.addEventListener("deviceready", onDeviceReady, false);
function onDeviceReady() {
    console.log(mydevice.cordova);
}
```

## Installation

    cordova plugin add cordova-plugin

## Properties

- mydevice.cordova
- mydevice.model
- mydevice.platform
- mydevice.uuid
- mydevice.version
- mydevice.manufacturer
- mydevice.isVirtual
- mydevice.serial

## mydevice.cordova

Get the version of Cordova running on the device.

## mydevice.model

The `mydevice.model` returns the name of the device's model or
product. The value is set by the device manufacturer and may be
different across versions of the same product.

### Quick Example

```js
var model = mydevice.model;
```

### Quirks

- Gets the [product name](http://developer.android.com/reference/android/os/Build.html#PRODUCT) instead of the [model name](http://developer.android.com/reference/android/os/Build.html#MODEL), which is often the production code name. For example, the Nexus One returns `Passion`, and Motorola Droid returns `voles`.

## mydevice.platform

Get the device's operating system name.

```js
var string = mydevice.platform;
```

### Quick Example

```js
var devicePlatform = mydevice.platform;
```

## mydevice.uuid

Get the device's Universally Unique Identifier ([UUID](http://en.wikipedia.org/wiki/Universally_Unique_Identifier)).

```js
var string = mydevice.uuid;
```

### Description

The details of how a UUID is generated are determined by the device manufacturer and are specific to the device's platform or model.


### Quick Example

```js
var deviceID = mydevice.uuid;
```

## mydevice.version

Get the operating system version.

    var string = mydevice.version;


### Quick Example

```js
var deviceVersion = mydevice.version;
```

## mydevice.manufacturer

Get the device's manufacturer.

    var string = mydevice.manufacturer;


### Quick Example

```js
var deviceManufacturer = mydevice.manufacturer;
```

## mydevice.isVirtual

whether the device is running on a simulator.

```js
var isSim = mydevice.isVirtual;
```

## mydevice.serial

Get the device hardware serial number ([SERIAL](http://developer.android.com/reference/android/os/Build.html#SERIAL)).

```js
var string = mydevice.serial;
```
