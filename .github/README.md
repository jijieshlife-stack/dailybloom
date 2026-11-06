# Daily Bloom – Android project

This is a small native Android wrapper around the Daily Bloom routine interface.
The routine itself is bundled inside the app, so it opens offline and stores
checkmarks and priorities locally on the phone using WebView local storage.

## Build an APK

1. Install Android Studio on a computer.
2. Open Android Studio → **Open** → select this `DailyBloom` project folder.
3. Allow Android Studio to sync Gradle and install any requested Android SDK.
   The project uses Android Gradle Plugin 8.7.3, Kotlin 2.0.21, and compile SDK 35.
4. Choose **Build → Build Bundle(s) / APK(s) → Build APK(s)**.
5. When the build completes, choose **locate**. The APK is normally at:
   `app/build/outputs/apk/debug/app-debug.apk`
6. Transfer that APK to your Android phone, open it, and allow installation
   from that source if Android asks.

## Offline behavior

- The checklist, priorities, progress and five prayer checkboxes work offline.
- Checkmarks are saved locally on the phone, grouped by Cairo calendar date.
- The five prayer names are included, but this offline version does not calculate
  or download changing adhan times. Follow your local Cairo prayer timetable.
- No account, analytics, or internet permission is included.

## Package details

- App name: Daily Bloom
- Application ID: `com.dailybloom.gigi`
- Minimum Android: Android 6.0 (API 23)
- Version: 1.0


## Build automatically in GitHub (no Android Studio needed)

This project includes `.github/workflows/build-apk.yml`.

1. On a computer, create a GitHub account if you do not already have one.
2. Create a new repository, for example `daily-bloom`.
3. Extract this ZIP. Upload the **contents** of the `daily_bloom_android_project` folder
   into the root of that repository (including the hidden `.github` folder).
4. Open the repository's **Actions** tab. If prompted, enable workflows.
5. Run **Build Daily Bloom APK** using **Run workflow**, or push/commit a change.
6. When the run finishes successfully, open the run, scroll to **Artifacts**, and
   download `Daily-Bloom-APK`.
7. Extract the downloaded artifact ZIP. It contains `app-debug.apk`.
8. Send `app-debug.apk` to your Samsung phone, tap it, and follow Android's
   installation prompts. If asked, allow installation from that source.

The APK is a debug-signed personal-use build. It is suitable for installing on your
own phone; it is not a Play Store release. GitHub account/repository setup is required
for this cloud-build route.
