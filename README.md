# Linka Material

Linka Material is a lightweight Android client based on the original LinkaLite app. It keeps Linka's federated social features and gives the Android interface a clean, classic Material look.

## Credits and project relationship

This app is derived from **Linka**, created by **Luiz Gustavo**. The upstream repository contains the original platform and LinkaLite Android client:

- [Linka source repository](https://github.com/luizgustavo76/Linka)
- [Linka documentation](https://luizgustavo76.github.io/Linka/documentation/docs.html)
- [Upstream license](https://github.com/luizgustavo76/Linka/blob/main/LICENSE.txt) — the upstream repository declares Apache License 2.0.

Linka Material is a modified client build; it is not a separate server or a replacement for the Linka project. Please retain upstream notices when redistributing source or builds.

## App overview

The Android client includes account sign-in and registration, a post feed, federation browsing, direct and group chats, channels, profiles, friend and inbox screens, and invite tools. The app connects to a Linka-compatible server; server settings can be changed in the app.

The interface uses Android's light Material theme on Android 5.0 (API 21) and newer, with a light legacy theme on earlier versions. Layouts use Android density-independent sizing and provide compact dimensions for small screens.

| Setting | Value |
| --- | --- |
| App label | Linka Material |
| Application ID | `com.LinkaMaterialProject.linkaMaterial` |
| Version | `1.1.5` (`versionCode` 3) |
| Minimum SDK | API 3 |
| Target SDK | API 9 |
| Compile SDK | API 34 |
| Java source/target | Java 17 |

The manifest requests network access, network state, and vibration. It allows cleartext traffic for compatibility with existing HTTP server endpoints.

## Build without Android Studio

Install a JDK 21 runtime, Android SDK command-line tools, and accept the Android SDK licenses. The Gradle wrapper downloads Gradle 9.3.1; the project is configured to use a Java 21 Gradle daemon and Java 17 source compatibility. Install Android SDK Platform 34 if Gradle does not install it automatically.

From the project directory, run:

**Windows PowerShell:**

```powershell
.\gradlew.bat --no-daemon :app:assembleDebug
```

**macOS or Linux:**

```sh
./gradlew --no-daemon :app:assembleDebug
```

The debug APK is written to:

```text
app/build/outputs/apk/debug/app-debug.apk
```

To install it on a connected device with Android Debug Bridge:

```sh
adb install -r app/build/outputs/apk/debug/app-debug.apk
```

The debug APK is signed with a development key and is intended for testing. Configure a private release key before producing a release build; do not publish keystores or signing credentials.
