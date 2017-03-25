This page contains remarks about the different Mi Band firmware versions tested with Gadgetbridge. If you are using Gadgetbridge with a firmware version that is not listed here – or find that the information provided here are not correct – please provide your impressions and remarks to the team!

The firmwares are sorted by device. The recommended version comes first, then other versions sorted from newer to older.

Further information can be found on the [[Mi Band Firmware Update]] wiki page and here: https://github.com/flycodepl/mi-band-firmware-analyse

<!--
Template for each firmware:
## 1.0.
| Function | Behavior |
| --- | --- |
| alarms  | |
| notifications | |
| activity recognition |  |
| connection |  |
| battery life |  |
| gadgetbridge fw installer no. |  |

-->
# Mi Band 2 (Firmware 1.x)
**Note:** For text and special icon notifications you need to have firmware version >=1.0.1.28 and the corresponding font files (`Mili_pro.ft` and `Mili_pro.ft.en`) installed.

| Version / Function            | 1.0.1.39                          | 1.0.1.34                          | 1.0.1.28                          | 1.0.0.53                          | 1.0.0.39                          | 1.0.0.34 | 1.0.0.19                          |
| ----------------------------- | --------------------------------- | --------------------------------- | --------------------------------- | --------------------------------- | --------------------------------- | --------------------------------- | --------------------------------- |
| recommended                   | yes (when upgrading from 1.0.0.* versions, install version 1.0.0.53 (`Mili_pro_53.fw`) first)       | yes (when upgrading from 1.0.0.* versions, install version 1.0.0.53 (`Mili_pro_53.fw`) first)                               | yes (when upgrading from 1.0.0.* versions, install version 1.0.0.53 (`Mili_pro_53.fw`) first) | intermediate version needed to install newer firmware | yes                               | no      | no      |
| alarms                        | work                              | work                              | work (no smart alarms)       | ? | work                              | work (smart alarms partly?)      | work (smart alarms partly?)      |
| notifications                 | work                              | work                              | work                              | work | work                              | work                              | work                              |
| activity recognition          | works                             | works                             | works                             | ? | works                             | works                     | works                     |
| connection                    | works                             | works                          | works                             | works                             | works                             | works                             | works                             |
| battery life                  | good                              | good                           | good                              | ? | good                              | good                              | ? |
| heart rate measurement        | works                             | works                          | works                             | works | works                             | stopped working at some point (known firmware issue, not GB-related) | ? |
| gadgetbridge fw installer no. | 3929                             | 51770 | 32450 | 49197 | 41899                             | ? | ? |
| CRC32                         | 80f6ccbe                          | 01d1ef2d | ? | ? | 68efecd7                          | ? | ? |
| MD5SUM                        | 470641716d9e63115b839cb38eaafce7  | 3ae6d0abe06006fbcf0d1685ad8231bb | 804903543b7958c1b4f9b5c0e420bcb5 | abdd122897234f40b556f775ba0b9dc2 | a98ee8d6a04b3bb4aff472e2cc91c21b  | ? | ? |
| Mi Fit apk version            | 2.3.0                             | 2.2.12 | 2.2.9 | included in all newer apks as `Mili_pro_53.fw` | 2.2.0                             | ? | ? |

