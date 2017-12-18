This page contains remarks about the different Mi Band firmware versions tested with Gadgetbridge. If you are using Gadgetbridge with a firmware version that is not listed here – or find that the information provided here are not correct – please provide your impressions and remarks to the team!

The firmwares are sorted by device. The recommended version comes first, then other versions sorted from newer to older.

Further information can be found here: https://github.com/flycodepl/mi-band-firmware-analyse

For information on actually updating the firmware see the [[Mi Band Firmware Update]] wiki page.

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
