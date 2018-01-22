_Unfortunately we have no control on when a new release will appear on f-droid, but there are a few steps you can perform to check by yourself and follow the progress._

The last step we perform to mark the codebase as ready to be released by f-droid, is to add a _tag_ to our codebase. This tag is an information for the f-droid buildbot that a new version is ready, and must be "picked up" by the build bot. This happens automatically, usually within a few hours, but **we have no control over this part of the process**.

### How to check if f-droid picked up a new release

Open the [metadata page](https://gitlab.com/fdroid/fdroiddata/blob/master/metadata/nodomain.freeyourgadget.gadgetbridge.txt) on f-droid's gitlab repository and check if the new tag was added at the end of the file. The number that follows the comma on each ``Build:`` line is the build number, that you will need in the next step.


After the new release has been "picked up", the actual application must be built by f-droid. This happens automatically, usually within a few days, but **we have no control over this part of the process**.

### How to check if f-droid built a new release (that was picked up)

Open the [wiki page](https://f-droid.org/wiki/page/nodomain.freeyourgadget.gadgetbridge). The blue box on the right contains a label ``Updated:``. This is the last time the application was built by f-droid, and if you follow the link you will see the "build status". You will notice that the page title (and URL) contain a number, something like ``lastbuild_100``, in this case 100 is the build number. You can change the URL manually using the build number you noted in the previous step, if you want to be sure that you are seeing the results of that version.

After the new release has been built, the resulting apk must be signed by f-droid, the index of the main repository must be rebuilt and the new apk made available. This happens automatically, usually within a few days, but **we have no control over this part of the process**.

### How to check if f-droid signed a new release (that was built), updated the index and made the apk available

If an `.apk` was made available, this implies its being signed and the index updated – so we only need to check for the `.apk` here. For that, we have several options:

* Perform a manual refresh of the repo index(es) in your F-Droid client. If you have GB installed, you should be notified about an available update. If not, you still can search for the app and open its detail page – available builds should be listed.
* Visit the [Gadgetbridge web page on the F-Droid repo](https://f-droid.org/packages/nodomain.freeyourgadget.gadgetbridge/). In the "Packages" section, just below the blue "Download F-Droid" button, available packages are shown. What's listed here should reflect the latest index build.
* Download the `index.xml` manually and parse it (oops)

If you want to find out whether F-Droid has published any new apps or updates within a given time frame (aka "did they build anything at all lately?"), check with the [IzzyOnDroid Repo Browser](https://apt.izzysoft.de/fdroid/index.php?repo=main). Here you can filter by "added since" (new updates) and/or "updated since" (updates to already existing apps) to get an idea on "successful activity" in this context (the repo indexes at IzzyOnDroid are updated once per day, so they might not always reflect latest activities). Not only for the F-Droid main repo, by the way :wink: