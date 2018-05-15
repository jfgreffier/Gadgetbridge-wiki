This page holds specifics to the "[Bluetooth Low Energy](https://en.wikipedia.org/wiki/Bluetooth_Low_Energy)" (BTLE) devices of Pebble – meaning all Pebble 2 variants, but also your other Pebble should you use it in that mode (e.g. the Pebble Time Steel also supports BTLE).

### Pairing a Pebble BTLE
You should **NOT** pair a BTLE device via Android's Bluetooth settings. If you already did so and ran into problems with it in Gadgetbridge (which you certainly will if you did), first step is to "forget the device" – that is the Pebble in Android's Bluetooth settings as well as the Android device in the Pebble's settings. Instructions quoted from [this comment](https://github.com/Freeyourgadget/Gadgetbridge/issues/1098#issuecomment-389128938):

> * set/keep the client only option enabled
> * forget the Pebble (on the android device) and the android device (on the pebble)
> * toggle bluetooth on both pebble and android
> * add the pebble again (pressing the + button in gadgetbridge)
