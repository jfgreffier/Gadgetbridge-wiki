## CAUTION
This feature **has the potential to brick your Amazfit Bip**! That said, this has never happened to any of the developers, but remember **you're doing this at your own risk**.

## Getting the firmware
Since we may not distribute the firmware, you have to do a little work. You need to find and download a Mi Fit APK file. There is an APK Mirror Web site that might help you find Mi Fit. Extract the downloaded .apk file with "unzip", and you will find an `assets/` directory containing `*.fw` files, among others.

Next, you need to find out, which of the `*.fw` files you need.

## Amazfit Bip model
Currently we are aware of only one Amazfit Bip hardware version. If new version are released, different models might need a different `*.fw` file.

The Amazfit Bip requires the  `Mili_chaohu.*` files. For **tested versions** and **known issues** check [below](#known-firmware-versions).

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

Original Firmware Version: 0.0.7.90 (Tested, pre-installed with watches manufactured July 2017)

fw ver    | MiFit ver | tested | known&nbsp;issues | res ver | gps ver | fw-md5 | res-md5 | gps-md5
----------|-----------|--------|-------------------|---------|---------|--------|---------|--------
0.0.8.20  | 3.0.2     | no     | ??           | 7 | 9367,8f79a91,0,0, | d737c210d960ac552dba9e3d88d96a3e | 2283a4d78058321c6eed60ea17dc83b1 | db27b914056153ff47f137fd0f91209e
0.0.8.32  | 3.0.4     | no     | ??           | 10 | 9367,8f79a91,0,0, | 2e20c581bad02f849b1c7ddf9d2beb94 | ddc3c7075de22e8a82229a5d4e660532 | db27b914056153ff47f137fd0f91209e
0.0.8.74  | 3.0.5     | yes    | deep sleep [\[1\]](#fwfootnote1) | 12 | 9367,8f79a91,0,0, | bc0eccb54246a999ceb0052ed0f542d8 | 88a6675421ae9a58b2d7b85a8782842d | db27b914056153ff47f137fd0f91209e
0.0.8.88  | 3.0.7     | yes    | slow UI, deep sleep [\[1\]](#fwfootnote1) | 13 | 9367,8f79a91,0,0, | 2d182f06402b7bb9afe591f2697d312f | 8c2953fb1d714b0fe64c4013dd033bfb | db27b914056153ff47f137fd0f91209e
0.0.8.96  | OTA only  | yes    | deep sleep [\[1\]](#fwfootnote1) | 16 | 9367,8f79a91,0,0, | 5458007fe89a3e4df2d166d49d2a4d9b | 2a745c9e97a561bff8472f2193086d52 | db27b914056153ff47f137fd0f91209e
0.0.8.97  | OTA only  | yes    | deep sleep [\[1\]](#fwfootnote1) | 16 | 9367,8f79a91,0,0, | e19cf338204b9190b88f5666399d66b5 | 2a745c9e97a561bff8472f2193086d52 | db27b914056153ff47f137fd0f91209e
0.0.8.98  | OTA only  | yes    | deep sleep [\[1\]](#fwfootnote1) | 16 | 9367,8f79a91,0,0, | c2c5737a304b476e197ea38354b81ea8 | 2a745c9e97a561bff8472f2193086d52 | db27b914056153ff47f137fd0f91209e

**WITH ENGLISH LANGUAGE FROM HERE ON**

 fw ver  | MiFit ver | tested | known&nbsp;issues | res ver | gps ver | fw-md5 | res-md5 | gps-md5
---------|-----------|--------|-------------------|---------|---------|--------|---------|--------
0.0.9.14 | 3.1.0     | yes    | deep sleep [\[1\]](#fwfootnote1) | 17 | 9367,8f79a91,0,0, | 92824f9e7cbb1a0729fbd27938ab2ba5 | e90b394bf0f9a055a108798656877ebe | db27b914056153ff47f137fd0f91209e
0.0.9.26 | 3.1.2     | yes    | deep sleep [\[1\]](#fwfootnote1), connection drops with some phones | 17 | 9565,dfbd8fa,0,0, | 78e59e39d237198af0c0e2aed5c82a1e | e90b394bf0f9a055a108798656877ebe | 97f9794cc46b2ebddaa0b52fe27a4f8f
0.0.9.40 | 3.1.3     | yes    | deep sleep [\[1\]](#fwfootnote1) | 19 | 9565,dfbd8fa,0,0, | fae9548f699ede59687b219a20e6e70d | 7099605b7e062645476f6b8bb815f6fb | 97f9794cc46b2ebddaa0b52fe27a4f8f
0.0.9.49[2] | 3.1.6.1   | yes    | deep sleep [\[1\]](#fwfootnote1) | 20 | 9565,dfbd8fa,0,0, | ba17b217a85d5e48e7061f36d9e9554e | 656c784e54c9ece7688eea64cb4d32d3 | 97f9794cc46b2ebddaa0b52fe27a4f8f
0.0.9.59[2] | 3.1.7.1   | yes    | deep sleep [\[1\]](#fwfootnote1) | 20 | 9565,dfbd8fa,0,0, | 617af082c8526b35452702798e6ce33c | 656c784e54c9ece7688eea64cb4d32d3 | 97f9794cc46b2ebddaa0b52fe27a4f8f
0.1.0.11[2] | 3.1.8.1   | yes    | deep sleep [\[1\]](#fwfootnote1) | 20 | 9565,dfbd8fa,0,0, | 
52e056e27a5b27891e257b71dae39e09 | 656c784e54c9ece7688eea64cb4d32d3 | 97f9794cc46b2ebddaa0b52fe27a4f8f
0.1.0.08 | 3.1.9   | no     | deep sleep [\[1\]](#fwfootnote1) | 20 | 9565,dfbd8fa,0,0, | 47ae3eb87462a946deddc315be00b406 | 656c784e54c9ece7688eea64cb4d32d3 | 97f9794cc46b2ebddaa0b52fe27a4f8f


<a name="fwfootnote1">[1]</a>: deep sleep detection does not work properly with Gadgetbridge, see https://github.com/Freeyourgadget/Gadgetbridge/issues/686#issuecomment-343773224

[2] Probable Beta Firmware (never appeared in a regular Mi-Fit release)