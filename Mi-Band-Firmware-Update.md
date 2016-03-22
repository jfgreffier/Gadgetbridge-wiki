## CAUTION
This feature is currently highly discouraged, as it has the potential to brick the Mi Band! That said, we this has never happened to any of the developers, but remember you're doing this on your own risk.

## Getting the Firmware
Since we may not distribute the firmware, you have to do a little work. You need to find and download a MiFit APK file. There is an APK Mirror Web site that might help you find MiFit. Extract the downloaded .apk file with "unzip", and you will find an `assets/` directory containing `*.fw` files, among others.

Next, you need to find out, which of the `*.fw` files you need.

## Mi Band Model
Which Mi Band do you have? There are 3 different models and each of them needs a different `*.fw` file.

1. Model 1 (coloured LEDs): `Mili.fw`

1. Model 1A (white LEDs): `Mili_1a.fw`

1. Model 1S (white LEDs + heart rate sensor): `Mili_hr.fw`

## Known firmwares' md5
As mentioned above, we are not allowed to distribute firmware files, these md5 values may be used to check if the firmware file you obtained is valid/is not corrupted.
**To check the md5 you may use the command `md5sum` on a linux computer.**

1. Model 1 (coloured LEDs): `Mili.fw`
 * 01.00.10.14 - 1c43d7f03c911f9ba8844ddd44bd8304
 * 01.00.11.06 - 2833690a70ec8c6699ccd3ac08b933cc
 * 01.00.12.00 - 3a941165b7b4e296ecd68cdfb0e01062

1. Model 1A (white LEDs): `Mili_1a.fw`
 * 05.15.11.20 - 356a8e1f006c541b76b306d4dbfbfaea
 * 05.15.12.10 - bbb904842a807acf1e2be5e2b41d888b

1. Model 1S (white LEDs + heart rate sensor): `Mili_hr.fw`
 * 04.15.11.20 - 7be80f0061efdf660e25a2d7cb3b6660
 * 04.15.12.10 - 24d8b84f8964489b893d1cb4581dc85f

## Installing the Firmware
Copy the desired Mi Band firmware as a `*.fw` file to your Android device and open it from any file manager on that device. The Gadgetbridge firmware update activity should then be started and guide you through the installation process.

Note that both upgrade and downgrade of firmware versions is possible.