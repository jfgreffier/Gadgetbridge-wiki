The Pebble watch ships with several system apps. Some of them are visible by default (Music), others can be activated from within Gadgetbridge's *Application Manager* (Health), and again others are hidden by default and require the "untested features" fo be enabled (Sport, Golf – see [Pebble specific settings](https://github.com/Freeyourgadget/Gadgetbridge/wiki/Configuration#pebble-specific-settings)).

### Music
![Music](https://i.imgur.com/SsWWSzP.png)  
<sup>*Music* on the *Pebble Time Steel*</sup>

Starting with v0.10.1, *Music* works well with most players – though only for "basic information": it displays the currently played track's interpret and title (see screenshot), which is updated whenever the track on your Android device changes. This is confirmed at least for the following apps:

* the stock (AOSP) music player
* Cyanogen's *Apollo*
* [DJD Player](https://github.com/mikaelstaldal/DJDPlayer)
* [GEM Player](https://github.com/SubstanceMobile/GEM)
* [Timber](https://f-droid.org/repository/browse/?fdid=naman14.timber)

But it somehow failed for [Jockey](https://github.com/marverenic/Jockey).

With the *Music* watchapp active, you also can control those players via the three buttons on the right of your Pebble: the upper button skips one title back, the lower forward. Pressing the middle button (labeled with three dots, as shown in the screenshot above) reveals a play/pause button, to fire the action press it again.

### Health

### Sport
*Sport* and *Golf* are some kind of barebone apps. It is possible for companion apps to

* start and stop them
* set the values you see on screen
* customize the name and icon
* react to the middle button when the app is started

Gadgetbridge does have support for all these except for changing the icon (for which of course you need to "Allow 3rd Party Android App Access" in Gadgetbridge [Pebble specific settings](https://github.com/Freeyourgadget/Gadgetbridge/wiki/Configuration#pebble-specific-settings). One app known to work with this is [RunnerUp](https://f-droid.org/repository/browse/?fdfilter=runnerup&fdid=org.runnerup).

### Golf