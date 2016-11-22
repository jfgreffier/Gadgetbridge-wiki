# Development Environment
The core team uses Debian GNU/Linux + [Android Studio](https://developer.android.com/studio/index.html) 2.2 (as of November 2016). It is also available for Windows and Mac, but we never used that.
You can use any Android device connected to USB to run your code straight from Android Studio on the device. Be aware that you cannot install your own built version and F-Droid's at the same time. You can export and import your database, though.

If you only want to compile the code, you can simply execute
```./gradlew assembleDebug```
or
```./gradlew assembleRelease```

# Short Introduction to Gadgetbridge's Source Code
## Important Classes
- [PebbleSupport] (https://github.com/Freeyourgadget/Gadgetbridge/blob/master/app/src/main/java/nodomain/freeyourgadget/gadgetbridge/service/devices/pebble/PebbleSupport.java) (see class hierarchy)
- [PebbleProtocol] (https://github.com/Freeyourgadget/Gadgetbridge/blob/master/app/src/main/java/nodomain/freeyourgadget/gadgetbridge/service/devices/pebble/PebbleProtocol.java) (pebble communication protocol)
- [PebbleIOThread] (https://github.com/Freeyourgadget/Gadgetbridge/blob/master/app/src/main/java/nodomain/freeyourgadget/gadgetbridge/service/devices/pebble/PebbleIoThread.java) (background thread for pebble communication)
- [MiBandSupport] (https://github.com/Freeyourgadget/Gadgetbridge/blob/master/app/src/main/java/nodomain/freeyourgadget/gadgetbridge/service/devices/miband/MiBandSupport.java) (see class hierarchy)
- [BtLEQueue] (https://github.com/Freeyourgadget/Gadgetbridge/blob/master/app/src/main/java/nodomain/freeyourgadget/gadgetbridge/service/btle/BtLEQueue.java) (communication queue for Bluetooth LE devices)
- [DeviceCommunicationService] (https://github.com/Freeyourgadget/Gadgetbridge/blob/master/app/src/main/java/nodomain/freeyourgadget/gadgetbridge/service/DeviceCommunicationService.java) (Android service channeling the communication with devices)
- [DeviceService] (https://github.com/Freeyourgadget/Gadgetbridge/blob/master/app/src/main/java/nodomain/freeyourgadget/gadgetbridge/model/DeviceService.java) ("client side API" of DeviceCommunicationService, see [GBApplication#deviceService()] (https://github.com/Freeyourgadget/Gadgetbridge/blob/master/app/src/main/java/nodomain/freeyourgadget/gadgetbridge/GBApplication.java#L156))
- [GBDevice] (https://github.com/Freeyourgadget/Gadgetbridge/blob/master/app/src/main/java/nodomain/freeyourgadget/gadgetbridge/impl/GBDevice.java) (generic, device-unspecific)
- [DeviceCoordinator] (https://github.com/Freeyourgadget/Gadgetbridge/blob/master/app/src/main/java/nodomain/freeyourgadget/gadgetbridge/devices/DeviceCoordinator.java) (see class hierarchy)
- [ControlCenter] (https://github.com/Freeyourgadget/Gadgetbridge/blob/master/app/src/main/java/nodomain/freeyourgadget/gadgetbridge/activities/ControlCenter.java) (main activity)

## Overview
![Overview UML Component Diagram](https://github.com/Freeyourgadget/Gadgetbridge/blob/master/app/src/main/assets/devintro.png)

All the details about the communication/protocol with a concrete device (Pebble, Mi Band, ...) is inside the "Concrete Device Impl." component, that is, the concrete implementations of the `DeviceSupport` interface. Only the `DeviceCommunicationService` has access to those -- clients (typically Activities) talk to the `DeviceService` interface in order to communicate with the devices.

### Extracting CSV Data from the SQLite Database

```
$ sqlite3 ActivityDatabase <<!
> .headers on
> .mode csv
> .output out.csv
> select * from GBActivitySamples;
> !
```

taken from [SO](http://stackoverflow.com/questions/5776660/export-from-sqlite-to-csv-using-shell-script).

### Bluetooth Error Codes
https://android.googlesource.com/platform/external/bluetooth/bluedroid/+/android-5.1.1_r37/stack/include/gatt_api.h