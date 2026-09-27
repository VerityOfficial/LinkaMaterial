# Linka Material 1.1.5

Linka Material is a lightweight Android client derived from the LinkaLite Android app in the Linka project. Version 1.1.5 presents Linka's social and messaging features in a clean, light Material interface while retaining a legacy theme path for older Android versions.

## Release overview

The standalone, copy-ready description for version 1.1.5 is in [RELEASE_OVERVIEW.md](RELEASE_OVERVIEW.md).

## Interface and device compatibility

- Android 5.0 (API 21) and newer use the native light Material system theme, blue app bar/accent, light surfaces, and elevated list cards.
- Android API 11–20 use the light Holo theme; earlier versions use Android's light legacy theme.
- Bottom navigation uses four equal-width touch areas with a shared icon viewport and consistent bar height.
- Android selects compact dimensions for small-screen devices; other layouts use density-independent dimensions and flexible widths.
- The manifest declares `minSdk 3`, `targetSdk 9`, and support for small through extra-large screens. These are the project's configured SDK values, not a guarantee that every feature works on every Android release or server.

## Release details

| Setting | Value |
| --- | --- |
| App label | Linka Material |
| Version name | 1.1.5 |
| Version code | 3 |
| Application ID | `com.LinkaMaterialProject.linkaMaterial` |
| Compile SDK | 34 |
| Java source and target | 17 |
| Build system | Gradle wrapper 9.3.1; Android Gradle Plugin 9.1.1 |

The manifest requests internet access, network-state access, and vibration. It permits cleartext traffic to preserve compatibility with HTTP server endpoints. Use a trusted server when transmitting account credentials.

## Build without Android Studio

Install a JDK 21 runtime, Android SDK command-line tools, and accept the Android SDK licenses. The Gradle wrapper downloads Gradle 9.3.1, and the project is configured to use a Java 21 Gradle daemon with Java 17 source compatibility. Install Android SDK Platform 34 if Gradle does not install it automatically.

Run the build from this project directory:

**Windows PowerShell**

```powershell
.\gradlew.bat --no-daemon :app:assembleDebug
```

**macOS or Linux**

```sh
./gradlew --no-daemon :app:assembleDebug
```

The debug APK is created at `app/build/outputs/apk/debug/app-debug.apk`. Install it on a connected device with:

```sh
adb install -r app/build/outputs/apk/debug/app-debug.apk
```

The debug APK is signed with a development key and is for testing. A public release build needs a release key controlled by the distributor; keep keystores and signing credentials private.

## Credits and license

This app is derived from **Linka**, created by **Luiz Gustavo**. Credit and source links:

- [Original Linka repository](https://github.com/luizgustavo76/Linka)
- [Original Linka documentation](https://luizgustavo76.github.io/Linka/documentation/docs.html)
- [Upstream LICENSE.txt](https://github.com/luizgustavo76/Linka/blob/main/LICENSE.txt) — the upstream repository declares Apache License 2.0.

Linka Material is a modified Android client build, not a separate Linka server or an official replacement for the upstream project. Preserve the upstream license and notices when redistributing the source or binaries.


Source archive note: the original release-signing key and credentials are intentionally excluded. Build an installable debug APK with `.\gradlew.bat :app:assembleDebug`; configure your own private release signing key to create a release build.
