# WakeStop — public downloads

This repository holds public APK/unsigned IPA release assets and non-confidential
device-testing checklists/reports. It does not contain the app's source history,
signing keys, credentials or users' trip data.

## Latest Home/map verification — 1.1.0 (3), 10 October 2026

- [Android debug APK (3)](https://github.com/trtqt1203/wakestop-downloads/releases/download/home-maps-20261010-build3/WakeStop-debug.apk)
- [Build/test report](https://github.com/trtqt1203/wakestop-downloads/releases/download/home-maps-20261010-build3/ALARM_LIST_REPORT.md)
- [Physical-device checklist](https://github.com/trtqt1203/wakestop-downloads/releases/download/home-maps-20261010-build3/PHYSICAL_TEST_CHECKLIST.md)
- [SHA-256 checksums](https://github.com/trtqt1203/wakestop-downloads/releases/download/home-maps-20261010-build3/SHA256SUMS)

Corner-only help, one new-trip alarm (explicit Add up to ten), user-centered
follow camera and main maps with persistent settings/details sheets. Android
unit/build/lint passed: **40 unit tests**, native UI tests **compiled only**.
APK downloaded anonymously: HTTP 200, 20,519,190 bytes, checksum/bytes match.

**No fresh iOS IPA is available for this update yet.** Equivalent iOS source
and version (3) are committed, but macOS verification/export is blocked by
the disconnected Codemagic browser/unavailable API token and GitHub billing
rejection. The previous IPA (2) below does not contain these changes. No new
visual screenshot or physical-device acceptance is claimed; see the checklist.
Application source repository stays private; no secrets/raw logs are uploaded.

## Previous sequential stop alarms — 10 October 2026

Version **1.1.0 (2)** on both platforms: up to five ordered stops plus the
destination, 1–10 named thresholds for the current target, persisted progress
and per-target dedup. Radius and Road modes are both supported. Advancing a stop
does not cancel its sounding alarm.

- [Android debug APK](https://github.com/trtqt1203/wakestop-downloads/releases/download/stops-20261010-376f517/WakeStop-debug.apk)
- [iOS unsigned device IPA](https://github.com/trtqt1203/wakestop-downloads/releases/download/stops-20261010-376f517/WakeStop-unsigned.ipa)
- [Build/test report](https://github.com/trtqt1203/wakestop-downloads/releases/download/stops-20261010-376f517/ALARM_LIST_REPORT.md)
- [Physical two-stop checklist](https://github.com/trtqt1203/wakestop-downloads/releases/download/stops-20261010-376f517/PHYSICAL_TEST_CHECKLIST.md)
- [SHA-256 checksums](https://github.com/trtqt1203/wakestop-downloads/releases/download/stops-20261010-376f517/SHA256SUMS)
- [Final release](https://github.com/trtqt1203/wakestop-downloads/releases/tag/stops-20261010-376f517)

Android build/lint and **34 unit tests passed**. Real macOS iOS archive and
**32 unit tests passed**. Eleven UI cases reported passing assertions, but the
whole simulator gate **FAILED** during two pre-existing post-test result-bundle
finalization hangs. No blind timeout increase/retry. Both final build files were
downloaded anonymously (HTTP 200), checked byte-for-byte and verified against
SHA256SUMS. The IPA is **unsigned** and must be signed by the owner before install.

**Physical acceptance is pending**: test the checklist on your own devices.
Simulation does not verify GPS/audio/reboot/real journeys, and the previously
reported solitary iPhone 1–2-second alarm silence is **not proven fixed**.
The APK-only intermediate release `stops-20261010-ded77b5` is superseded.

## Previous alarm-session fixes — 8 October 2026

- [Android debug APK](https://github.com/trtqt1203/wakestop-downloads/releases/download/alarm-reliability-20261008-44056f9/WakeStop-debug.apk)
- [iOS unsigned device IPA](https://github.com/trtqt1203/wakestop-downloads/releases/download/alarm-reliability-20261008-44056f9/WakeStop-unsigned.ipa)
- [Build/test report](https://github.com/trtqt1203/wakestop-downloads/releases/download/alarm-reliability-20261008-44056f9/ALARM_LIST_REPORT.md)
- [Physical-device checklist](https://github.com/trtqt1203/wakestop-downloads/releases/download/alarm-reliability-20261008-44056f9/PHYSICAL_TEST_CHECKLIST.md)
- [Checksums and handoff documents](https://github.com/trtqt1203/wakestop-downloads/releases/tag/alarm-reliability-20261008-44056f9)

Swipe-to-dismiss on both platforms; fixed top-right **?** tutorial access;
iOS alarm-session admission no longer cancels an undismissed threshold;
Android playback is retained across same-trip intents/configuration recreation.
Android's 24 unit tests/build/lint and iOS device archive passed. iOS's 24 unit
and 11 UI tests reported passing assertions (including swipe and help), but the
whole simulator gate **FAILED** due to two existing post-test finalization hangs.
Physical-phone
acceptance is pending: the reported solitary iPhone 1–2-second silence is **not
confirmed fixed**. Both actual build downloads returned anonymous HTTP 200
and matched their original SHA-256 checksums and bytes.

## Previous Set Trip fixes — 8 October 2026

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
