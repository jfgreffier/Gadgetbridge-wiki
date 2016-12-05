You can interact with incoming calls and SMS from your Pebble. For advanced features, you need to prepare your own Canned Replies:

## Configure Canned Replies
This can be done from the [Pebble specific settings](https://github.com/Freeyourgadget/Gadgetbridge/wiki/Configuration#pebble-specific-settings) in the "Canned Messages" section.

[![CallReject Messages](https://i.imgur.com/I781IQEm.png)](https://i.imgur.com/I781IQE.png) [![CannedReplySuffix](https://i.imgur.com/NgRr67Dm.png)](https://i.imgur.com/NgRr67D.png) [![CannedReply](https://i.imgur.com/WRh7W7rm.png)](https://i.imgur.com/WRh7W7r.png)  
<sup>Configure messages for call rejection (#1) and other canned replies (#2 and #3)</sup>

Tap an empty row here to add a new message, tap an existing entry to modify. When done, tap the top-row to "Update on Pebble" – i.e. to send your changes to your Pebble and make them available there.


## Reject calls
### Simple call rejection
[![Simple Reject](https://i.imgur.com/ZjuNQw5s.png)](https://i.imgur.com/ZjuNQw5.png) [![Simple Rejected](https://i.imgur.com/IxFeQrps.png)](https://i.imgur.com/IxFeQrp.png)  
<sup>Simple call rejection (with no canned responses set up)</sup>

With no canned messages set up, you can still reject incoming calls – as the screenshots above show: push the lower-right button, done. You'll see a simple red screen confirming the call was rejected (or "declined").

### Advanced call rejection
[![Advanced Reject](https://i.imgur.com/al0CTvns.png)](https://i.imgur.com/al0CTvn.png) [![Advanced Reject Menu](https://i.imgur.com/5gcuGCVs.png)](https://i.imgur.com/5gcuGCV.png) [![Advanced Reject Message](https://i.imgur.com/amabcdks.png)](https://i.imgur.com/amabcdk.png)  
<sup>Advanced call rejection with canned replies</sup>

Having set up some **canned messages,** you'll have one additional button available on incoming calls: pushing the upper-right button on your Pebble now first rejects the call, and then brings you to a menu as shown in the second screenshot. Now push the middle-right button for "Canned Messages", and you will see the messages you've setup before. Select one, and it is sent to the caller.

**Reply with Voice** is a feature available only on devices with a built-in microphone (e.g. Pebble Time). We can pretty much assume it will never work with Gadgetbridge unless a miracle happens and a working opensource library pops up that can do speech recognition (if you know such a library, please let us know).

**Emoji** lets you chose an emoji from a list. It is not our idea, its just there and we can't remove that.


## Reply to messages
As you might have noticed in the [Pebble specific settings](https://github.com/Freeyourgadget/Gadgetbridge/wiki/Configuration#pebble-specific-settings), you can also setup another section of canned "Replies". With those you are able to act on incoming SMS, but also on other Android wear compatible notifications such as in Signal or Conversations. It is meant to be general purpose, the only problem is that not many projects support wearable actions. Setup of the messages works the same way as [described above](#configure-canned-replies). Additionally, you can configure a "common suffix" to be appended to each of the canned replies when sending them out.