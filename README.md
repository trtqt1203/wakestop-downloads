# WakeStop — public downloads

This repository holds public APK/unsigned IPA release assets and non-confidential
device-testing checklists/reports. It does not contain the app's source history,
signing keys, credentials or users' trip data.

## Current physical-device test build

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
