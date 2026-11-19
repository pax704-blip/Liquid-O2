CASH FLOW TRACKER  -  Android and iPhone app project

ANDROID  (free, no coding, about 15 minutes, no Android Studio needed)
1. Make a free account at github.com and create a new repository (any name).
2. Unzip this folder. In the repository click "Add file" > "Upload files" and drag in
   EVERYTHING from inside the folder (www, assets, package.json, capacitor.config.json, etc.). Commit.
3. Check the repository has a file at .github/workflows/android.yml.
   If it is missing: go to the Actions tab > "set up a workflow yourself", paste in the text of
   android-build.yml from this folder, and commit it.
4. Actions tab > "Build Android APK" > Run workflow. Wait about 5-10 minutes for the green tick.
5. Open the finished run, scroll to Artifacts, download "CashFlow-APK", unzip it to get app-debug.apk.
6. Send app-debug.apk to your phone and open it. Allow "install unknown apps" when asked.
   (Play Protect may show a warning because this is a personal test build; choose Install anyway.)

This is a debug build for your own devices. Publishing on Google Play needs a signed release build
(Android Studio plus a $25 one-time Play Console fee).

IPHONE
Apple only allows iPhone apps to be built on a Mac with Xcode and signed with an Apple Developer
account ($99 a year). On a Mac:
   npm install
   npx cap add ios
   npx cap sync ios
   npx cap open ios      (then press Run in Xcode, or use Product > Archive for TestFlight / App Store)
No Mac or paid account? The installable web version (CashFlowApp.zip, "Add to Home Screen" in Safari)
gives you the same app on iPhone, working offline.

YOUR DATA
Entries are stored inside the app on each device. Phone and PC do not share them.
In the app: Settings > "Save a backup file" / "Restore from backup" / "Export entries (CSV)".
Uninstalling the app deletes its data, so save a backup first.

CHANGE THE APP NAME OR ID
Edit capacitor.config.json (appName and appId) before building.
