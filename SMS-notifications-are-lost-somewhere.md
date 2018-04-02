**Problem**: 
You are using alternative SMS app (like Silence or Signal). Stock one is present and not disabled, but the alternative one is set up to be default.
All notifications but SMS are shown. Log says that *Gadgetbridge* is `Ignoring notification, is a system event`

**Solution**:
You have to disable SMS support in Gadgetbridge settings to fix your problem (change it to *Never*).

The reason is that we blacklist alternative SMS Apps in the generic notification receiver since it would otherwise result in double notifications (one picked up from the Android SMS receiver, and one picked up from the actual notification)

In case the SMS is encrypted, it would not make sense to use the SMS receiver, but only the notification receiver which already contains the decrypted content.