# Mi Band 1S (Firmware 4.x)
| Version / Function            | 4.15.12.10 Mi Band + 1.3.74.64 HR | 4.16.4.22 Mi Band + 1.3.76.22 HR  | 4.16.3.7 Mi Band + 1.3.76.18 HR  | 4.15.11.19 Mi Band  + ? HR                 |
| ----------------------------- | --------------------------------- | --------------------------------- | -------------------------------- | ------------------------------------------ |
| recommended                   | yes                               | yes                               | no                               | no                                         |
| alarms                        | work                              | work                              | work                             | does not work                              |
| notifications                 | work                              | work                              | work                             | work                                       |
| activity recognition          | works                             | works                             | works                            | unusable, detects far too many sleep hours |
| connection                    | works                             | works                             | works                            | works                                      |
| battery life                  | good                              | good                              | good                             | good                                       |
| heart rate measurement        | works                             | works                             | works                            | does not work                              |
| gadgetbridge fw installer no. | 68094986                          | 68158486                          | 68158215                         | ?                                          |
| CRC32                         | 393A9FC2                          | 5E1A74E2                          | A3F47C39                         | ?                                          |
| MD5SUM                        | 24d8b84f8964489b893d1cb4581dc85f  | 3b3b1427078b23808dce480a85665423  | 7883298d9696c608210991c1dc3d0030 | ?                                          |
| Mi band apk vesion            | 2.0.1, 2.0.4, 2.0.5               | 2.1.0, 2.1.1, 2.1.4, 2.1.5, 2.1.6 | 2.0.10                           | ?                                          |

# Mi Band 1A (with white LEDs, no heartrate sensor)
## 5.15.7.14 (recommended) (MiFit 1.5.912-1539)
| Function | Behavior |
| --- | --- |
| alarms | work |
| notifications | work |
| activity recognition | works |
| connection | works |
| battery life | good |
| gadgetbridge fw installer no. | 84870926 |

## From 5.15.7.29 upwards, notifications do not work well, or at all

## 5.15.11.19
| Function | Behavior |
| --- | --- |
| alarms | mostly works (randomly fails) |
| notifications | mostly works (randomly fails) |
| activity recognition | works |
| connection | works |
| battery life | good |
| sleep detection | doesn't work (band recognises sleep but not wake-up) |
| activity goal check | doesn't work |
| gadgetbridge fw installer no. | ? |

## 5.15.7.2
| Function | Behavior |
| --- | --- |
| alarms | do not work |
| activity recognition | ? |
| connection | ? |
| battery life | ? |
| gadgetbridge fw installer no. | ? |

# Mi Band 1 (coloured LEDs)

## 1.0.10.14
| Function | Behavior |
| --- | --- |
| activity recognition | no remarks |
| connection | Connecting and synchronizing seems to be slightly faster and more reliable than with previous firmware versions. However, for notifications the vibration feature does not work with Gadgetbridge versions prior to 0.6.2. |
| battery life | no remarks |
| gadgetbridge fw installer no. | 16779790 |

## 1.0.10.11
| Function | Behavior |
| --- | --- |
| activity recognition | seems to be working well, the "band not worn" detection looks good |
| connection | no remarks |
| battery life | no remarks |
| gadgedbridge fw installer no. | 16779787 |

## 1.0.10.6
| Function | Behavior |
| --- | --- |
| activity recognition | no remarks |
| connection | no remarks |
| battery life | no remarks |
| gadgedbridge fw installer no. | 16779782 |

## 1.0.10.3
| Function | Behavior |
| --- | --- |
| activity recognition | no remarks |
| connection | no remarks |
| battery life | no remarks |
| gadgedbridge fw installer no. | 16779779 |

## 1.0.9.48
| Function | Behavior |
| --- | --- |
| activity recognition | seems to be working well, there are many false positives regarding the band not worn state: in some cases the band is recognized as not worn even if it is. |
| connection | bluetooth range seems better compared to other version |
| battery life | no remarks |

## 1.0.9.27
| Function | Behavior |
| --- | --- |
| activity recognition | the sleep detection seems a bit off: a low activity level after 21:00 is often reported as light sleep |
| connection | the bluetooth connection seems to be problematic after some time |
| battery life | no remarks |

## 1.0.9.14
| Function | Behavior |
| --- | --- |
| activity recognition | no remarks |
| connection | the bluetooth connection seems to be problematic after some time |
| battery life | no remarks |

## 1.0.9.3
| Function | Behavior |
| --- | --- |
| activity recognition | works well, but it doesn't seem to recognize any sleep outside of "night hours". |
| connection | no remarks |
| battery life | no remarks |
