## CAUTION
This feature **has the potential to brick your Amazfit Cor**! That said, this has never happened to any of the developers, but remember **you're doing this at your own risk**.

## Getting the firmware
Since we may not distribute the firmware, you have to do a little work. You need to find and download a Mi Fit APK file. There is an APK Mirror Web site that might help you find Mi Fit. Extract the downloaded .apk file with "unzip", and you will find an `assets/` directory containing `*.fw` files, among others.

The Amazfit Cor requires the  `Mili_tempo.*` files. For **tested versions** and **known issues** check [below](#known-firmware-versions).

## Installing the firmware
Copy the desired Amazfit Cor firmware and resource files as a `*.res` and `*.fw` file to your Android device and open it from any file manager on that device. The Gadgetbridge FW/App Installer activity should then be started and guide you through the installation process.

### Recommended flashing order:
1. Mili_tempo.fw
2. Mili_tempo.res (The Cor will tell you when needed)

Flashing the `*.fw` triggers a reboot and will show a screen which will ask you to flash the .res if your version is outdated.

**Note 1:** Both upgrade and downgrade of firmware versions is possible.


## Known firmware Versions

Original Firmware Version: ?.?.?.??

fw ver    | MiFit ver | tested | known&nbsp;issues | res ver | gps ver | fw-md5 | res-md5 | gps-md5
----------|-----------|--------|-------------------|---------|---------|--------|---------|--------
