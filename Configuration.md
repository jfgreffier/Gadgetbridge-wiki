### Contents
* [General settings](#general-settings)
* [Pebble specific settings](#pebble-specific-settings)
* [Mi Band specific settings](#mi-band-specific-settings)

Tapping the overflow menu in the upper-right of the Gadgetbridge main screen, you get the option to enter configuration:

[![OverflowMenu](https://i.imgur.com/XBZGxkVm.png)](https://i.imgur.com/XBZGxkV.png)  
<sup>Overflow Menu: Chose to edit settings, debug settings, or exit Gadgetbridge</sup>

### General settings
As we want to configure Gadgetbridge, we obviously chose the first item – which leads us to the screen with general settings:

[![GeneralSettings (1)](https://i.imgur.com/6SkGlEXm.png)](https://i.imgur.com/6SkGlEX.png) [![GeneralSettings (2)](https://i.imgur.com/x5CXDcim.png)](https://i.imgur.com/x5CXDci.png) [![GeneralSettings (3)](https://i.imgur.com/KR1Hy92m.png)](https://i.imgur.com/KR1Hy92.png)  
<sup>The General Settings screen (click images for larger variants)</sup>

Most of the items here are pretty much self explaining. Nevertheless, I'll mention each of them with at least a short description:

* **General Settings**
  * **Connect when Bluetooth activated:** if checked, Gadgetbridge will try to automatically connect your Gadget as soon as Bluetooth gets toggled on.
  * **Reconnect automatically:** check this if you want Gadgetbridge to automatically try reconnecting your Gadget in case the connection was lost.
  * **Preferred Audioplayer:** tapping this will open a popup listing audio players Gadgetbridge has found on your Android device, and lets you pick one. You can leave this on „Default“ or explicitly select your favorite player if you encounter issues with your Gadgets remote-controlling.
  * **Theme:** this is for the Gadgetbridge app itself, and lets you chose between a dark and a bright skin.
  * **Language:** Gadgetbridge uses the system language by default. Here you can override this if you want.
  * **Sync time:** Whether Gadgetbridge should synchronize date and time from your Android device with your Gadget (usually updating the latter). When checked, this is done each time the Gadget gets connected, and whenever you change date/time or timezone on your Android device.
* **Notifications**
  * **Phone Calls:** chose whether incoming calls should be signalled to your Gadget.
  * **SMS:** chose when incoming SMS should cause notifications on your Gadget: always, only when your Android device's screen is off, never.
  * **K9-Mail:** similar to SMS but for mails if you use the great *K9-Mail* client.
  * **Pebble Messages:** again similar to SMS, but for Pebble companion apps.
  * **Generic notification support:** tapping that lets you tell the Android system to allow Gadgetbridge accessing notifications (so it can forward them to your Gadget at all) or not. An additional checkbox allows you to define whether those "other notifications" should also be sent to your Gadget when the Android device's screen is on.
  * **Blacklist Apps:** this opens a picker where you can exclude apps from having their notifications forwarded to your Gadget.
  * **Canned Replies:** define answers to pick from „interactive notifications“, so you can e.g. answer SMS directly from your Gadget. This currently only works for Pebble.
  * **About You:** Details on your person. These are sent to the Mi Band and Pebble Health to magically adjust their algorithms. We just know they have to be sent but we do not really know what happens on the device because firmware is not open source.
* **Device specific settings**  
  Here you can configure things specific to the device you're using (see below).
* **Developer Options**
  * **Write Log Files:** Whether Gadgetbridge should create its own log. You won't need that normally, but might be asked to activate it for troubleshooting when you've opened an issue in [our issue tracker](/Freeyourgadget/Gadgetbridge/issues).


### Pebble specific settings
[![PebbleSettings (1)](https://i.imgur.com/fkyMVcPm.png)](https://i.imgur.com/fkyMVcP.png) [![PebbleSettings (2)](https://i.imgur.com/iGjbTbOm.png)](https://i.imgur.com/iGjbTbO.png)  
<sup>Pebble specific settings</sup>

* **General settings**
  * **Allow 3rd Party Android App Access:** You'll need to check this if you want to use Pebble apps that come with their own Android companions, and the two should be able to communicate. Note that this is currently in experimental state, and does not always work. See [[PebbleKit Android App Compatibility]] for details.
  * **Reconnection Attempts:** How often should Gadgetbridge try to reconnect your Pebble once the connection was lost (but Bluetooth still active). Default is 12, but you can increase that: Reconnection tries are repeated in 2<sup>n</sup> seconds initially, and then all 64 seconds when that number was reached – which means the 12 corresponds to rawly 7 minutes until Gadgetbridge will give up. Setting it to 120 lets Gadgetbridge retry for about two hours before giving up. As there's an interval of 64 seconds before each additional try, the impact on your Android device's battery should be not noticable.
  * **Sunrise and Sunset:** whether to push sunrise/sunset times to your Pebble's timeline (only for devices supporting timeline, i.e. all the *Pebble Time* devices and older Pebbles with a firmware having timeline support added)
  * **Preferred Activitytracker:** Which activity tracker Gadgedbridge shall use as data source to display your activity data. This opens a popup to let you chose between *Pebble Health,* *Misfit* and *Morpheuz* (note *Morpheuz/Misfit* must be installed on your Pebble (and sync be enabled, see next item) before you can use them – they are still selectable without the (watch) apps being installed, but Gadgetbridge then or course couldn't obtain any data from them.
  * **Sync Pebble Health/Misfit/Morpheuz:** Which activity trackers you want to sync. Doesn't hurt to have options for [Misfit](https://help.getpebble.com/customer/portal/articles/1710334-misfit) / [Morpheuz](https://github.com/JamesFowler42/morpheuz20) turned on here if it's not installed. You'll only really need to disable things here when dealing with [[Multiple devices]].
* **Location**
  * **Acquire Location:** tapping this causes Gadgetbridge to obtain your location and fill the following two fields.
  * **Latitude/Longitude:** your current location. Gets filled automatically by tapping the entry above. Tapping the latitude/longitude fields also allows you to manually enter your location. These values are used for sunrise/sunset times.
* **Developer Options**
  * **Force Notification Protocol:** if checked, enforces the latest notification protocol available by your Pebble's firmware. This is a legacy option which only does something for 2.x firmware users: It forces 2.x style (instead of 1.x style) notifications instead in all cases. If is is not checked, for email notifications 1.x style notifications are used, because we can set an email icon there (but we wont have a context menu on the pebble then). Enable only if you know what you're doing – or being told by our devs.
  * **Enable untested features:** checking this will make some additional system apps visible in the Gadgetbridge App Manager (see [[Pebble Watchfaces]] for details). These include e.g. *Golf* and *Sport* – which are both rather „bare bones apps“: tapping their entry from the App Manager will show their interfaces on your Pebble, but won't let you do much with them. But you then can e.g. install the [RunnerUp](https://f-droid.org/repository/browse/?fdfilter=runnerup&fdid=org.runnerup) Sports activities tracker, which then will automatically start the *Sports* app on your device and use it as display – provided you've enabled *Allow access from other Android apps* (see above in the *General Settings* section). There might be other companions making use of these (also see [here](https://github.com/Freeyourgadget/Gadgetbridge/issues/322#issuecomment-223714965) for details). *Untested Features* also includes the possibility to [configure some watchfaces](https://github.com/Freeyourgadget/Gadgetbridge/issues/251) which offer HTML configuration pages via their "configure" menu entry when long-pressing an app in the watchapp list.
  * **Emulator IP:**
  * **Emulator Port:**

### Mi Band specific settings
[![MiBandSettings (1)](https://i.imgur.com/NJA87grm.png)](https://i.imgur.com/NJA87gr.png) [![MiBandSettings (2)](https://i.imgur.com/TzW42fTm.png)](https://i.imgur.com/TzW42fT.png)  
<sup>Mi Band specific settings (click images for larger variants)</sup>