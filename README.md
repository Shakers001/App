# MergeSMS — Green Edition

Native Android bulk SMS sender built with Java and Android SDK.

## Features
- Green-and-white interface with SMS-themed icons
- Import recipients from CSV (save Excel sheets as CSV first)
- Choose the phone-number column
- Select recipients individually or all at once
- Personalize message templates using CSV header placeholders, e.g. `Hello {name}`
- Send through the phone's SIM with confirmation and optional dual-SIM selection
- GitHub Actions workflow builds a debug APK

## Build on GitHub
1. Upload the **contents** of this folder to the root of a GitHub repository.
2. Push to the `main` branch, or open **Actions → Build MergeSMS Android APK → Run workflow**.
3. When the workflow succeeds, open the run and download the `MergeSMS-debug-APK` artifact.
4. Extract the artifact ZIP to get `app-debug.apk`.

The workflow is in `.github/workflows/build.yml`. It uses JDK 17, Android API 35, and Gradle 8.7.

## Notes
- CSV files must contain a header row. Up to 1,000 recipient rows are imported.
- SMS submission requires permission, a working SIM, and carrier service. Carrier charges may apply.
- Android's SMS service accepting a message does not confirm delivery.
- Test with a number you control before sending to a list.
- This project is not affiliated with Meridian Technologies; the UI is an original implementation inspired by common bulk-SMS workflows.
