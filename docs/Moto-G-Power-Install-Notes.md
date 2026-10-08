

### 🔍 Diagnostic: Why APK Installation Fails on Moto G Power Phones

I installed  DOSwriter on my Moto G Power without problem but recently it was failing to install. Problem ocurred on a second Moto G so I debugged it in Android Studio. DOSwriter installed ok after that. Here are some settings to prevent install errors on Moto G :

Motorola’s Package Installer on Android 10/11/12 enforces strict installation and update policies. When side-loading an APK, Motorola displays a generic `"App not installed"` error for the following reasons:

#### 1. **Existing Signature Conflict (`INSTALL_FAILED_UPDATE_INCOMPATIBLE`)** — *Most Common*
- **Cause**: If an earlier version of DOSwriter was installed via Android Studio, ADB, or a build signed with a different debug keystore, Motorola's `PackageInstaller` blocks side-loading an updated APK over the existing app.
- **Solution**: Uninstall the previous version of DOSwriter from your Moto G Power (**`Settings > Apps > DOSwriter > Uninstall`** or `adb uninstall com.example.doswriter`) before tapping to install the new APK.

#### 2. **"Install Unknown Apps" Permission Disabled on File Manager**
- **Cause**: On Motorola devices, the File Manager app (e.g. *Files by Google* or *Moto Files*) or Web Browser used to tap and open the `.apk` file must be granted explicit permission to install apps.
- **Solution**: On the Moto G Power, go to:
  **`Settings` ➔ `Apps & Notifications` ➔ `Special App Access` ➔ `Install Unknown Apps`**
  Select your File Manager or Chrome app and toggle **`Allow from this source`** to **ON**.

#### 3. **Unsigned Release Builds (`INSTALL_PARSE_FAILED_NO_CERTIFICATES`)**
- **Cause**: Standard Gradle `./gradlew assembleRelease` outputs an *unsigned* APK by default if `signingConfig` is absent. Motorola blocks unsigned APKs immediately.
- **Solution**: We configured `app/build.gradle.kts` to auto-sign both `release` and `debug` targets.

#### 4. **Same Version Code Conflicts**
- **Solution**: We incremented the app version to **`versionCode = 2`** and **`versionName = "1.1"`** in [app/build.gradle.kts](file:///home/abe/code/DOSwriter/app/build.gradle.kts) so Motorola’s installer recognizes the APK as a clean upgrade.

---

### 📱 How to Install the New APK on Moto G Power

1. **Uninstall Existing Build**: On your Moto G Power, go to `Settings > Apps > DOSwriter` and tap **Uninstall**.
2. **Build Fresh APK**: Run `./gradlew assembleDebug` or `./gradlew assembleRelease`.
3. **Location of Installable APK**:
   - `app/build/outputs/apk/debug/DWTEv1.0-*-app-debug.apk`
   - `app/build/outputs/apk/release/DWTEv1.0-*-app-release.apk`
4. Copy the `.apk` file to the Moto G Power Downloads folder and open it using your File Manager (ensuring *"Allow from this source"* is enabled).