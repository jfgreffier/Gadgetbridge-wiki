### Contents
* [General settings](#general-settings)
* [Pebble specific settings](#pebble-specific-settings)
* [Mi Band specific settings](#mi-band-specific-settings)

Tapping the overflow menu in the upper-right of the Gadgetbridge main screen, you get the option to enter configuration:

[![OverflowMenu](http://i.imgur.com/Y4F516Fm.png)](http://i.imgur.com/Y4F516F.png)  
<sup>Overflow Menu: Chose to edit settings, debug settings, or exit Gadgetbridge</sup>

### General settings
As we want to configure Gadgetbridge, we obviously chose the first item – which leads us to the screen with general settings:

[![GeneralSettings (1)](http://i.imgur.com/PgXDB72m.png)](http://i.imgur.com/PgXDB72.png) [![GeneralSettings (2)](http://i.imgur.com/2h0Qabsm.png)](http://i.imgur.com/2h0Qabs.png) [![GeneralSettings (3)](http://i.imgur.com/432CvREm.png)](http://i.imgur.com/432CvRE.png)  
<sup>The General Settings screen (click images for larger variants)</sup>

Most of the items here are pretty much self explaining. Nevertheless, I'll mention each of them with at least a short description:

* **General Settings**
  * **Connect when Bluetooth activated:** if checked, Gadgetbridge will try to automatically connect your Gadget as soon as Bluetooth gets toggled on.
  * **Automatically reconnect:** check this if you want Gadgetbridge to automatically try reconnecting your Gadget in case the connection was lost.
  * **Preferred audio player:** tapping this will open a popup listing audio players Gadgetbridge has found on your Android device, and lets you pick one. You can leave this on „Default“ or explicitly select your favorite player if you encounter issues with your Gadgets remote-controlling.
  * **Skin:** this is for the Gadgetbridge app itself, and lets you chose between a dark and a bright skin.
  * **Synchronize time:** Whether Gadgetbridge should synchronize date and time from your Android device with your Gadget (usually updating the latter). When checked, this is done each time the Gadget gets connected, and whenever you change date/time or timezone on your Android device.
* **Notifications**
  * **Calls:** chose whether incoming calls should be signalled to your Gadget.
  * **SMS:** chose when incoming SMS should cause notifications on your Gadget: always, only when your Android device's screen is off, never.
  * **K9-Mail:** similar to SMS but for mails if you use the great *K9-Mail* client.
  * **Pebble notifications:** again similar to SMS, but for Pebble companion apps.
  * **Other notifications:** tapping that lets you tell the Android system to allow Gadgetbridge accessing notifications (so it can forward them to your Gadget at all) or not. An additional checkbox allows you to define whether those "other notifications" should also be sent to your Gadget when the Android device's screen is on.
  * **Lock Apps:** this opens a picker where you can exclude apps from having their notifications forwarded to your Gadget.
  * **Predefined answers:** {define answers to pick from „interactive notifications“, so you can e.g. answer SMS directly from your Gadget}
  * **About yourself:** {Details on your person}
* **Device specific settings**  
  Here you can configure things specific to the device you're using (see below).
* **Developer options**
  * **Write logs:** Whether Gadgetbridge should create its own log. You won't need that normally, but might be asked to activate it for troubleshooting when you've opened an issue in [our issue tracker](/Freeyourgadget/Gadgetbridge/issues).


### Pebble specific settings
[![PebbleSettings](http://i.imgur.com/0npwl5zm.png)](http://i.imgur.com/0npwl5z.png)  
<sup>Pebble specific settings</sup>

* **General settings**
  * **Allow access from other Android apps:** You'll need to check this if you want to use Pebble apps that come with their own Android companions, and the two should be able to communicate. Note that this is currently in experimental state, and does not always work. See [[PebbleKit Android App Compatibility]] for details.
  * **Reconnection tries:** How often should Gadgetbridge try to reconnect your Pebble once the connection was lost (but Bluetooth still active). Default is 12, but you can increase that: Reconnection tries are repeated in 2<sup>n</sup> seconds initially, and then all 64 seconds when that number was reached – which means the 12 corresponds to rawly 7 minutes until Gadgetbridge will give up. Setting it to 120 lets Gadgetbridge retry for about two hours before giving up. As there's an interval of 64 seconds before each additional try, the impact on your Android device's battery should be not noticable.
  * **Preferred activity tracker:** opens a popup to let you chose between *Pebble Health,* *Misfit* and *Morpheus* (note *Morpheus/Misfit* must be installed before you can use them; they are still selectable without the apps being installed, but then Gadgetbridge wouldn't process/save health data – useful e.g. if you [connect your Pebble to multiple Android devices](https://github.com/Freeyourgadget/Gadgetbridge/issues/322#issuecomment-223765820) and don't want to end up with incomplete health data on each of them; note this trick won't work if you use *Morpheus/Misfit*, see [here](https://github.com/Freeyourgadget/Gadgetbridge/issues/322#issuecomment-223773016)).
* **Developer Options**
  * **enforce notification protocol:** if checked, enforces the latest notification protocol available by your Pebble's firmware. {enable only if you know what you're doing – or being told by our devs}
  * **Activate untested features:** checking this will make some additional system apps visible in the Gadgetbridge App Manager (see [[Pebble Watchfaces]] for details). These include e.g. *Golf* and *Sport* – which are both rather „bare bones apps“: tapping their entry from the App Manager will show their interfaces on your Pebble, but won't let you do much with them. But you then can e.g. install the [RunnerUp](https://f-droid.org/repository/browse/?fdfilter=runnerup&fdid=org.runnerup) Sports activities tracker, which then will automatically start the *Sports* app on your device and use it as display – provided you've enabled *Allow access from other Android apps* (see above in the *General Settings* section). There might be other companions making use of these (also see [here](https://github.com/Freeyourgadget/Gadgetbridge/issues/322#issuecomment-223714965) for details).
  * **Emulator IP:**
  * **Emulator Port:**

### Mi Band specific settings
[![MiBandSettings (1)](http://i.imgur.com/JB6lk0km.png)](http://i.imgur.com/JB6lk0k.png) [![MiBandSettings (2)](http://i.imgur.com/xM5nPFJm.png)](http://i.imgur.com/xM5nPFJ.png)  
<sup>Mi Band specific settings (click images for larger variants)</sup>