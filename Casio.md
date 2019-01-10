# Supported Watches and Status

Initial support for Casio watches was done on a GB-X6900B here: [PR 1377](https://github.com/Freeyourgadget/Gadgetbridge/pull/1377). When adding a new watch, it filters only for "CASIO", so other models might be supported as well.

* Casio GB-X6900B: Supported, might take several tries to connect for the first time
* Casio GB-6900B: Should work, please report
* Casio GB-5600B: Should work, please report

# Connecting

Connecting to the watch sometimes takes more than one try, especially, when using the watch for the first time with Gadgetbridge. Be sure to delete the existing pairing from both, the phone and the watch, before adding it to Gadgetbridge.

# Implemented features

* Notifications
* Music Control
* Phone Finder
* Time synchronization

# Missing features

Currently, it is not possible to make any adjustments of the watch (exception: time synchronization) as the official app can do.

# Implementation specific details

The watch seems to always require time synchronization on connecting. Thus, the respective option in Gadgetbridge's settings has no effect for Casio models, the time is always synchronized when requested by the watch.

# Protocol and other models

The implementation for Gadgetbridge is based on Bluewatcher (https://github.com/masterjc/bluewatcher) and additional analysis work. There is no formal specification of the protocol available.