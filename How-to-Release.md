## How to create a new release
0. Make sure you are on master and on current HEAD
1. Run $ tx pull -a and check for new and updated translations
2. Add/commit translations, if applicable
3. Update CHANGELOG.md and commit
4. Adjust **versionName** and **versionCode** in app/build.gradle
5. Make sure it builds and testcases succeed
6. Push the changes
7. Tag the version and push the tag
8. Party!
