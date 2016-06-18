### Multiple Android devices and one Gadget
It is possible to share one Gadget among multiple Android devices, but only one device can be connected at a time; furthermore by default Gadgetbridge acknowledges the activity data sent by the device (i.e. the device will remove this data from its internal memory) and you won't have a complete set on any Android device.
You also need a Gadget that supports pairing to multiple devices, so far Miband does **not** support this scenario while Pebble watches do.

#### Pebble
In the pebble settings, starting with release 0.10.1, the activity trackers to sync can be set by checking the related checkboxes in Pebble settings. This is independent from the activity tracker to display on graphs (currently labeled "Preferred Activitytracker") but activity trackers that are not synced will save no data in Gadgetbridge DB, hence nothing will be shown on the graphs either.

The default GB configuration is for a single, "Master" device having all the checkboxes checked. If you want to use another device preserving your activity data, configure this "Slave" Android device ensuring the checkboxes that are relevant to you are not selected. Be aware that by default these checkboxes **are** checked, because that's the most common use-case for Gadgetbridge.

##### Multiple Trackers
You can use multiple trackers simultaneously (e.g. Pebble Health and Morpheuz). By default, sync for all supported trackers is activated – which should be fine for most users (even if they don't have Morpheus or Misfit installed). The only context in which you must deactivate them is the [Multiple Android devices and one Gadget](#multiple-android-devices-and-one-gadget) case described above.

If you are satisfied with a third party tracker and want to switch off the integrated Pebble Health, you can do so from the app manager: long-press on the "Health" app and tap "Deactivate" (at the same place you can press "Activate" to enable it). For Morpheuz and Misfit, simply uninstall their watch apps if you no longer wish to use them.

Note that at least [Pebble discourages using multiple tracking apps simultaneously](https://help.getpebble.com/customer/en/portal/articles/2239065-pebble-health?b_id=8308) (quote: *Pebble Health is very efficient and should use less battery than other third party fitness trackers. Please note, running two activity trackers will increase battery drain, and is not recommended.*) So better decide for one.

### Multiple Gadgets and one Android device
This is currently not possible, as [Gadgetbridge only allows one device to be connected at a time](https://github.com/Freeyourgadget/Gadgetbridge/issues/305#issuecomment-219798461). It is [technically possible](https://github.com/Freeyourgadget/Gadgetbridge/issues/305#issuecomment-221086169), though, and thoughts are being made. But it's not yet on the roadmap for one of the next releases.

