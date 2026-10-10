# t3code-apk-builder

Builds an unofficial standalone Android APK from the latest
[T3 Code nightly release](https://github.com/pingdotgg/t3code/releases)
every day at **01:23 UTC**, or manually through Actions. Existing builds are skipped.
GitHub schedules can be delayed and are disabled after 60 days without repository activity.

Download `t3code.apk` from [Releases](https://github.com/abcamiletto/t3code-apk-builder/releases),
or add this repository to [Obtainium](https://github.com/ImranR98/Obtainium).
Enable background updates and Shizuku for unattended installation;
non-root Shizuku needs restarting after phone reboots.

The APK supports ARM phones, bundles its JavaScript, and disables upstream OTA updates.
It uses `com.abcamiletto.t3code.nightly`, so it installs alongside the official app.
Upstream public cloud configuration comes from `.env.example`.
Google sign-in and Firebase push may require separate credentials for this package/signature.

Signing uses the repository secrets `KEYSTORE_BASE64` (base64-encoded PKCS#12 keystore)
and `KEYSTORE_PASSWORD`. Keep the same key for all updates and back it up securely.
Forks must supply their own secrets. No Expo account is required.

This repository builds and publishes APKs; installation runs on your phone.
