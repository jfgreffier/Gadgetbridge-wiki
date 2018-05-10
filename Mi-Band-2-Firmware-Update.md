## CAUTION
This feature **has the potential to brick your Mi Band 2**! That said, this has never happened to any of the developers, but remember **you're doing this at your own risk**.

## Getting the firmware
Since we may not distribute the firmware, you have to do a little work. You need to find and download a Mi Fit APK file. There is an APK Mirror Web site that might help you find Mi Fit. Extract the downloaded .apk file with "unzip", and you will find an `assets/` directory containing `*.fw` files, among others.

## Choosing the right firmware version for your Model

Device Name | HW Revisions | `*.fw` file
------------|--------------|------------
Mi Band 2   | V0.1.3.2 V0.1.3.3 V0.1.3.4 | Mili_pro.fw
Mi Band 2   | V0.9.3.3 V0.9.3.4 | Mili_pro_tph.fw
Mi Band 2   | V0.16.2.2    | Mili_pro_tph_as7000.fw
Mi Band 2   | ?            | Mili_pro_tph_indian.fw
Mi Band HRX | ?            | Mili_pro_i.fw

## Installing the firmware
Copy the desired Mi Band firmware as a `*.fw` file to your Android device and open it from any file manager on that device. The Gadgetbridge firmware update activity should then be started and guide you through the installation process.

**Important:** Mi Band 2 upgrades from 1.0.0.* firmware versions to newer versions (>1.0.1.* ) require to upgrade to an intermediate firmware version first. This intermediate version is 1.0.0.53 and is included in all Mi Fit APKs that supply such newer firmware. Besides the `Mili_pro.fw` file there will also be the file `Mili_pro_53.fw`. Install the latter *before* installing the `Mili_pro.fw` file.

**Note 1:** Both upgrade and downgrade of firmware versions is possible.

Starting with Firmware version 1.0.1.28 the Mi Band 2 supports text and special icon notifications. In order to get it working you need to have Gadgetbridge version >=0.18.0 and install the font files after installing the corresponding firmware file. These font files are located in the same directory as the firmware files and named `Mili_pro.ft*` (currently `Mili_pro.ft` and `Mili_pro.ft.en`). The installation process is the same as with the firmware file.

**Note 2:** Text and special icon support is still under development and has currently limited functionality.

**Note 3:** After flashing some firmware versions the first time coming from prior versions you have to remove the pairing in Android Bluetooth settings, then press the + button in Gadgetbridge to pair again. Do this if you have problems connecting after a firmware update, you wont lose any data. 

## Mi Band 2 (original version) firmwares

### 0.0.0 series

fw ver   | MiFit ver | tested | known&nbsp;issues | fw-md5 
---------|-----------|--------|-------------------|--------
0.0.0.58 | 2.0.0     | no | ? | 67e54bc888373b45a6867c7b49bb7d8c
0.0.0.63 | 2.0.5     | no | ? | f5dd9cb05b17a2031e3d0578416d4cd9
0.0.0.81 | 2.0.10    | no | ? | bb763022f82b4528b465e76eb61860ec


### 1.0.0 series

fw ver   | MiFit ver | tested | known&nbsp;issues | fw-md5 
---------|-----------|--------|-------------------|--------
1.0.0.2  | 2.1.0     | no  | ? | e92c1d40691322f0a4fa718a150a4c32
1.0.0.11 | 2.1.3     | no  | ? | e1a4a2650366d9ba1e428a822dee014f
1.0.0.18 | 2.1.5     | no  | ? | bed62211776a5623767d51861d8b71a1
1.0.0.23 | 2.1.6     | no  | ? | dd7c055415d41fcc567ea783b70f0319
1.0.0.39 | 2.1.9     | yes | ? | a98ee8d6a04b3bb4aff472e2cc91c21b
1.0.0.53 | 2.2.4     | yes | ? | abdd122897234f40b556f775ba0b9dc2


### 1.0.1 series

fw ver   | MiFit ver | tested | known&nbsp;issues | fw-md5 
---------|-----------|--------|-------------------|--------
1.0.1.21 | 2.2.8     | no  | ? | d3d9d3d1cf7d227acba9a0be2015f61b
1.0.1.28 | 2.2.9     | yes | ? | 804903543b7958c1b4f9b5c0e420bcb5
1.0.1.34 | 2.2.12    | yes | ? | 3ae6d0abe06006fbcf0d1685ad8231bb
1.0.1.39 | 2.3.0     | yes | ? | 470641716d9e63115b839cb38eaafce7
1.0.1.47 | 2.4.0     | no  | ? | 045edd2b2df5876f777a14eb3bc29966
1.0.1.50 | 2.4.2     | no  | ? | e7ecb89b71236452c1bf4a89521bc30a
1.0.1.53 | 3.0.5     | yes | ? | 42197ff93b9f4b0c6c9eee2b5b2308f5
1.0.1.54 | 3.1.0     | yes | ? | fa69dceb28458d99a905583ee2f8e2ef
1.0.1.59 | 3.1.5     | no  | ? | c3b771a7279fd6d8d361aecb7a91f051
1.0.1.67 | 3.1.9     | no  | ? | ddf32cd76409828bc15216b8f5eed3e2
1.0.1.69 | 3.2.1     | yes | ? | 8652a310283ed3fb52b4f44bc3d387e8
1.0.1.81 | 3.2.2.2   | no  | ? | d17a4d0bc4f1a3df3c903366396c230f
1.0.1.81 | 3.3.2     | yes | ? | d17a4d0bc4f1a3df3c903366396c230f

