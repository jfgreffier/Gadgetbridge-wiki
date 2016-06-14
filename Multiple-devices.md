### Multiple Android devices and one Gadget
It is possible to share one Gadget among multiple Android devices, but only one device can be connected at a time; furthermore the implication would be that chunks of your health data will be send to different android devices (so you won't have a complete set on any of them; [source](https://github.com/Freeyourgadget/Gadgetbridge/issues/322#issuecomment-223714965)).

This will change with the release v0.10.1 of Gadgetbridge: The activity trackers to sync can be set by checking the newly introduced checkboxes in Pebble settings. This is independent from the activity tracker to display on graphs (currently labeled "Preferred Activitytracker") but activity trackers that are not synced will save no data in Gadgetbridge DB, hence nothing will be shown on the graphs as well.

You make one device the "Master" checking all the checkboxes that are relevant to your usage, and the other the "Slave" ensuring the checkboxes are not selected. Be aware that by default these checkboxes **are** checked, because that's the most common use-case for Gadgetbridge.

### Multiple Gadgets and one Android device
This is currently not possible, as [Gadgetbridge only allows one device to be connected at a time](https://github.com/Freeyourgadget/Gadgetbridge/issues/305#issuecomment-219798461). It is [technically possible](https://github.com/Freeyourgadget/Gadgetbridge/issues/305#issuecomment-221086169), though, and thoughts are being made. But it's not yet on the roadmap for one of the next releases.


### Multiple Trackers
You can use multiple trackers simultaneously (e.g. Pebble Health and Morpheuz). By default, sync for all supported trackers is activated – which should be fine for most users (even if they don't have Morpheus or Misfit installed). The only context in which you must deactivate them is the [Multiple Android devices and one Gadget](#multiple-android-devices-and-one-gadget) case described above.

If you are satisfied with a third party tracker and want to switch off the integrated Pebble Health, you can do so from the app manager: long-press on the "Health" app and tap "Deactivate" (at the same place you can press "Activate" to enable it). For Morpheuz and Misfit, simply uninstall their watch apps if you no longer wish to use them.