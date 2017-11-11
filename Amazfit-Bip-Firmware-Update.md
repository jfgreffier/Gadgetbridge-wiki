## CAUTION
This feature **has the potential to brick your Anazefit Bip**! That said, this has never happened to any of the developers, but remember **you're doing this at your own risk**.

## Getting the firmware
Since we may not distribute the firmware, you have to do a little work. You need to find and download a Mi Fit APK file. There is an APK Mirror Web site that might help you find Mi Fit. Extract the downloaded .apk file with "unzip", and you will find an `assets/` directory containing `*.fw` files, among others.

Next, you need to find out, which of the `*.fw` files you need.

## Amazfit Bip model
Currently we are aware of only one Amazfit Bip hardware version. If new version are released, different models might need a different `*.fw` file.

The Amazfit Bip requires the  `Mili_chaohu.*` files.

## Installing the firmware on Amazfit Bip models
Copy the desired Amazfit Bip firmware and ressource files as a `*.gps`, `*.res` and `*.fw` file to your Android device and open it from any file manager on that device. The Gadgetbridge FW/App Installer activity should then be started and guide you through the installation process.

### Recommended flashing order:
1. Mili_chaohu.gps
1. Mili_chaohu.res
1. Mili_chaohu.fw

Flash the `*.fw` file last because it triggers a reboot. After flashing the `*.gps` and `*.res` files do not touch your device - just continue flashing.

**Note 1:** Both upgrade and downgrade of firmware versions is possible.

Starting with Firmware version 0.0.9.14 the Amazfit Bip supports English text notifications. In order to get it working you need to have Gadgetbridge version >=0.22.2. If the desired language is not shown  automatically, you can select it in at Settings->Amazfit Bip Settings->Language after installing the corresponding firmware file.

**Note 2:** After flashing to a 0.0.9.x release the first time coming from prior versions you have to remove the pairing in Android Bluetooth settings, then press the + button in Gadgetbridge to pair again.

## Known firmware Versions

0.0.7.90 (Tested, pre-installed with watches manufactured July 2017)

0.0.8.20 (Untested, included in Mifit 3.0.2)

0.0.8.32 (Untested, included in Mifit 3.0.4)

0.0.8.74 (Tested, included in Mifit 3.0.5, deep sleep detection does not work with Gadgetbridge)

0.0.8.88 (Tested, slow UI, included in Mifit 3.0.7, deep sleep detection does not work with Gadgetbridge)

0.0.8.96 (Tested, OTA Update, deep sleep detection does not work with Gadgetbridge)

0.0.8.97 (Tested, OTA Update, deep sleep detection does not work with Gadgetbridge)

0.0.8.98 (Tested, OTA Update, deep sleep detection does not work with Gadgetbridge)

**WITH ENGLISH LANGUAGE FROM HERE ON**

0.0.9.14 (Tested, included in Mifit 3.1.0, deep sleep detection does not work with Gadgetbridge)

0.0.9.26 (Tested, included in Mifit 3.1.2, deep sleep detection does not work with Gadgetbridge, connection drops with some phones)
