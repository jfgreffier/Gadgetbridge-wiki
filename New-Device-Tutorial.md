# Supporting a new device in Gadgetbridge

This is a step by step tutorial for supporting a new device in Gadgetbridge. There are some differences depending on the transport layer being used (Bluetooth Classic, Bluetooth LE, WiFi, ...), but most of it is independent of that. The tutorial only covers the basics to get you started quickly. For more details, have a look at the existing implementations for other devices. Try to do your implementation in a similar way (where it makes sense), so as to ease maintenance.

See [Appendix: Infrastructure](#appendix-infrastructure) for some general implementation topics and [[Developer-Documentation]] for an overview into Gadgetbridge's inner workings and important classes.

Before going into the details, let's have a short look at the process the user has to go through in order to connect a new device.
<pre>
Start Device Discovery
  -> Select one of the displayed devices
    -> If necessary: pair/authenticate with the device
      -> If necessary: provide certain settings like nick name, age, height, ...
        -> Initialize the device
          -> Device can be used
</pre>

For this tutorial we will add support for the exemplary SuperBand 4000 device, so many things are named after that.

## Part 1: Discovery
The first part deals with discovering SuperBand 4000 devices and telling Gadgetbridge that/how they are supported.

1. Add a new device type constant SUPERBAND_4000 to `nodomain.freeyourgadget.gadgetbridge.model.DeviceType`. Pick a new number as the `key` and leave 10 numbers "room" to the last number. These are reserved so that related devices can have nearby numbers.
Also specify a default icon (coloured) and a disabled icon (greyscale). If you don't have any yet, reuse some other icons.
2. Create a new package `nodomain.freeyourgadget.gadgetbridge.devices.superband4000`.
3. In that package, create a class `SuperBand4000DeviceCoordinator` that extends `nodomain.freeyourgadget.gadgetbridge.devices.AbstractDeviceCoordinator`. This class tells Gadgetbridge whether a discovered device is supported and what features are supported (with the implementation in Gadgetbridge, not in general).
    1. Implement the method `getDeviceType()` and return the constant `DeviceType.SUPERBAND_4000` that you previously added.
    2. If your device is a Bluetooth LE device, override the method `createBLEScanFilters()` and return a list of `ScanFilter`s for recognizing your device during discovery by a Bluetooth service UUID for example. You can skip this if you cannot or don't know how to recognize your device that way yet.
    3. Implement the method `DeviceType getSupportedType(GBDeviceCandidate candidate)`. This method will be called during discovery in order to check wether the discovered device is supported by Gadgetbridge. To decide this, you might check further services, the MAC address, or even the device name if you don't know a better way, yet. If you're determined to support the given device candidate, you return the recognized `DeviceType`. Typically this is the one that you return in `getDeviceType()`. If you do *not* recognize the given candidate, return `DeviceType.UNKNOWN` so that another `DeviceCoordinator` can be asked.
    4. Implement `getBondingStyle()` depending on how your device needs to be paired on the Bluetooth level. Return `BONDING_STYLE_BOND` to perform BLE pairing, `BONDING_STYLE_ASK` to let the user decide that during discovery, or `BONDING_STYLE_NONE` to not perform BLE pairing at all.
    5. If your device needs some very special kind of pairing/bonding/authentication before it can be used, you may override the method `getPairingActivity()` in which you return an `Activity` class that will be shown for your device after the device discovery process. Otherwise, just return `null`.
    6. There are several more methods that you need to implement, mostly `supportsXXX()` where `XXX` is a certain feature a device may support or not. As soon as you implement support for one such feature, make sure to announce it by returning `true` in the corresponding `supportsXXX()` method. Otherwise the feature will not be available in Gadgetbridge.
4. Register your `SuperBand4000DeviceCoordinator` class with `nodomain.freeyourgadget.gadgetbridge.util.DeviceHelper#createCoordinators()` so that it will be used.

So, that was the first part. With these changes, Gadgetbridge should be able to find and display your device in the Discovery view. If that is not the case, add breakpoints in your device coordinator's `getSupportedType()` method to find out why. Also check the `ScanFilter`s, if any. Only once your device is found and displayed during discovery, does it make sense to continue with the next steps.

## Part 2: Communication
The next part deals with the communication between Gadgetbridge and your device. This part is very specific to the device and the communication protocol being used.

This code lives in a separate package because it is used by a contiuously running background `Service`. This service is the `nodomain.freeyourgadget.gadgetbridge.service.DeviceCommunicationService`.

1. Create the package `nodomain.freeyourgadget.gadgetbridge.service.devices.superband4000`
2. Create a `SuperBand4000DeviceSupport` class in that package. As the super class, choose one of the existing abstract classes like `nodomain.freeyourgadget.gadgetbridge.service.serial.AbstractSerialDeviceSupport` or `nodomain.freeyourgadget.gadgetbridge.service.btle.AbstractBTLEDeviceSupport`, depending on the transport layer.
3. Edit `nodomain.freeyourgadget.gadgetbridge.service.DeviceSupportFactory#createBTDeviceSupport()` and add the code to instantiate your support class for `DeviceType.SUPERBAND_4000`.

## Bluetooth Classic
For Bluetooth Classic with `AbstractSerialDeviceSupport` as super class, you will usually create at least two other classes: a `SuperBand4000IOThread` and a `SuperBand4000Protocol`.

* The `*IOThread` class manages the Bluetooth rfcomm socket in a non-blocking way for callers.
* The `*Protocol` class understands and handles the incoming and outgoing messages.

## Bluetooth LE
For Bluetooth LE, you will use the `nodomain.freeyourgadget.gadgetbridge.service.btle.Transaction` and `nodomain.freeyourgadget.gadgetbridge.service.btle.BtLEQueue` classes to communicate with the device via GATT events. Theses classes will take care of synchronizing everything.

See the subclasses of `nodomain.freeyourgadget.gadgetbridge.service.btle.profiles.AbstractBleProfile` for some ready-to-be-used implementations of standard BLE services/profiles.

## Final Words
We hope that this tutorial will help you get started with adding support for new devices in Gadgetbridge.

For questions and improvements, do not hesitate to contact us!

<pre>
Happy hacking,
the Gadgetbridge Team
</pre>

## Appendix: Infrastructure
### Logging
We use `slf4j` for logging, so just use `LoggerFactory.getLogger(Your.class)` and log away. The output will be written to the Android Log (so you can get it with logcat or Android Studio) as well as to the file `/sdcard/Android/data/nodomain.freeyourgadget.gadgetbridge/files/gadgetbridge.log`. File logging needs to be enabled in Gadgetbridge's preferences, first.

### Information Display
Use one of the `nodomain.freeyourgadget.gadgetbridge.util.GB#toast()` methods to display information to the user. They

- not only display, but also log warnings and errors
- can safely be called from a background thread

### Database
We use `greenDAO` for database access. See `nodomain.freeyourgadget.gadgetbridge.daogen.GBDaoGenerator` for entity definition and generation.
