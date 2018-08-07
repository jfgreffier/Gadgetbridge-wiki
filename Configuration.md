### Contents
* [General settings](#general-settings)
* [Pebble specific settings](#pebble-specific-settings)
* [Mi Band / Amazfit specific settings](#mi-band--amazfit-specific-settings)

Tapping the overflow menu in the upper-right of the Gadgetbridge main screen, you get the option to enter configuration:

[![OverflowMenu](https://i.imgur.com/XBZGxkVm.png)](https://i.imgur.com/XBZGxkV.png)  
<sup>Overflow Menu: Chose to edit settings, debug settings, or exit Gadgetbridge</sup>

### General settings
As we want to configure Gadgetbridge, we obviously choose the first item – which leads us to the screen with general settings:

[![GeneralSettings (1)](https://i.imgur.com/AKDMGs0m.png)](https://i.imgur.com/AKDMGs0.png) [![GeneralSettings (2)](https://i.imgur.com/kIm58q3m.png)](https://i.imgur.com/kIm58q3.png) [![GeneralSettings (3)](https://i.imgur.com/3xAZiBcm.png)](https://i.imgur.com/3xAZiBc.png)  
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
  * **Blacklist Apps:** this opens a picker where you can exclude apps from having their notifications forwarded to your Gadget. You have two options: ``NOTIF`` and ``PEBBLE``: the former will prevent android notification from reaching your gadget, the latter will block Pebble Messages. For instance OsmAnd is known to send many Pebble Messages when using the navigation functionality and you might want to block these.
  * **About You:** Details on your person. These are sent to the Mi Band/Amazfit and Pebble Health to magically adjust their algorithms. We just know they have to be sent but we do not really know what happens on the device because firmware is not open source.
* **Device specific settings**  
  Here you can configure things specific to the device you're using (see below).
* **Developer Options**
  * **Write Log Files:** Whether Gadgetbridge should create its own log. You won't need that normally, but might be asked to activate it for troubleshooting when you've opened an issue in [our issue tracker](/Freeyourgadget/Gadgetbridge/issues).


### Pebble specific settings
[![PebbleSettings (1)](https://i.imgur.com/SRIEZYvm.png)](https://i.imgur.com/SRIEZYv.png) [![PebbleSettings (2)](https://i.imgur.com/eEJ5caxm.png)](https://i.imgur.com/eEJ5cax.png)  
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
* **[Canned Messages](https://github.com/Freeyourgadget/Gadgetbridge/wiki/Calls-and-SMS#configure-canned-replies)**
  * **Replies:** define answers to pick from „interactive notifications“, so you can e.g. answer SMS directly from your Gadget.
  * **Call Dismissal:** Here you can setup "canned replies" for call rejection, which enables you to reject a call with an SMS (e.g. informing the calling party you're in a meeting and will call back later).
* **Developer Options**
  * **Force Notification Protocol:** if checked, enforces the latest notification protocol available by your Pebble's firmware. This is a legacy option which only does something for 2.x firmware users: It forces 2.x style (instead of 1.x style) notifications instead in all cases. If is is not checked, for email notifications 1.x style notifications are used, because we can set an email icon there (but we wont have a context menu on the pebble then). Enable only if you know what you're doing – or being told by our devs.
  * **Enable untested features:** checking this will make some additional features available which are either not yet tested thoroughly to be called "stable", or are otherwise primarily intended for developers and testers. What exactly is covered by that is subject to change between versions, so we won't document that here.
  * **Emulator IP:**
  * **Emulator Port:**


### Mi Band / Amazfit specific settings
[![MiBandSettings (1)](https://i.imgur.com/NJA87grm.png)](https://i.imgur.com/NJA87gr.png) [![MiBandSettings (2)](https://i.imgur.com/TzW42fTm.png)](https://i.imgur.com/TzW42fT.png)  
<sup>Mi Band specific settings (click images for larger variants)</sup>

* **About you**
  * **Name/Alias:** This is the name you want to give to your Mi Band/Amazfit, can be anything.
  * **Wearing left or right?:** Set which arm you are going to wear your Mi Band/Amazfit on.
  * **Target steps for each day:** The goal of steps you want to reach, can be any number you want.
  * **Alarms to reserve for upcoming events:** Mi Band/Amazfit have a limit of three alarms that can be configured. They will alert you even when the band is not connected to your mobile, e.g. in order to wake you up. Press the Mi Band/Amazfit items in the main screen to configure alarms. This setting tells Gadgetbridge how many alarms shall be reserved for reminders of calendar events. These will not be user configurable then.
  * **Use Heartrate Sensor to improve sleep:** Only for Mi Band 1S at the moment. When this is selected Gadgetbridge will make use of the Heartrate sensor to better detect when you are sleeping. 
  * **Device time offset in hours (for detecting sleep of shift workers):** The Mi Band device currently records sleep only if it happens after 10pm and before 7am. The offset is used to trick the device to record sleep in non-standard hours. If you usually sleep, say, from 6am to 2pm, set the shift to -8, so at 6am the device thinks it's still 10pm of the day before.
* **Vibration settings**
  * Each setting here allows you to set a different vibration pattern for each type of notification.
* **Developer options**
  * Special settings reserved for developers, leave as is unless you know what you are doing.