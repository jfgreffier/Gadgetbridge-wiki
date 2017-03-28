The Pebble watch ships with several system apps. Some of them are visible in Gadgetbridge's *Application Manager* by default (Music), some need to be activated from within Gadgetbridge's *Application Manager* to do their work on your Pebble (Health), and others are hidden by default in the *Application Manager* unless "untested features" are enabled (Sport, Golf – see [Pebble specific settings](https://github.com/Freeyourgadget/Gadgetbridge/wiki/Configuration#pebble-specific-settings); they'll work on your Pebble though when a matching third-party companion app triggers them).

### Music
[![Music](https://i.imgur.com/SsWWSzPs.png)](https://i.imgur.com/SsWWSzP.png) [![Music](https://i.imgur.com/sKwyaWKs.png)](https://i.imgur.com/sKwyaWK.png) [![Volume Control](https://i.imgur.com/FR8Uk9ss.png)](https://i.imgur.com/FR8Uk9s.png)  
<sup>*Music* on the *Pebble Time Steel*</sup>

*Music* works well with most players – though often only for „basic information“: it displays the currently played track's interpret, album and title (see screenshot), which is updated whenever the track on your Android device changes. This is confirmed at least for the following apps:

* the stock (AOSP) music player
* Cyanogen's *Apollo*
* [DJD Player](https://github.com/mikaelstaldal/DJDPlayer)
* [GEM Player](https://github.com/SubstanceMobile/GEM)
* [Timber](https://f-droid.org/repository/browse/?fdid=naman14.timber)
* [AntennaPod](https://github.com/AntennaPod/AntennaPod)

But it somehow failed for [Jockey](https://github.com/marverenic/Jockey). If your Android device runs Lollipop (Android 5) or later, you might even see a progress bar on your Pebble (confirmed e.g. for *Timber* and *AntennaPod).*

With the *Music* watchapp active, you also can control those players via the three buttons on the right side of your Pebble: the upper button skips one title back, the lower forward. Pressing the middle button (labeled with three dots, as shown in the screenshot above) reveals a play/pause button, to fire the action press it again. Long-pressing the upper/lower button will even let you control the volume (see second screenshot).

<sup>(Note that on Kitkat using external controls like these can lead to a [full-time wake-lock](https://github.com/Freeyourgadget/Gadgetbridge/issues/322#issuecomment-226942564).)</sup>

### Health (not for Pebble Classic and Steel)
To activate the [*Health* app](https://help.getpebble.com/customer/en/portal/articles/2239065-pebble-health?b_id=8308), open the „Application Manager“ in Gadgetbridge (second icon in the first screenshot below), long-press the „Health“ entry, and select „Activate“. The app then will collect healt data on your watch (steps and sleep data), and – provided you didn't deactivate it – Gadgetbridge will sync this data. If you selected „Pebble Health“ as your preferred activity tracker, those data will be used on Gadgetbridge's „Your activity“ screens:

[![Menu](https://i.imgur.com/iJPrv0tm.png)](https://i.imgur.com/iJPrv0t.png) [![Activity&Sleep](https://i.imgur.com/70YobbFm.png)](https://i.imgur.com/70YobbF.png) [![Sleep](https://i.imgur.com/OZ43x0Tm.png)](https://i.imgur.com/OZ43x0T.png) [![Sleep Weekly](https://i.imgur.com/glI9jpzm.png)](https://i.imgur.com/glI9jpz.png) [![Steps](https://i.imgur.com/rlsTLYUm.png)](https://i.imgur.com/rlsTLYU.png)  
<sup>Context menu and activity screens; click images for larger variants)</sup>

With your Pebble connected, tap the „Activity“ button (see first screenshot). You should then see a screen like in the second screenshot, summarizing your activity of the last 24 hours. From here you can swipe to the other screens (or tap their „tab“ on the bottom of the screen). In case you wonder whether I have no heart (beats): the Pebble has no sensor for that, so it doesn't support it (screens are the same for MiBand, which does support heart rate). As you've probably already have discovered on the screenshots, you can browse through the days using the corresponding buttons in the upper part of the screen.

This is what it will look like on your Pebble:

[![Steps](https://i.imgur.com/DurBLw1m.png)](https://i.imgur.com/DurBLw1.png) [![Sleep](https://i.imgur.com/Vnev4Fem.png)](http://i.imgur.com/Vnev4Fe.png)  
<sup>Steps and Sleep on your Pebble watch (click images for larger variants)</sup>

Live activity (the 4th tab, missing in above screenshots) does not work with *Pebble Health,* health does not send live data (it can be used with the Mi Band). Gadgetbridge separates data from the Mi Band, Pebble Health, Misfit and Morpheuz. The database can be exported in the debug activity. It is a sqlite database, so you could use it with your own project to interpret collected data (also see [Exporting data - meaning of columns](https://github.com/Freeyourgadget/Gadgetbridge/issues/332) if you're interested in this).


### Notifications
[![Notifications](https://i.imgur.com/togixyRs.png)](https://i.imgur.com/togixyR.png) [![Notifications](https://i.imgur.com/CVOfpkys.png)](https://i.imgur.com/CVOfpky.png)  
<sup>Notifications on the Pebble</sup>

This is the place where you can find all notifications which were sent to your Pebble – including those you've missed to read. The watchapp allows you to read them, or clear them *all* out (but not to clear selected entries). Consider this to be your „notification history“.

### Alarms
[![Alarms](https://i.imgur.com/io9CNCKs.png)](https://i.imgur.com/io9CNCK.png) [![Alarms](https://i.imgur.com/rvFR6Jds.png)](https://i.imgur.com/rvFR6Jd.png) [![Alarms](https://i.imgur.com/ZnetpJqs.png)](https://i.imgur.com/ZnetpJq.png) [![SmartAlarm](https://i.imgur.com/9wW26wts.png)](https://i.imgur.com/9wW26wt.png) [![SetAlarm](https://i.imgur.com/AKDk7wX.gif)](https://i.imgur.com/rMWwBTg.gif)  
<sup>Alarms on the Pebble</sup>

You can [setup alarms directly on your Pebble](https://help.getpebble.com/customer/portal/articles/2415680-alarms-smart-alarms?b_id=8308): either „normal alarms“ that fire exactly at the time configured, or „smart alarms“ (not on Pebble Classic and Steel) which fire at a point in the specified interval – avoiding to get you up on the wrong side of bed by not firing while you're in a phase of deep-sleep. For both types, you can define which days they should be enabled – and you can setup multiple alarms, and use different vibration patterns (not on Pebble Classic an Steel). Unfortunately, it's not possible to [sync Pebble alarms with your stock Android alarms](https://github.com/Freeyourgadget/Gadgetbridge/issues/317).

Oh: do not expect some nice music or birds sound to wake you app. The Pebble has no speaker for that. Instead, it will „hum“ (vibrate).

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


### Weather
Starting with version 0.17, *Gadgetbridge* offers support for weather information on your Pebble. To do this without requiring the `INTERNET` permission for itself, this requires the help of a weather provider on your Android device – which is provided by the [Weather notification](https://f-droid.org/repository/browse/?fdid=ru.gelin.android.weather.notification) app available at *F-Droid.*

[![InstallApp](https://i.imgur.com/5pxDZVKm.png)](https://i.imgur.com/5pxDZVK.png) [![ActivateWeather](https://i.imgur.com/372DQFvm.png)](https://i.imgur.com/372DQFv.png) [![ActivateSkin](https://i.imgur.com/AeWeT5Zm.png)](https://i.imgur.com/AeWeT5Z.png)  
<sup>Install the Weather Notification app / activate Pebble Weather app / activate the skin</sup>

If your Pebble runs firmware 4.x, just open *Gadgetbridge,* tap the „App Manager“ icon of your device, and switch to the „Installed Apps“ tab. There you should find an app labeled „Weather (System)“. Long tap that. If you didn't yet install the afore mentioned weather provider, you will be prompted to do so now (first screenshot above this paragraph). Tapping the prompt will open your web browser with the app's page at *F-Droid,* where you can use the APK download link. Alternatively, open your *F-Droid* app, search for „Weather notification“, and install it that way. Once installed and long-pressing the entry again, you should see something like in the second screenshot – and can enable the Pebble „Weather“ system app.

If your device runs a lower firmware version, you won't have that system app available. In this case, just make sure you install the „provider“ from *F-Droid* as described, and continue with the next step. Weather will still be available to the watchfaces.

Now, you must enable the *Gadgetbridge* skin in the *Weather notification* app: start the app, and flip the switch as shown in the third screenshot. If you don't want weather information in your notification area, flip off the „Default Skin“. Feel free to adjust the other settings; for weather to work with your Pebble and *Gadgetbridge* you're already done now.

[![WeatherApp](https://i.imgur.com/PZVkcscs.png)](https://i.imgur.com/PZVkcsc.png) [![Healthify](https://i.imgur.com/oXW7XI7s.png)](https://i.imgur.com/oXW7XI7.png) [![TrekVolle](https://i.imgur.com/YBcgJUOs.png)](https://i.imgur.com/YBcgJUO.png)  
<sup>Pebble Weather app / weather with the [Healthify](https://apps.getpebble.com/en_US/application/57caac70be5ad0a9cf000167?section=watchfaces&dev_settings=true) watchface / weather with the [TrekVolle](https://apps.getpebble.com/en_US/application/56bb35ee90610aa83400000f?dev_settings=true&section=watchfaces) watchface</sup>

For watchfaces to show weather information, *Gadgetbridge* must adapt to them. Check with the [Pebble weather for watchface requests](https://github.com/Freeyourgadget/Gadgetbridge/issues/482) issue if your candidate already is supported. If it's not, you can ask there for it to be added. Please understand that this requires a look into the watchface's code – so it being Open Source would help a lot here.

Now, enjoy the weather in your watchface – as shown by the two examples above!