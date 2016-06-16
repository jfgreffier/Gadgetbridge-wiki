The Pebble watch ships with several system apps. Some of them are visible by default (Music), others can be activated from within Gadgetbridge's *Application Manager* (Health), and again others are hidden by default and require the "untested features" fo be enabled (Sport, Golf – see [Pebble specific settings](https://github.com/Freeyourgadget/Gadgetbridge/wiki/Configuration#pebble-specific-settings)).

### Music
[![Music](https://i.imgur.com/SsWWSzPs.png)](https://i.imgur.com/SsWWSzP.png)  
<sup>*Music* on the *Pebble Time Steel*</sup>

Starting with v0.10.1, *Music* works well with most players – though only for "basic information": it displays the currently played track's interpret and title (see screenshot), which is updated whenever the track on your Android device changes. This is confirmed at least for the following apps:

* the stock (AOSP) music player
* Cyanogen's *Apollo*
* [DJD Player](https://github.com/mikaelstaldal/DJDPlayer)
* [GEM Player](https://github.com/SubstanceMobile/GEM)
* [Timber](https://f-droid.org/repository/browse/?fdid=naman14.timber)

But it somehow failed for [Jockey](https://github.com/marverenic/Jockey).

With the *Music* watchapp active, you also can control those players via the three buttons on the right side of your Pebble: the upper button skips one title back, the lower forward. Pressing the middle button (labeled with three dots, as shown in the screenshot above) reveals a play/pause button, to fire the action press it again.

### Health
To activate the *Health* app, open the Application Manager in Gadgetbridge, long-press the "Health" entry, and select "Activate". The app then will collect healt data on your watch (steps and sleep data), and – provided you didn't deactivate it – Gadgetbridge will sync this data. If you selected "Pebble Health" as your preferred activity tracker, those data will be used on Gadgetbridge's "Your activity" screens:

[![Menu](https://i.imgur.com/jZfEhHmm.png)](https://i.imgur.com/jZfEhHm.png) [![Activity&Sleep](https://i.imgur.com/70YobbFm.png)](https://i.imgur.com/70YobbF.png) [![Sleep](https://i.imgur.com/OZ43x0Tm.png)](https://i.imgur.com/OZ43x0T.png) [![Steps](https://i.imgur.com/rlsTLYUm.png)](https://i.imgur.com/rlsTLYU.png)  
<sup>Context menu and activity screens; click images for larger variants)</sup>

With your Pebble connected, long-press its name and select "Your Activity" from the drop-down (first screenshot). You should then see a screen like in the second screenshot, summarizing your activity of the last 24 hours. From here you can swipe to the other screens (or tap their "tab" on the bottom of the screen). In case you wonder whether I have no heart (beats): the Pebble has no sensor for that, so it doesn't support it (screens are the same for MiBand, which does support heart rate). As you've probably already have discovered on the screenshots, you can browse through the days using the corresponding buttons in the upper part of the screen.

This is what it will look like on your Pebble:

[![Steps](https://i.imgur.com/DurBLw1m.png)](https://i.imgur.com/DurBLw1.png) [![Sleep](https://i.imgur.com/Vnev4Fem.png)](http://i.imgur.com/Vnev4Fe.png)  
<sup>Steps and Sleep on your Pebble watch (click images for larger variants)</sup>


### Sport
*Sport* and *Golf* are some kind of barebone apps. It is possible for companion apps to

* start and stop them
* set the values you see on screen
* customize the name and icon
* react to the middle button when the app is started

[![Sport](https://i.imgur.com/dYxzWKes.png)](https://i.imgur.com/dYxzWKe.png)  
<sup>The *Sport* watchapp</sup>

Gadgetbridge does have support for all these except for changing the icon (of course you need to "Allow 3rd Party Android App Access" in Gadgetbridge [Pebble specific settings](https://github.com/Freeyourgadget/Gadgetbridge/wiki/Configuration#pebble-specific-settings) first). One app known to work with this is [RunnerUp](https://f-droid.org/repository/browse/?fdfilter=runnerup&fdid=org.runnerup).

### Golf
[![Golf](https://i.imgur.com/T6XYIHds.png)](https://i.imgur.com/T6XYIHd.png)  
<sup>The *Golf* watchapp</sup>