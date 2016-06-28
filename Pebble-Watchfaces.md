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

[![App Manager](https://i.imgur.com/3473hE9m.png)](https://i.imgur.com/3473hE9.png) [![WatchApps](https://i.imgur.com/gvsRaKlm.png)](https://i.imgur.com/gvsRaKl.png) [![WatchFaces](https://i.imgur.com/nHsGLcsm.png)](https://i.imgur.com/nHsGLcs.png)  
<sup>Gadgetbridge App Manager with open context menu</sup>

The App-Manager is divided in three tabs. Left to right from the screenshots: _Apps in cache_ (i.e. apps you've installed via Gadgetbridge, but which you also might have uninstalled meanwhile; Gadgetbridge keeps them in its cache until you explicitly remove them from there), _Installed apps_ Gadgetbridge knows about (i.e. system apps and those you've installed yourself via Gadgetbridge), and Installed _watchfaces_ (again those shipped with your watch and those you've installed yourself via Gadgetbridge). With FW 3.x Gadgetbridge cannot know anything about apps or watchfaces you've installed by other means (e.g. using the official Pebble app, or using another Android device), as this firmware offers no way to query that information: the official Pebble app manages that via the cloud.

Except for in the first tab, you also can rearrange the order apps and watchfaces appear in – in the App Manager as well as on your Pebble: tap and hold an entry, move it around, and drop it where you want it to be shown. Long pressing and releasing the Health app you can activate or deactivate Pebble Health data collection on your Pebble (e.g. when switching between different trackers like Morpheuz and Pebble Health).

As the first screenshot shows, you can also reinstall an app (in case you've deleted it), delete it from the watch, or delete it from the watch and the Gadgetbridge cache. If the app has a configuration page, you can call that from here as well: it will most likely open in a browser window, from where you submit your configuration values directly back to the corresponding watch app. Some watch apps however use a protocol the browser doesn't understand:

[![Protocol Error](https://i.imgur.com/V8tZVlMm.png)](https://i.imgur.com/V8tZVlM.png) [![Paste URL](https://i.imgur.com/pF1zM5hm.png)](https://i.imgur.com/pF1zM5h.png) [![New config](https://i.imgur.com/0fDYRsAm.png)](https://i.imgur.com/0fDYRsA.png)  
<sup>Configure a watch app using an "unknown protocol"</sup>

As the screenshots show, your browser will then display an error page. Long-press the URL shown and select to copy it to the clipboard, then close the browser (first screenshot). Back in Gadgetbridge, paste that URL into the field shown, and hit the button to parse the URL (second screenshot). After that, you have the choice to directly send the parsed data to the watch app to configure it, or to save it as a "preset". The latter saves you from running the entire procedure again: if you want to use the configuration you've saved as preset, you can just select that directly when calling the "Configure" item next time.

**Note:** With Firmware 3.x Gadgetbridge has no means of determining which watchfaces are installed on your Pebble. Hence it can only tell what's in its cache (i.e. the apps you've installed via Gadgetbridge), so please don't wonder.

Btw: a single tap on a watchface in Gadgetbridge will start it on your Pebble – saving your from button-juggling.


### Why do some watchfaces not work fully?
There are some restrictions to consider. Remember for example that Gadgetbridge comes without the Internet permission (for privacy reasons) – so watchfaces won't be able to access the internet through it. That means weather data can't be retrieved – and things like e.g. the [TripAdvisor](https://apps.getpebble.com/de_DE/application/5509b04684ad023da7000030?dev_settings=true&hardware=basalt&is_browser=true&platform=android&query=&section=watchapps) app cannot do anything useful.

That's by design – and before you ask: No, Gadgetbridge won't get the Internet permission added. For your own sake (and so you can trust us not to send your data somewhere into the cloud). There *might* be an [Internet-enabled companion app](https://github.com/Freeyourgadget/Gadgetbridge/issues/302) (or addon) one day, though. To work around that, you could use watchfaces that have another Android companion app which comes with the Internet permission. Unfortunately, there are [security implications](https://github.com/Freeyourgadget/Gadgetbridge/issues/302#issuecomment-219211974) with all of them: don't blame the devs for that, they're innocents. Put into simple terms: as the watchfaces are installed on your Pebble (and not on the Android device), Android cannot assing them specific permissions – and thus they need to use less secure means of communication. Details behind the link.