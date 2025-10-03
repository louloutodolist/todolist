# TodoOfflineApp (Android, Offline APK)

This Android Studio project packages your To‑Do HTML into an *offline* Android app.
Everything loads from local `assets/` — no internet required, service worker not needed.

## Build steps (macOS/Windows/Linux)

1. Install **Android Studio** (latest) and open this folder.
2. When prompted, let Android Studio upgrade Gradle/AGP if it wants.
3. In the toolbar, select **Run ▶** to install on a connected device/emulator (USB debugging must be enabled).

## Create a signed APK (for sideloading)

1. **Build > Generate Signed Bundle / APK...**
2. Choose **APK**, click **Next**.
3. Create a new **Key store** (choose a password you’ll remember), fill in fields, **Next**.
4. Select **release** build variant, choose output folder, **Finish**.
5. The APK will be in `app/release/` — copy to your phone and install (enable “Install unknown apps”).

## Update your To‑Do HTML later
- Replace `app/src/main/assets/index.html` with your updated file and rebuild.

## Notes
- `localStorage` is enabled via `domStorageEnabled = true` and persists per app install.
- If your HTML makes external requests (CDNs, APIs), they won’t work offline unless you bundle them locally too.
- Orientation, fullscreen, or status‑bar color tweaks can be added if you want — just ask.
