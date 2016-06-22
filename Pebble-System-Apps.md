The Pebble watch ships with several system apps. Some of them are visible in Gadgetbridge's *Application Manager* by default (Music), some need to be activated from within Gadgetbridge's *Application Manager* to do their work on your Pebble (Health), and others are hidden by default in the *Application Manager* unless "untested features" are enabled (Sport, Golf – see [Pebble specific settings](https://github.com/Freeyourgadget/Gadgetbridge/wiki/Configuration#pebble-specific-settings); they'll work on your Pebble though when a matching third-party companion app triggers them).

### Music
[![Music](https://i.imgur.com/SsWWSzPs.png)](https://i.imgur.com/SsWWSzP.png) [![Volume Control](https://i.imgur.com/FR8Uk9ss.png)](https://i.imgur.com/FR8Uk9s.png)  
<sup>*Music* on the *Pebble Time Steel*</sup>

*Music* works well with most players – though often only for "basic information": it displays the currently played track's interpret, album and title (see screenshot), which is updated whenever the track on your Android device changes. This is confirmed at least for the following apps:

* the stock (AOSP) music player
* Cyanogen's *Apollo*
* [DJD Player](https://github.com/mikaelstaldal/DJDPlayer)
* [GEM Player](https://github.com/SubstanceMobile/GEM)
* [Timber](https://f-droid.org/repository/browse/?fdid=naman14.timber)
* [AntennaPod](https://github.com/AntennaPod/AntennaPod)

But it somehow failed for [Jockey](https://github.com/marverenic/Jockey). If your Android device runs Lollipop (Android 5) or later, you might even see a progress bar on your Pebble (confirmed e.g. for *Timber* and *AntennaPod).*

With the *Music* watchapp active, you also can control those players via the three buttons on the right side of your Pebble: the upper button skips one title back, the lower forward. Pressing the middle button (labeled with three dots, as shown in the screenshot above) reveals a play/pause button, to fire the action press it again. Long-pressing the upper/lower button will even let you control the volume (see second screenshot).

### Health (not for Pebble Classic and Steel)
To activate the [*Health* app](https://help.getpebble.com/customer/en/portal/articles/2239065-pebble-health?b_id=8308), open the Application Manager in Gadgetbridge, long-press the "Health" entry, and select "Activate". The app then will collect healt data on your watch (steps and sleep data), and – provided you didn't deactivate it – Gadgetbridge will sync this data. If you selected "Pebble Health" as your preferred activity tracker, those data will be used on Gadgetbridge's "Your activity" screens:

[![Menu](https://i.imgur.com/jZfEhHmm.png)](https://i.imgur.com/jZfEhHm.png) [![Activity&Sleep](https://i.imgur.com/70YobbFm.png)](https://i.imgur.com/70YobbF.png) [![Sleep](https://i.imgur.com/OZ43x0Tm.png)](https://i.imgur.com/OZ43x0T.png) [![Steps](https://i.imgur.com/rlsTLYUm.png)](https://i.imgur.com/rlsTLYU.png)  
<sup>Context menu and activity screens; click images for larger variants)</sup>

With your Pebble connected, long-press its name and select "Your Activity" from the drop-down (first screenshot). You should then see a screen like in the second screenshot, summarizing your activity of the last 24 hours. From here you can swipe to the other screens (or tap their "tab" on the bottom of the screen). In case you wonder whether I have no heart (beats): the Pebble has no sensor for that, so it doesn't support it (screens are the same for MiBand, which does support heart rate). As you've probably already have discovered on the screenshots, you can browse through the days using the corresponding buttons in the upper part of the screen.

This is what it will look like on your Pebble:

[![Steps](https://i.imgur.com/DurBLw1m.png)](https://i.imgur.com/DurBLw1.png) [![Sleep](https://i.imgur.com/Vnev4Fem.png)](http://i.imgur.com/Vnev4Fe.png)  
<sup>Steps and Sleep on your Pebble watch (click images for larger variants)</sup>

Live activity (the 4th tab, missing in above screenshots) does not work with *Pebble Health,* health does not send live data (it can be used with the Mi Band). Gadgetbridge separates data from the Mi Band, Pebble Health, Misfit and Morpheuz. The database can be exported in the debug activity. It is a sqlite database, so you could use it with your own project to interpret collected data (also see [Exporting data - meaning of columns](https://github.com/Freeyourgadget/Gadgetbridge/issues/332) if you're interested in this).


### Notifications
[![Notifications](https://i.imgur.com/togixyRs.png)](https://i.imgur.com/togixyR.png) [![Notifications](https://i.imgur.com/CVOfpkys.png)](https://i.imgur.com/CVOfpky.png)  
<sup>Notifications on the Pebble</sup>

This is the place where you can find all notifications which were sent to your Pebble – including those you've missed to read. The watchapp allows you to read them, or clear them *all* out (but not to clear selected entries). Consider this to be your "notification history".

### Alarms
[![Alarms](https://i.imgur.com/io9CNCKs.png)](https://i.imgur.com/io9CNCK.png) [![Alarms](https://i.imgur.com/rvFR6Jds.png)](https://i.imgur.com/rvFR6Jd.png) [![Alarms](https://i.imgur.com/ZnetpJqs.png)](https://i.imgur.com/ZnetpJq.png) [![SmartAlarm](https://i.imgur.com/9wW26wts.png)](https://i.imgur.com/9wW26wt.png) [![SetAlarm](https://i.imgur.com/AKDk7wX.gif)](https://i.imgur.com/rMWwBTg.gif)  
<sup>Alarms on the Pebble</sup>

You can [setup alarms directly on your Pebble](https://help.getpebble.com/customer/portal/articles/2415680-alarms-smart-alarms?b_id=8308): either "normal alarms" that fire exactly at the time configured, or "smart alarms" (not on Pebble Classic and Steel) which fire at a point in the specified interval – avoiding to get you up on the wrong side of bed by not firing while you're in a phase of deep-sleep. For both types, you can define which days they should be enabled – and you can setup multiple alarms, and use different vibration patterns (not on Pebble Classic an Steel). Unfortunately, it's not possible to [sync Pebble alarms with your stock Android alarms](https://github.com/Freeyourgadget/Gadgetbridge/issues/317).

Oh: do not expect some nice music or birds sound to wake you app. The Pebble has no speaker for that. Instead, it will "hum" (vibrate).

### Watchfaces
[![Watchfaces](https://i.imgur.com/Tp0VMBms.png)](https://i.imgur.com/Tp0VMBm.png) [![Watchfaces](https://i.imgur.com/pAqDJDRs.png)](https://i.imgur.com/pAqDJDR.png)  
<sup>Watchfaces on the Pebble</sup>

If you have multiple watch faces installed, this is where you can switch between them. Use the top and bottom buttons on your Pebble's right side to navigate, and the middle button to select the face you wish to see.


### Sport and Golf
*Sport* and *Golf* are some kind of barebone apps. It is possible for companion apps to

* start and stop them
* set the values you see on screen
* customize the name and icon
* react to buttons when the app is started

[![Sport](https://i.imgur.com/dYxzWKes.png)](https://i.imgur.com/dYxzWKe.png)  
<sup>The *Sport* watchapp</sup>

[![Golf](https://i.imgur.com/T6XYIHds.png)](https://i.imgur.com/T6XYIHd.png)  
<sup>The *Golf* watchapp</sup>

Gadgetbridge does have support for all these except for changing the icon (of course you need to "Allow 3rd Party Android App Access" in Gadgetbridge [Pebble specific settings](https://github.com/Freeyourgadget/Gadgetbridge/wiki/Configuration#pebble-specific-settings) first). One app known to work with this is [RunnerUp](https://f-droid.org/repository/browse/?fdfilter=runnerup&fdid=org.runnerup).

The Golf App should also work with Gadgetbridge, although it is untested. [Freecaddie](https://www.freecaddie.com/) and [Golf Pad Gps](http://golfpadgps.com/) seem to be a golf companion apps with Pebble support.