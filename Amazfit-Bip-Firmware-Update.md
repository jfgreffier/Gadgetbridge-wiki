## CAUTION
This feature **has the potential to brick your Amazfit Bip**! That said, this has never happened to any of the developers, but remember **you're doing this at your own risk**.

## Getting the firmware
Since we may not distribute the firmware, you have to do a little work. You need to find and download a Mi Fit APK file. There is an APK Mirror Web site that might help you find Mi Fit. Extract the downloaded .apk file with "unzip", and you will find an `assets/` directory containing `*.fw` files, among others.

The Amazfit Bip requires the  `Mili_chaohu.*` files. For **tested versions** and **known issues** check [below](#known-firmware-versions).

## Installing the firmware
Copy the desired Amazfit Bip firmware and ressource files as a `*.gps`, `*.res` and `*.fw` file to your Android device and open it from any file manager on that device. The Gadgetbridge FW/App Installer activity should then be started and guide you through the installation process.

### Recommended flashing order:
1. Mili_chaohu.fw
2. Mili_chaohu.res (The Bip will tell you when needed)
3. Mili_chaohu.gps (This rarely changes, check the table below, if you should update)

Flashing the `*.fw` triggers a reboot and will show a screen which will ask you to flash the .res if your version is outdated.

**Note 1:** Both upgrade and downgrade of firmware versions is possible but untested, we do not encourage do do it.

**Note 2:** After flashing to a 0.0.9.x release the first time coming from prior versions you have to remove the pairing in Android Bluetooth settings, then press the + button in Gadgetbridge to pair again.

**Note 3:** Starting with Firmware version 0.0.9.14 the Amazfit Bip supports English menus. If the desired language is not shown  automatically, you can select it in at Settings->Amazfit Bip Settings->Language after installing the corresponding firmware file.

**Note 4:** Recent firmwares come in two version ("Normal" and Latin), While "Normal" seems to support English and Chinese (Spanish support introduced and later dropped), the Latin version seems to support Spanish and Russian. If you flash the Latin version you also need to flash the Latin font (which does not contain CJK Characters).

## Known firmware Versions

Original Firmware Versions: 

- 0.0.7.90 (Tested, pre-installed with Chinese watches manufactured July 2017)
- 0.0.8.95 (pre-installed with the "English Version" manufactured December 2017)

**0.0.8 series**

fw ver    | MiFit ver | tested | known&nbsp;issues | res ver | gps ver | fw-md5 | res-md5 | gps-md5
----------|-----------|--------|-------------------|---------|---------|--------|---------|--------
0.0.8.10  | 3.0.0     | no     | ??           | 7 | 9367,8f79a91,0,0, | d5e10b1b25f9a2a4cabba0ca8ff64b87 | 2283a4d78058321c6eed60ea17dc83b1 | db27b914056153ff47f137fd0f91209e
0.0.8.20  | 3.0.2     | no     | ??           | 7 | 9367,8f79a91,0,0, | d737c210d960ac552dba9e3d88d96a3e | 2283a4d78058321c6eed60ea17dc83b1 | db27b914056153ff47f137fd0f91209e
0.0.8.32  | 3.0.4     | no     | ??           | 10 | 9367,8f79a91,0,0, | 2e20c581bad02f849b1c7ddf9d2beb94 | ddc3c7075de22e8a82229a5d4e660532 | db27b914056153ff47f137fd0f91209e
0.0.8.74  | 3.0.5     | yes    | deep sleep [\[1\]](#fwfootnote1) | 12 | 9367,8f79a91,0,0, | bc0eccb54246a999ceb0052ed0f542d8 | 88a6675421ae9a58b2d7b85a8782842d | db27b914056153ff47f137fd0f91209e
0.0.8.88  | 3.0.7     | yes    | slow UI, deep sleep [\[1\]](#fwfootnote1) | 13 | 9367,8f79a91,0,0, | 2d182f06402b7bb9afe591f2697d312f | 8c2953fb1d714b0fe64c4013dd033bfb | db27b914056153ff47f137fd0f91209e
0.0.8.96  | OTA only  | yes    | deep sleep [\[1\]](#fwfootnote1) | 16 | 9367,8f79a91,0,0, | 5458007fe89a3e4df2d166d49d2a4d9b | 2a745c9e97a561bff8472f2193086d52 | db27b914056153ff47f137fd0f91209e
0.0.8.97  | OTA only  | yes    | deep sleep [\[1\]](#fwfootnote1) | 16 | 9367,8f79a91,0,0, | e19cf338204b9190b88f5666399d66b5 | 2a745c9e97a561bff8472f2193086d52 | db27b914056153ff47f137fd0f91209e
0.0.8.98  | OTA only  | yes    | deep sleep [\[1\]](#fwfootnote1) | 16 | 9367,8f79a91,0,0, | c2c5737a304b476e197ea38354b81ea8 | 2a745c9e97a561bff8472f2193086d52 | db27b914056153ff47f137fd0f91209e

**0.0.9 series (introduces English language)**

 fw ver  | MiFit ver | tested | known&nbsp;issues | res ver | gps ver | fw-md5 | res-md5 | gps-md5
---------|-----------|--------|-------------------|---------|---------|--------|---------|--------
0.0.9.14 | 3.1.0     | yes    | deep sleep [\[1\]](#fwfootnote1) | 17 | 9367,8f79a91,0,0, | 92824f9e7cbb1a0729fbd27938ab2ba5 | e90b394bf0f9a055a108798656877ebe | db27b914056153ff47f137fd0f91209e
0.0.9.26 | 3.1.2     | yes    | deep sleep [\[1\]](#fwfootnote1), connection drops with some phones | 17 | 9565,dfbd8fa,0,0, | 78e59e39d237198af0c0e2aed5c82a1e | e90b394bf0f9a055a108798656877ebe | 97f9794cc46b2ebddaa0b52fe27a4f8f
0.0.9.40 | 3.1.3     | yes    | deep sleep [\[1\]](#fwfootnote1) | 19 | 9565,dfbd8fa,0,0, | fae9548f699ede59687b219a20e6e70d | 7099605b7e062645476f6b8bb815f6fb | 97f9794cc46b2ebddaa0b52fe27a4f8f
0.0.9.49[2] | 3.1.6.1   | yes    | deep sleep [\[1\]](#fwfootnote1) | 20 | 9565,dfbd8fa,0,0, | ba17b217a85d5e48e7061f36d9e9554e | 656c784e54c9ece7688eea64cb4d32d3 | 97f9794cc46b2ebddaa0b52fe27a4f8f
0.0.9.59[2] | 3.1.7.1   | yes    | deep sleep [\[1\]](#fwfootnote1) | 20 | 9565,dfbd8fa,0,0, | 617af082c8526b35452702798e6ce33c | 656c784e54c9ece7688eea64cb4d32d3 | 97f9794cc46b2ebddaa0b52fe27a4f8f

**0.1.0 series**

 fw ver  | MiFit ver | tested | known&nbsp;issues | res ver | gps ver | fw-md5 | res-md5 | gps-md5
---------|-----------|--------|-------------------|---------|---------|--------|---------|--------
0.1.0.08 | 3.1.9     | yes     | deep sleep [\[1\]](#fwfootnote1) | 20 | 9565,dfbd8fa,0,0, | 47ae3eb87462a946deddc315be00b406 | 656c784e54c9ece7688eea64cb4d32d3 | 97f9794cc46b2ebddaa0b52fe27a4f8f
0.1.0.11[2] | 3.1.8.1   | yes    | deep sleep [\[1\]](#fwfootnote1) | 20 | 9565,dfbd8fa,0,0, | 52e056e27a5b27891e257b71dae39e09 | 656c784e54c9ece7688eea64cb4d32d3 | 97f9794cc46b2ebddaa0b52fe27a4f8f
0.1.0.17[2] | 3.2.0.1   | yes     | deep sleep [\[1\]](#fwfootnote1) | 21 | 9565,dfbd8fa,0,0, | 15c899aff4842eaea3608b512e86b2c6 | fcda343cdffbe12acec6bb8e9e9d20ca | 97f9794cc46b2ebddaa0b52fe27a4f8f
0.1.0.26    | 3.2.1     | yes    | deep sleep [\[1\]](#fwfootnote1) | 22 | 9565,dfbd8fa,0,0, | a64b9ce5d58612d13da08b507db79a01 | c9e82528cb97db2e5bb85781d6f38c54 | 97f9794cc46b2ebddaa0b52fe27a4f8f
0.1.0.27[2] | 3.2.2.1   | yes    | deep sleep [\[1\]](#fwfootnote1) | 22 | 9565,dfbd8fa,0,0, | f76b8c0e536c609ee7e04400f3f866ed | c9e82528cb97db2e5bb85781d6f38c54 | 97f9794cc46b2ebddaa0b52fe27a4f8f
0.1.0.33[2] | 3.2.2.2   | yes    | deep sleep [\[1\]](#fwfootnote1) | 23 | 9565,dfbd8faf42,0 | 3109ebb17d7bfee045e1996d79030aad | 136a07f0f1740d3a9cd3688e50500d44 | b4f787b3e722e69252df90e4c710b85d
0.1.0.39[2] | 3.2.2.3   | yes    | deep sleep [\[1\]](#fwfootnote1) | 24 | 9565,dfbd8faf42,0 | c37c04794ffc893c872cc116a402aaf4 | 25e306b149e5a0f574b81521a7ad6951 | b4f787b3e722e69252df90e4c710b85d
0.1.0.43[2] | 3.2.3.1   | yes    | deep sleep [\[1\]](#fwfootnote1) | 24 | 9565,dfbd8faf42,0 | 19d3adcf6583a76f4d10a32a8276b022 | 25e306b149e5a0f574b81521a7ad6951 | b4f787b3e722e69252df90e4c710b85d
0.1.0.44    | 3.2.5     | yes     | deep sleep [\[1\]](#fwfootnote1) | 24 | 9565,dfbd8fa,0,0, | c2deae493b880e50feae1c4a8953f665 | 25e306b149e5a0f574b81521a7ad6951 | 97f9794cc46b2ebddaa0b52fe27a4f8f
0.1.0.45[2] | 3.2.5.1   | yes    | deep sleep [\[1\]](#fwfootnote1) | 24 | 9567,8b05506,0,0, | 9c1e36695cae0d8711a2aa9f4990aea9 | 25e306b149e5a0f574b81521a7ad6951 | c426b761147dd871e22fb887a8de630f
0.1.0.51[2] | 3.2.7.1   | no     | deep sleep [\[1\]](#fwfootnote1) | 25 | 9567,8b05506,0,0, | 26116b3b2ebb4b83badf92fa5814ff35 | 48a0d11de49f52b12cc2c8a7a72f6218 | c426b761147dd871e22fb887a8de630f
0.1.0.66[2] | 3.2.7.2   | no     | deep sleep [\[1\]](#fwfootnote1), slow UI | 26 | 9567,8b05506,0,0, | e00e197f9f9c83ea15e1083eaf6e8814 | e77e6ec609a6fedf5f8954a2f00011de | c426b761147dd871e22fb887a8de630f
0.1.0.70    | 3.2.7     | yes     | deep sleep [\[1\]](#fwfootnote1) | 26 | 9567,8b05506,0,0, | 7fbbfba40b8c26fa086704843747edee | e77e6ec609a6fedf5f8954a2f00011de | c426b761147dd871e22fb887a8de630f
0.1.0.77[2] | 3.2.8.1   | no     | deep sleep [\[1\]](#fwfootnote1) | 27 | 9567,8b05506,0,0, | 585b8ff7eddade8d403816239b5b5ad5 | 57733612f256814ab190c6ea244d2035 | c426b761147dd871e22fb887a8de630f
0.1.0.80    | 3.2.8     | yes    | deep sleep [\[1\]](#fwfootnote1) | 27 | 9567,8b05506,0,0, | 769391c599e1091b0b07dbb23ee33a92 | 57733612f256814ab190c6ea244d2035 | c426b761147dd871e22fb887a8de630f
0.1.0.86    | 3.2.9     | yes    | deep sleep [\[1\]](#fwfootnote1) | 28 | 9567,8b05506,0,0, | 787d8bb255bd7515a75bd194bbdf432c | f759680274f023d057d8f529b27fb0f7 | c426b761147dd871e22fb887a8de630f
0.1.0.87[2] | 3.3.0.1   | no     | deep sleep [\[1\]](#fwfootnote1) | 28 | 9567,8b05506,0,0, | 73a121307977235f4cb3f4a21e866421 | f759680274f023d057d8f529b27fb0f7 | c426b761147dd871e22fb887a8de630f
0.1.0.89[2] | 3.3.0.2   | no     | deep sleep [\[1\]](#fwfootnote1) | 28 | 9567,8b05506,0,0, | 503fe62959df4ccc1755e7b5147d59c7 | f759680274f023d057d8f529b27fb0f7 | c426b761147dd871e22fb887a8de630f
0.1.0.99[2] | 3.3.2.1   | no     | deep sleep [\[1\]](#fwfootnote1) | 29 | 9567,8b05506,0,0, | d00c5dbe4c1cff2de0904e9f66fd752b | bfe0e5550f3e6628c2ea11e3c08978d5 | c426b761147dd871e22fb887a8de630f


**0.1.1 series**

 fw ver  | MiFit ver | tested | known&nbsp;issues | res ver | gps ver | fw-md5 | res-md5 | gps-md5
---------|-----------|--------|-------------------|---------|---------|--------|---------|--------
0.1.1.05[2] | 3.3.2.2   | no     | deep sleep [\[1\]](#fwfootnote1) | 30 | 9567,8b05506,0,0, | 7e4e4163f6bcb965f336f9f81d644b44 | 4648ed16f3f06ba4af189f5d2f9a2e15 | c426b761147dd871e22fb887a8de630f
0.1.1.14    | 3.3.1     | yes    | deep sleep [\[1\]](#fwfootnote1) | 31 | 9567,8b05506,0,0, | 0b45fc881e5396614488226b995d4ee6 | 16542e0167d0cb6a2e0be94736af7383 | c426b761147dd871e22fb887a8de630f
0.1.1.15[2] | 3.3.4.1   | no     | deep sleep [\[1\]](#fwfootnote1) | 32 | 9567,8b05506,0,0, | ce77cade5a9b4a61bc0dfdbfba74ebc1 | e8d954081b4448ce0621caa35ba59c54 | c426b761147dd871e22fb887a8de630f
0.1.1.17[2] | 3.3.4.6   | yes    | deep sleep [\[1\]](#fwfootnote1) | 32 | 9567,8b05506,0,0, | 330b77a0cf4f0dd1500581fc57543ac7 | e8d954081b4448ce0621caa35ba59c54 | c426b761147dd871e22fb887a8de630f
0.1.1.25[2] | 3.3.4.9   | no     | deep sleep [\[1\]](#fwfootnote1) | 32 | 9567,8b05506,0,0, | fca925d9979336d91bf2defebae5061e | e8d954081b4448ce0621caa35ba59c54 | c426b761147dd871e22fb887a8de630f
0.1.1.29[2] | 3.3.4.10  | yes    | deep sleep [\[1\]](#fwfootnote1) | 33 | 9567,8b05506,0,0, | 591645d7043b7ed8fd195595a350baad | e7521511a24bf7ee87f4262dfe04d9c8 | c426b761147dd871e22fb887a8de630f
0.1.1.31[2] | 3.3.4.11  | yes    | deep sleep [\[1\]](#fwfootnote1) | 34 | 9567,8b05506,0,0, | bb5b6add4950b848201575f71c73aa42 | 5c78d121088725c9be6a3f58333cd464 | c426b761147dd871e22fb887a8de630f
0.1.1.36    | 3.3.2     | yes    | deep sleep [\[1\]](#fwfootnote1) | 34 | 9567,8b05506,0,0, | 958afb6ed1d21e028554b525d294667c | 5c78d121088725c9be6a3f58333cd464 | c426b761147dd871e22fb887a8de630f
0.1.1.39[2] | 3.3.4.13  | yes    | deep sleep [\[1\]](#fwfootnote1) | 36 | 9567,8b05506,0,0, | a6b1425f0ac0a0777bc474a66256e548 | 920d9e961e7f770bdd57dc9aeeba7f5f | c426b761147dd871e22fb887a8de630f
0.1.1.41[2] | 3.4.0.1   | yes    | deep sleep [\[1\]](#fwfootnote1) | 37 | 9567,8b05506,0,0, | be8d0cee6ccdc89b00c6696229be2083 | 2a092f2bd12410c587dd6a4b26e7a396 | c426b761147dd871e22fb887a8de630f
0.1.1.45[2] | 3.4.0.2   | yes    | deep sleep [\[1\]](#fwfootnote1) | 38 | 9567,8b05506,0,0, | 8db0857956bff4446277418ca5a54db8 | b93943ea00af4f1d4d17434a4b3a9c67 | c426b761147dd871e22fb887a8de630f

**1.0.x series**

 fw ver  | MiFit ver | tested | known&nbsp;issues | res ver | gps ver | fw-md5 | res-md5 | gps-md5
---------|-----------|--------|-------------------|---------|---------|--------|---------|--------
1.0.1.00 | 3.4.2     | yes     | deep sleep [\[1\]](#fwfootnote1) | 39 | 9567,8b05506,0,0, | 2e4d0a04b7c6a58bcebdb6643a164a5c | de29d2348bef88ce81fa307b2b5adddb | c426b761147dd871e22fb887a8de630f
1.0.2.00[2] | 3.4.4.1   | yes    | deep sleep [\[1\]](#fwfootnote1) | 40 | 9567,8b05506,0,0, | 37ed4544d7b67ae9af2359d6f4583ae0 | 1bd4015d3e4beccd6f20e67404e0799d | c426b761147dd871e22fb887a8de630f
1.1.1.00[2] | 3.4.4.2   | yes    | deep sleep [\[1\]](#fwfootnote1), slowed a bit | 40 | 9567,8b05506,0,0, | 020d5b055cc32aa1f374641b10388661 | 1bd4015d3e4beccd6f20e67404e0799d | c426b761147dd871e22fb887a8de630f
1.1.2.05    | 3.4.4     | yes    | deep sleep [\[1\]](#fwfootnote1) | 41 | 9567,8b05506,0,0, | 21edab6ad18108817409107bc5425e36 | c49e723e02f8ba27682641bc473b3519 | c426b761147dd871e22fb887a8de630f
1.1.2.05    | 3.4.6     | yes    | deep sleep [\[1\]](#fwfootnote1) | 41 | 9567,8b05506,0,0, | 21edab6ad18108817409107bc5425e36 | c49e723e02f8ba27682641bc473b3519 | c426b761147dd871e22fb887a8de630f

<a name="fwfootnote1">[1]</a>: deep sleep detection does not work properly with Gadgetbridge, see https://github.com/Freeyourgadget/Gadgetbridge/issues/686#issuecomment-343773224

[2] Beta Firmware (never appeared in a regular Mi Fit release)