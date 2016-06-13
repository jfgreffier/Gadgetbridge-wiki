This page is about apps running on your Pebble, also called „Watchfaces“.

### Contents
* [Where can I find Watchfaces?](#where-can-i-find-watchfaces)
* [How do I install them to my Pebble?](#how-do-i-install-them-to-my-pebble)
* [How do I manage installed watchfaces?](#how-do-i-manage-installed-watchfaces)
* [Why do some watchfaces not work fully?](#why-do-some-watchfaces-not-work-fully)

### Where can I find Watchfaces?
You can find them on many places. The official source for watchfaces is the corresponding section in the Pebble store: [Watchfaces](https://apps.getpebble.com/en_US/watchfaces?dev_settings=true). There you can browse through a large collection of watchfaces and, following the button on the end of each watchface page, download them via the „Download PBW“ button.

There are also several free and open-source watchfaces you can find here at Github. The Gadgetbridge team e.g. recommends:

* [Mario Time](https://github.com/ClusterM/pebble-mario)
* [Mini Dungeon](https://github.com/Torivon/MiniDungeon)

### How do I install them to my Pebble?
Once the `.pbw` files are on your Android device running Gadgetbridge (either because you've downloaded them there, or copied them over from your computer), simply tap the file in the file manager of your choice (or the „Downloads“ app). A popup will appear asking you what to open it with. Chose the Gadgetbridge „FW/App Installer“, and the watchface will be installed to your Pebble. If you download a watchface directly on the device running Gadgetbridge, your browser might even prompt you to:

[![FM install](http://i.imgur.com/7ulfoS8t.png)](http://i.imgur.com/7ulfoS8.png) [![BrowserInstall](https://i.imgur.com/vN00enQm.png)](https://i.imgur.com/vN00enQ.png)  
<sup>Install a watchface from within the file manager / install it directly from the browser</sup>

### How do I manage installed watchfaces?
Once you've installed a watchface, Gadgetbridge will cache it. So tapping your device in Gadgetbridge (when it's connected) brings you to the app manager. Long-tap (alias „tap-and-hold“) the entry of an app will bring up a context menu with available actions:

[![App Manager](https://i.imgur.com/WfE3oTIm.png)](https://i.imgur.com/WfE3oTI.png)  
<sup>Gadgetbridge App Manager with open context menu</sup>

As the screenshot shows, here you can reinstall an app (in case you've deleted it), delete it from the watch, or delete it from the watch and the Gadgetbridge cache.

Note: With Firmware 3.x Gadgetbridge has no means of determining which watchfaces are installed on your Pebble. Hence it can only tell what's in its cache, so please don't wonder.

Btw: a single tap on a watchface in Gadgetbridge will start it on your Pebble – saving your from button-juggling.


### Why do some watchfaces not work fully?
There are some restrictions to consider. Remember for example that Gadgetbridge comes without the Internet permission (for privacy reasons) – so watchfaces won't be able to access the internet through it. That means weather data can't be retrieved – and things like e.g. the [TripAdvisor](https://apps.getpebble.com/de_DE/application/5509b04684ad023da7000030?dev_settings=true&hardware=basalt&is_browser=true&platform=android&query=&section=watchapps) app cannot do anything useful.

That's by design – and before you ask: No, Gadgetbridge won't get the Internet permission added. For your own sake (and so you can trust us not to send your data somewhere into the cloud). There *might* be an [Internet-enabled companion app](https://github.com/Freeyourgadget/Gadgetbridge/issues/302) (or addon) one day, though. To work around that, you could use watchfaces that have another Android companion app which comes with the Internet permission. Unfortunately, there are [security implications](https://github.com/Freeyourgadget/Gadgetbridge/issues/302#issuecomment-219211974) with all of them: don't blame the devs for that, they're innocents. Put into simple terms: as the watchfaces are installed on your Pebble (and not on the Android device), Android cannot assing them specific permissions – and thus they need to use less secure means of communication. Details behind the link.