## Mi Band 2 (tph) firmwares

### 1.0.1 series

fw ver   | MiFit ver | tested | known&nbsp;issues | fw-md5 
---------|-----------|--------|-------------------|--------
1.0.1.30 | 2.2.12    | no | ? | 921b558eb0764280d070322b3e92c920
1.0.1.33 | 2.3.0     | no | ? | bd773efaa1c40096bea6509ead7610c1
1.0.1.47 | 2.4.0     | no | ? | 9ed679eacfbd978fd8a28d82fd31e688
1.0.1.50 | 3.0.0     | no | ? | 85b8b60b5e58d022c2d492178ed129cd
1.0.1.53 | 3.0.6     | yes | ? | 2aad5d32fa58b1d753139da6c88dc2d6
1.0.1.67 | 3.1.9     | no | ? | 9a42733b1b053182ed2d9758d14d96c0
1.0.1.69 | 3.2.1     | yes | ? | f290f8390bea7a1abd0af4018299b44c
1.0.1.81 | 3.2.2.2   | no  | ? | 932b980b70a90ecb97b29c7fbfe8438a

## Mi Band 2 (tph_as7000) firmwares

### 1.0.1 series

fw ver   | MiFit ver | tested | known&nbsp;issues | fw-md5 
---------|-----------|--------|-------------------|--------
1.0.1.52 | 3.0.5     | no | ? | 541d7fc6525a6cafa8c6ef224765f39e
1.0.1.67 | 3.1.9     | no | ? | 5f4e939a32dc3cf50f3564a827c60100
1.0.1.69 | 3.2.1     | yes | ? | 3199c3c3eaf14316ec7a9b35eb0baa74
1.0.1.81 | 3.2.2.2   | no  | ? | 70174d598811ed28de818358515418f3

## Mi Band 2 (tph_indian) firmwares

### 1.0.1 series

fw ver   | MiFit ver | tested | known&nbsp;issues | fw-md5 
---------|-----------|--------|-------------------|--------
1.0.1.58 | 3.0.0     | no | ? | f55cf0c4d28b07ddaae94aa65c5715e4
1.0.1.61 | 3.0.2     | no | ? | 19cfc77a37ae235052bfbc1be792e174
1.0.1.69 | 3.0.4     | no | ? | abd38ca3231aa2eb61ef574f7f2c60ff
1.0.1.70 | 3.2.2.3   | no | ? | e08b3632fa0ace7fbfad4fc43b425df6
1.0.1.81 | 3.2.2.2   | no  | ? | aeea9e3e8997922b1cea843838be7987

## Mi Band HRX firmwares

### 1.0.1 series

fw ver   | MiFit ver | tested | known&nbsp;issues | fw-md5 
---------|-----------|--------|-------------------|--------
1.0.1.49 | 3.0.0     | no | ? | 27af1c31d6dda4fa3a7d1eed30870a17
1.0.1.52 | 3.0.2     | no | ? | 5c7bb03511fffccac5b14ace21c492f5


### Original Mi Band 2 Firmware 1.0.x.x (old table)

| Version / Function | 1.0.1.54 | 1.0.1.53 | 1.0.1.50 | 1.0.1.47         | 1.0.1.39                          | 1.0.1.34                          | 1.0.1.28                          | 1.0.0.53                          | 1.0.0.39                          | 1.0.0.34 | 1.0.0.19                          |
| ----------------------- | -----------------------|------ |------ |------ | --------------------------------- | --------------------------------- | --------------------------------- | --------------------------------- | --------------------------------- | --------------------------------- | --------------------------------- |
| recommended                   | yes | yes| no | no |yes  | yes   | yes  | yes | yes                               | no      | no      |
| alarms                        | work | work | work | ? |work                              | work                              | work (no smart alarms)       | ? | work                              | work (smart alarms partly?)      | work (smart alarms partly?)      |
| notifications                 | work | work | work | ? |work                              | work                              | work                              | work | work                              | work                              | work                              |
| activity recognition          | no deep sleep[1] | no deep sleep[1] | no deep sleep[1] | no deep sleep[1] | works                             | works                             | works                             | ? | works                             | works                     | works                     |
| text and special icon notifications | partial | partial | partial | ? | partial | partial | partial |no |no | no | no
| heart rate measurement        | works | works | works | ? | works                             | works                          | works                             | works | works                             | stopped working at some point (known firmware issue, not GB-related) | ? |
| Gadgetbridge FW installer no. | 47364 | 32121 | 50471 | ? |3929                             | 51770 | 32450 | 49197 | 41899                             | ? | ? |
| CRC32                         | ? | 4c44ea29 | 26913267 | ? |80f6ccbe                          | 01d1ef2d | ? | ? | 68efecd7                          | ? | ? |
| Mi Fit APK version            | 3.1.0 | 3.0.5 | 3.0.4-2.4.2 | >2.4.0 |2.3.0                             | 2.2.12 | 2.2.9 | >2.2.0 | 2.2.0                             | ? | ? |

[1]: deep sleep detection does not work properly with Gadgetbridge, see https://github.com/Freeyourgadget/Gadgetbridge/issues/686#issuecomment-343773224
