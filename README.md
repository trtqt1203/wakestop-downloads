# WakeStop — public downloads

This repository holds public APK/unsigned IPA release assets and non-confidential
device-testing checklists/reports. It does not contain the app's source history,
signing keys, credentials or users' trip data.

## Current Set Trip fixes — 8 October 2026

- [Android debug APK](https://github.com/trtqt1203/wakestop-downloads/releases/download/set-trip-fixes-20261008-953e82b/WakeStop-debug.apk)
- [iOS unsigned device IPA](https://github.com/trtqt1203/wakestop-downloads/releases/download/set-trip-fixes-20261008-953e82b/WakeStop-unsigned.ipa)
- [Physical-device checklist](https://github.com/trtqt1203/wakestop-downloads/releases/download/set-trip-fixes-20261008-953e82b/PHYSICAL_TEST_CHECKLIST.md)
- [Build/test report](https://github.com/trtqt1203/wakestop-downloads/releases/download/set-trip-fixes-20261008-953e82b/ALARM_LIST_REPORT.md)
- [SHA-256 checksums and actual iOS screenshots](https://github.com/trtqt1203/wakestop-downloads/releases/tag/set-trip-fixes-20261008-953e82b)

Done/outside-tap keyboard dismissal, Road pre-Start preview/ETA/red on-route
points (no Road circles), and single-editor accordion. Android build/unit/lint
passed; iOS device archive succeeded. The whole iOS simulator gate FAILED during
two post-test finalizations despite 21 unit + 11 UI tests reporting passed
assertions. Both build downloads and attached documents/images were downloaded
anonymously and compared byte-for-byte with their originals. Real-phone acceptance
is pending; source is private and no raw diagnostic logs are published.

## Previous physical-device test build (before these fixes)

- [Android debug APK](https://github.com/trtqt1203/wakestop-downloads/releases/download/physical-check-20261008-09a0ff6/WakeStop-debug.apk)
- [iOS unsigned device IPA](https://github.com/trtqt1203/wakestop-downloads/releases/download/physical-check-20261008-09a0ff6/WakeStop-unsigned.ipa)
- [Physical-device checklist](https://github.com/trtqt1203/wakestop-downloads/releases/download/physical-check-20261008-09a0ff6/PHYSICAL_TEST_CHECKLIST.md)
- [Verification report](https://github.com/trtqt1203/wakestop-downloads/releases/download/physical-check-20261008-09a0ff6/PHYSICAL_VERIFICATION_REPORT.md)
- [SHA-256 checksums](https://github.com/trtqt1203/wakestop-downloads/releases/download/physical-check-20261008-09a0ff6/SHA256SUMS)

Android requires API 26+ and Google Play Services. The iOS package is a device
arm64 build requiring iOS 26+, **unsigned**: the owner must sign/resign it before
installation. Keep the existing application ID/signature/container when checking
an upgrade's old-trip data; do not uninstall/clear data to bypass a mismatch.

These are test builds, not a claim of verified real GPS, background audio or
journey reliability. Physical-device verification remains pending the owner's
iPhone and Android results. See each release's report for actual build/test
results; simulator assertion passes are not physical visual confirmation.
