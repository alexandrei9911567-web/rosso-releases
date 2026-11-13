# Rosso

Release packages for Rosso, a TV app for Android TV, Samsung (Tizen) and LG (webOS).
Every installed Rosso checks this repository's newest release (`latest.json`, signed) and updates
itself.

## Install

Always the newest version:

| TV | File |
|---|---|
| Android TV / Google TV (most TVs, e.g. TCL) | [rosso-android-armeabi-v7a.apk](https://github.com/alexandrei9911567-web/rosso-releases/releases/latest/download/rosso-android-armeabi-v7a.apk) |
| Android TV with a 64-bit system | [rosso-android-arm64-v8a.apk](https://github.com/alexandrei9911567-web/rosso-releases/releases/latest/download/rosso-android-arm64-v8a.apk) |
| Samsung (Tizen) | [rosso-samsung.wgt](https://github.com/alexandrei9911567-web/rosso-releases/releases/latest/download/rosso-samsung.wgt) + [rosso-samsung-engine.tpk](https://github.com/alexandrei9911567-web/rosso-releases/releases/latest/download/rosso-samsung-engine.tpk) |
| LG (webOS) | [rosso-lg.ipk](https://github.com/alexandrei9911567-web/rosso-releases/releases/latest/download/rosso-lg.ipk) |

### Android TV (no PC needed)
1. On the TV, install **Downloader** from the Play Store.
2. *Settings → Apps → Security & restrictions → Unknown sources*: allow **Downloader**.
3. In Downloader, enter the address of the Android file above and install it.
4. Later versions arrive by themselves: when Rosso opens it shows "A new version is available";
   choose **Update** and confirm Android's question.
5. Optional, so that Rosso opens again by itself after updating: *Settings → Apps → Special app access →
   Display over other apps* → allow **Rosso**.

### Samsung
Developer mode on the TV and a PC on the same network: both files are installed with Tizen's `sdb`
(the `.tpk` is Rosso's engine service). Later versions update themselves.

### LG
Developer mode (LG's *Developer Mode* app) and a PC on the same network: `ares-install rosso-lg.ipk`.
Keep developer mode's session extended: when it runs out, LG removes the apps installed this way.

## Updates
Each release carries `latest.json` and its signature. A TV takes an update only when the signature
matches the key built into Rosso, and every file matches its sha256.
