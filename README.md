# Free TV Player (Android TV / Android 9+)

A starter Android TV IPTV player that loads M3U/M3U8 playlists and plays streams using AndroidX Media3 ExoPlayer. It starts with a public India playlist from the iptv-org project, and you can replace it with your own playlist URL.

## Features
- Android TV remote-friendly channel list and landscape playback layout
- M3U/M3U8 playlist URL loading
- Built-in default playlist URL (public directory; channel availability may vary)
- HLS/M3U8 playback via Media3 HLS module; MP4 and other formats depend on stream/device support
- HTTP and HTTPS stream URLs are permitted (HTTP streams are unencrypted)
- Minimum Android version: Android 9 (API 28)

## Build APK with Android Studio
1. Install Android Studio and its Android SDK Platform 35, plus a compatible JDK (Android Studio's bundled JDK is fine).
2. Extract this folder and open **FreeTVPlayer** in Android Studio.
3. Allow Gradle sync to finish. If prompted, install missing SDK components.
4. Select **Build → Build Bundle(s) / APK(s) → Build APK(s)**.
5. The debug APK will be under `app/build/outputs/apk/debug/app-debug.apk`.
6. Install it on your Android TV (enable installation from your chosen file-transfer method if required).

## Use
- On launch, the app tries to load `https://iptv-org.github.io/iptv/countries/in.m3u`.
- To use your own playlist, focus the URL field, enter an HTTP(S) M3U/M3U8 URL, then select **Load playlist**.
- Select a channel in the left list to start playback. Use the remote's D-pad and OK/Select.

## Important
- This is a player, not a subscription or channel provider. Use streams you own or are authorized to watch. Public playlists can include unavailable, region-restricted, or changed streams; a stream may stop working at any time.
- This starter supports remote playlist URLs. It does not yet include local-file picker, favorites, EPG, or channel logos.
- For Android 9 compatibility, streams must use formats/codecs supported by the device and must have valid TLS/network access.
