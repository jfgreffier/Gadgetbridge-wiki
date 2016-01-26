# Short Introduction to Gadgetbridge's Source Code:
## Important Classes
- PebbleSupport (see class hierarchy)
- PebbleIOThread
- MiBandSupport (see class hierarchy)
- BtLEQueue (communication queue for Bluetooth LE devices)
- DeviceCommunicationService (Android service channeling the communication with devices)
- DeviceService ("client side API" of DeviceCommunicationService, see GBApplication#deviceService())
- GBDevice (generic, device-unspecific)
- DeviceCoordinator (see class hierarchy)
- ControlCenter (main activity)

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