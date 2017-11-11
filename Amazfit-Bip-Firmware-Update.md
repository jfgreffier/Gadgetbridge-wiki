## CAUTION
This feature **has the potential to brick your Anazefit Bip**! That said, this has never happened to any of the developers, but remember **you're doing this at your own risk**.

## Getting the firmware
Since we may not distribute the firmware, you have to do a little work. You need to find and download a Mi Fit APK file. There is an APK Mirror Web site that might help you find Mi Fit. Extract the downloaded .apk file with "unzip", and you will find an `assets/` directory containing `*.fw` files, among others.

Next, you need to find out, which of the `*.fw` files you need.

## Amazfit model
Currently we are aware of only one Amazfit Bip hardware version. If new version are released, different models might need a different `*.fw` file.

1. Model Bip: `Mili_chaohu.fw`
   You need to install these three files in this order:
   * Mili_chaohu.gps
   * Mili_chaohu.res
   * Mili_chaohu.fw


## Known firmwares' md5
As mentioned above, we are not allowed to distribute firmware files, these md5 values may be used to check if the firmware file you obtained is valid/is not corrupted.
**To check the md5 you may use the command `md5sum` on a GNU/Linux distribution.**

1. Model Bip: 
 * Files included in Mifit 3.1.3
   * `Mili_chaohu.gps` - 97f9794cc46b2ebddaa0b52fe27a4f8f
   * `Mili_chaohu.res` - 7099605b7e062645476f6b8bb815f6fb
   * `Mili_chaohu.fw`  - fae9548f699ede59687b219a20e6e70d

## Installing the firmware on Amazfit Bip models
Copy the desired Amazfit Bip firmware and ressource files as a `*.gps`, `*.res` and `*.fw` file to your Android device and open it from any file manager on that device. The Gadgetbridge FW/App Installer activity should then be started and guide you through the installation process.

### Recommended flashing order:
1. Mili_chaohu.gps
1. Mili_chaohu.res
1. Mili_chaohu.fw

Flash the `*.fw` file last because it triggers a reboot. After flashing the `*.gps` and `*.res` files do not touch your device - just continue flashing.

**Note 1:** Both upgrade and downgrade of firmware versions is possible.

Starting with Firmware version 0.0.9.14 the Amazfit Bip supports English text notifications. In order to get it working you need to have Gadgetbridge version >=0.22.2 and select the language in the settings->Amazfit Bip Settings->Language  after installing the corresponding firmware file.

**Note 2:** After flashing to a 0.0.9.x release the first time coming from prior versions you have to remove the pairing in Android Bluetooth settings, then press the + button in Gadgetbridge to pair again.