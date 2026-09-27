# Linka Material 1.1.5

Linka Material is a lightweight Android client for the Linka decentralized social platform. Version 1.1.5 brings the LinkaLite client into a clean, classic Material interface while retaining compatibility-oriented layouts and a legacy theme for older Android versions.

Linka Material connects to a Linka-compatible server; it does not include or host the server itself. Choose or change the server address in the app. Social, messaging, federation, and image features depend on the selected server and its supported endpoints.

## What you can do

- **Set up an account:** sign in or register, select a server, and use the app's account integration service.
- **Read and publish:** browse the home feed, create posts, view and comment on posts, and browse federation feeds.
- **Connect with people:** find friends, open direct and global chats, create or join groups, and use group channels and external chats.
- **Manage groups:** update group details, manage channels and members, moderate members, and generate or send supported invitations.
- **Manage your profile:** view profiles and pictures, update account details, and edit your biography.
- **Stay informed:** view inbox and notification messages. The app can request and display notifications; this build does not include a push-notification receiver or background messaging service.

Profile pictures and post images are loaded through the client's image-loading path, including the Linka lightweight image-render endpoint where supported.

## Interface and compatibility

Android 5.0 (API 21) and newer use the native light Material theme, with blue accents, light surfaces, elevated cards, and evenly sized bottom navigation. Android 3.0–4.4 use a light Holo theme, while earlier versions use the platform's light legacy theme. Small-screen devices receive compact dimensions, and the layouts use density-independent sizing.

The app manifest declares minimum SDK 3 and target SDK 9. Those are the configured install/target values; they do not guarantee every feature will work on every Android release or server. The app requests internet access, network-state access, and vibration, and permits cleartext HTTP for compatibility with existing server endpoints. Use a trusted server when sending account credentials.

## Release information

- **Version:** 1.1.5 (version code 3)
- **Application ID:** `com.LinkaMaterialProject.linkaMaterial`
- **Compile SDK:** 34

Linka Material is an independent modified Android client based on the original LinkaLite app. It does not bundle third-party federation services or host user content.

## Credits

Linka Material is derived from **Linka**, created by **Luiz Gustavo**. Please retain upstream notices when redistributing the source or binaries.

- [Original Linka repository](https://github.com/luizgustavo76/Linka)
- [Linka documentation](https://luizgustavo76.github.io/Linka/documentation/docs.html)
- [Upstream LICENSE.txt (Apache License 2.0)](https://github.com/luizgustavo76/Linka/blob/main/LICENSE.txt)
