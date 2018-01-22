_Unfortunately we have no control on when a new release will appear on f-droid, but there are a few steps you can perform to check by yourself and follow the progress._

The last step we perform to mark the codebase as ready to be released by f-droid, is to add a _tag_ to our codebase. This tag is an information for the f-droid buildbot that a new version is ready, and must be "picked up" by the build bot. This happens automatically, usually within a few hours, but **we have no control over this part of the process**.

### How to check if f-droid picked up a new release

Open the [metadata page](https://gitlab.com/fdroid/fdroiddata/blob/master/metadata/nodomain.freeyourgadget.gadgetbridge.txt) on f-droid's gitlab repository and check if the new tag was added at the end of the file. The number that follows the comma on each ``Build:`` line is the build number, that you will need in the next step.


After the new release has been "picked up", the actual application must be built by f-droid. This happens automatically, usually within a few days, but **we have no control over this part of the process**.

### How to check if f-droid built a new release (that was picked up)

Open the [wiki page](https://f-droid.org/wiki/page/nodomain.freeyourgadget.gadgetbridge). The blue box on the right contains a label ``Updated:``. This is the last time the application was built by f-droid, and if you follow the link you will see the "build status". You will notice that the page title (and URL) contain a number, something like ``lastbuild_100``, in this case 100 is the build number. You can change the URL manually using the build number you noted in the previous step, if you want to be sure that you are seeing the results of that version.

After the new release has been built, the resulting apk must be signed by f-droid, the index of the main repository must be rebuilt and the new apk made available. This happens automatically, usually within a few days, but **we have no control over this part of the process**.

### How to check if f-droid signed a new release (that was built), updated the index and made the apk available

Unfortunately we have no idea how to follow these steps. We can just wait for the updated application to be available within f-droid.
