## CAUTION
This feature is currently highly discouraged, as it has the potential to brick the Mi Band! That said, we this has never happened to any of the developers, but remember you're doing this on your own risk.

## Getting the Firmware
Since we may not distribute the firmware, you have to do a little work. You need to find and download a MiFit APK file. There is an APK Mirror Web site that might help you find MiFit. Extract the downloaded .apk file with "unzip", and you will find an `assets/` directory containing `*.fw` files, among others.

Next, you need to find out, which of the `*.fw` files you need.

## Mi Band Model
Which Mi Band do you have? There are 3 different models and each of them needs a different `*.fw` file.

1. Model 1 (coloured LEDs): `Mili.fw`

2. Model 1A (white LEDs): `Mili_1a.fw`

3. Model 1S (white LEDs + heart rate sensor): `Mili_hr.fw`

## Installing the Firmware
Copy the desired Mi Band firmware as a `*.fw` file to your Android device and open it from any file manager on that device. The Gadgetbridge firmware update activity should then be started and guide you through the installation process.