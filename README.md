# WakeStop — Tải ứng dụng

**Lên xe chợp mắt – Khỏe khoắn cả ngày**

*Nap on the way – Fresh all day*

Repo này cung cấp APK, IPA và các báo cáo/checklist không mật, tải được không cần
đăng nhập. Mã nguồn ứng dụng được giữ riêng tư; không công bố khóa ký, thông tin
đăng nhập hoặc dữ liệu chuyến đi của người dùng.

## Bản mới nhất — 1.1.0 (39), ngày 24/10/2026

Chuẩn bị cho đợt phát hành ngày **25/10/2026**. Đây vẫn là **Release thử nghiệm**,
chưa phải phê duyệt phát hành production. Việc chuẩn hóa tên file không thay đổi
nội dung, chữ ký hoặc trạng thái kiểm chứng của build 39.

| Nền tảng | Tải trực tiếp | Dung lượng | Lưu ý |
|---|---|---|---|
| Android | [WakeStop-1.1.0-build39-Android.apk](https://github.com/trtqt1203/wakestop-downloads/releases/download/ui-fixes-20261024-build39/WakeStop-1.1.0-build39-Android.apk) | 52.285.971 bytes (~52,3 MB) | Android 8 trở lên; Release tối ưu R8, tắt debug; giữ chữ ký thử nghiệm cũ |
| iOS | [WakeStop-1.1.0-build39-iOS-unprovisioned.ipa](https://github.com/trtqt1203/wakestop-downloads/releases/download/ui-fixes-20261024-build39/WakeStop-1.1.0-build39-iOS-unprovisioned.ipa) | 9.829.198 bytes (~9,8 MB) | iOS 26 trở lên; **cần ký lại app và phần mở rộng trước khi cài** |

IPA được build bằng xtool ở cấu hình Release, có chữ ký ad-hoc cục bộ nhưng chưa
có provisioning profile/chữ ký phân phối Apple. Link công khai không làm IPA tự
cài được. Không yêu cầu gỡ app/xóa dữ liệu để né lỗi chữ ký khi cập nhật.

- [Trang tải đầy đủ build 39](https://github.com/trtqt1203/wakestop-downloads/releases/tag/ui-fixes-20261024-build39)
- [Báo cáo thay đổi và kết quả kiểm tra build 39](https://github.com/trtqt1203/wakestop-downloads/releases/download/ui-fixes-20261024-build39/UI_LAYOUT_BUILD39.md)
- [Checklist kiểm tra trên điện thoại](https://github.com/trtqt1203/wakestop-downloads/releases/download/ui-fixes-20261024-build39/PHYSICAL_TEST_CHECKLIST.md)
- [SHA-256 của hai file mang tên mới](https://github.com/trtqt1203/wakestop-downloads/releases/download/ui-fixes-20261024-build39/WakeStop-1.1.0-build39-SHA256SUMS.txt)

Đã tải toàn bộ hai file từ link công khai không đăng nhập và đối chiếu đúng bytes,
SHA-256. Android: **227/227 unit test**, Debug/Release build và lint đạt. iOS:
**19/19 test portable trên Linux** và xtool Release build đạt; **không phải native
XCTest/UI trên iPhone**. Lượt macOS CI trước bị Actions budget chặn trước runner.
Các kết quả này không thay thế kiểm tra đầy đủ trên máy thật hoặc chứng nhận bảo mật.

Build 39 sửa thẻ chuyến yêu thích bị cắt, bố cục nút tính giờ lên đường, gộp
cài đặt vào **Tùy chỉnh**, và mặc định Tiếng Việt khi cài mới trên cả hai nền tảng.
Các link tên cũ của build 39 vẫn được giữ để không làm hỏng lượt tải trước.

## Lịch sử — Android 1.1.0 (9), ngày 12/10/2026 — không phải bản mới nhất

Các mục dưới đây là hồ sơ cũ; hãy dùng link **build 39 ở trên** để tải bản mới.

- [Android debug APK (9)](https://github.com/trtqt1203/wakestop-downloads/releases/download/android-native-map-20261012-build9/WakeStop-debug.apk)
- [Current report (REPORT.md)](https://github.com/trtqt1203/wakestop-downloads/releases/download/android-native-map-20261012-build9/REPORT.md)
- [Physical checklist](https://github.com/trtqt1203/wakestop-downloads/releases/download/android-native-map-20261012-build9/PHYSICAL_TEST_CHECKLIST.md)
- [Actual Set Trip street raster](https://github.com/trtqt1203/wakestop-downloads/releases/download/android-native-map-20261012-build9/set-trip-real-map.png)
- [Home showing build9](https://github.com/trtqt1203/wakestop-downloads/releases/download/android-native-map-20261012-build9/home-build9.png)
- [Checksums](https://github.com/trtqt1203/wakestop-downloads/releases/download/android-native-map-20261012-build9/SHA256SUMS)

APK8's DoH diagnostic passed, but the real osmdroid loader called a 5-argument
overload while our adapter overrode only 3 arguments. APK9 fixes the actual
dispatch and puts Retry above overlapping controls. RED native regression
failed with transport calls0; GREEN selected native suite10 passed. Local
unit70/build/lint pass; real street raster visible after a cache-empty start,
not a mock or owner-phone acceptance. APK **21,324,848 bytes**,
SHA-256 `45a5dff4388fa2108b3a8d89931135af5b31890c70b1301ffc9d8a7b9e184613`,
same APK8 signer; anonymous HTTP200/bytes/checksums verified. Install as update.

Still OSM/system-first Google HTTPS DNS, no new provider/global DNS change,
disabled TLS or fixed OSM CDN IP. iOS remains6: MapKit has no such overload and
its error/Retry already overlays controls, no new IPA/macOS gate claimed.
GitHub CI could not allocate runners (both jobs0 steps), not an app-gate pass.
Source private, this delivery repo public. Original phone test remains pending.

## Previous Android DNS diagnostic — 1.1.0 (8), native integration superseded

- [Android debug APK (8)](https://github.com/trtqt1203/wakestop-downloads/releases/download/android-map-dns-20261012-build8/WakeStop-debug.apk)
- [Current report (REPORT.md)](https://github.com/trtqt1203/wakestop-downloads/releases/download/android-map-dns-20261012-build8/REPORT.md)
- [Physical checklist](https://github.com/trtqt1203/wakestop-downloads/releases/download/android-map-dns-20261012-build8/PHYSICAL_TEST_CHECKLIST.md)
- [Actual Set Trip screenshot](https://github.com/trtqt1203/wakestop-downloads/releases/download/android-map-dns-20261012-build8/set-trip-real-map.png)
- [Map connection disclosure](https://github.com/trtqt1203/wakestop-downloads/releases/download/android-map-dns-20261012-build8/map-connection-disclosure.png)
- [Checksums](https://github.com/trtqt1203/wakestop-downloads/releases/download/android-map-dns-20261012-build8/SHA256SUMS)

System DNS first, automatic Google DNS-over-HTTPS fallback for OSM raster only.
No phone DNS change, VPN, paid map service or API key. Google sees hostname and
connection IP, not trip coordinates in the DNS query. Search/bus/routing keep
their existing resolvers; still requires internet. APK **21,656,412 bytes**,
SHA-256 `4a5430d76f93a872ba49f99cc924737b97de5f127069847234cf5fb36c2c4a56`,
same APK7 signer; anonymous HTTP200/bytes/checksums verified.

Local Android gates passed (70 unit tests, build/lint); actual API34 native/live
checks OK (8 tests). Default emulator DNS failed yet production client fetched
valid PNG200. Actual street raster/disclosure screenshots, not owner-phone
acceptance. GitHub CI could not allocate runners (zero executed steps), not a
CI pass. iOS remains (6), unchanged: MapKit owns its base-map transport, no new
IPA/macOS check claimed; existing UI failures remain open. Source stays private.

## Previous Android map follow-up — Android 1.1.0 (7), 12 October 2026

- [Android debug APK (7)](https://github.com/trtqt1203/wakestop-downloads/releases/download/android-map-retry-20261012-build7/WakeStop-debug.apk)
- [Current report (REPORT.md)](https://github.com/trtqt1203/wakestop-downloads/releases/download/android-map-retry-20261012-build7/REPORT.md)
- [Physical checklist](https://github.com/trtqt1203/wakestop-downloads/releases/download/android-map-retry-20261012-build7/PHYSICAL_TEST_CHECKLIST.md)
- [Actual Set Trip screenshot](https://github.com/trtqt1203/wakestop-downloads/releases/download/android-map-retry-20261012-build7/set-trip-real-map.png)
- [Checksums](https://github.com/trtqt1203/wakestop-downloads/releases/download/android-map-retry-20261012-build7/SHA256SUMS)

Retry resets failed-URL backoff while preserving cache/camera/overlays; DNS and
HTTPS failures have distinct reasons. Android unit/build/lint passed (60 unit
tests), 6 actual native checks passed on API34. Real street raster is visible
with working emulator DNS; not a mock or owner-phone acceptance. APK 20,602,386
bytes, same debug signer as APK6, anonymous HTTP200/bytes/checksum verified.
The APK does not silently override the phone's DNS or map provider.

iOS remains (6), unchanged: MapKit has no osmdroid state to reset, so no new
IPA/macOS pass is claimed. Its existing download and known UI limitations are
in the prior dual-platform release below. App source remains private.

## Previous dual-platform bus/map build — 1.1.0 (6), 12 October 2026

- [Android debug APK (6)](https://github.com/trtqt1203/wakestop-downloads/releases/download/bus-map-20261012-build6/WakeStop-debug.apk)
- [iOS unsigned device IPA (6)](https://github.com/trtqt1203/wakestop-downloads/releases/download/bus-map-20261012-build6/WakeStop-unsigned.ipa)
- [Current-task report](https://github.com/trtqt1203/wakestop-downloads/releases/download/bus-map-20261012-build6/ALARM_LIST_REPORT.md)
- [Physical-device checklist](https://github.com/trtqt1203/wakestop-downloads/releases/download/bus-map-20261012-build6/PHYSICAL_TEST_CHECKLIST.md)
- [Bus places/policy](https://github.com/trtqt1203/wakestop-downloads/releases/download/bus-map-20261012-build6/BUS_STOPS.md)
- [SHA-256 checksums](https://github.com/trtqt1203/wakestop-downloads/releases/download/bus-map-20261012-build6/SHA256SUMS)

Both platforms: bus error reasons, Retry/backoff/Retry-After and retained expired
cache. Android: missing-tile diagnostics/recovery; the owner's phone-specific
cause is still unconfirmed. Separately reproduced iOS small-map camera insets
corrected. Consumption copy removed, background-reliability/OEM guidance kept.

Android unit/build/lint passed (57 unit results). iOS final-source archive and
unit/UI compilation passed; corrected and final-source simulator unit runs
passed all 54 tests. **UI gate did not pass:** three cases failed (keyboard/layout,
camera-test signal, toggle/marker); batch stopped after repeated post-test
finalization hangs, sixteen UI cases unrun. No timeout padding/retries and no
new physical-device or screenshot pass. Details/remaining work are in the report.

Both binaries downloaded anonymously (HTTP 200), checksums and bytes matched.
APK 20,601,070 bytes; IPA 485,657 bytes, Payload/WakeStop.app, iPhoneOS arm64,
version 1.1.0 (6), **unsigned; owner signing required before installation**.
App source remains private; no credentials/private raw logs are published.
Use the checklist on both devices. Do not use a test build as the sole alarm.

## Previous map/route test build — 1.1.0 (5), 11 October 2026

- [Android debug APK (5)](https://github.com/trtqt1203/wakestop-downloads/releases/download/map-route-20261011-build5-c4a6448/WakeStop-debug.apk)
- [iOS unsigned device IPA (5)](https://github.com/trtqt1203/wakestop-downloads/releases/download/map-route-20261011-build5-c4a6448/WakeStop-unsigned.ipa)
- [Build/test report](https://github.com/trtqt1203/wakestop-downloads/releases/download/map-route-20261011-build5-c4a6448/ALARM_LIST_REPORT.md)
- [Physical-device checklist](https://github.com/trtqt1203/wakestop-downloads/releases/download/map-route-20261011-build5-c4a6448/PHYSICAL_TEST_CHECKLIST.md)
- [Bus places/policy](https://github.com/trtqt1203/wakestop-downloads/releases/download/map-route-20261011-build5-c4a6448/BUS_STOPS.md)
- [SHA-256 checksums](https://github.com/trtqt1203/wakestop-downloads/releases/download/map-route-20261011-build5-c4a6448/SHA256SUMS)

Tiered/forced Road+Bus places, picker gesture/camera ownership and center pin,
retained road previews with explicit errors/Retry, and keyboard/sheet layout.
Android gates passed (51 unit results; native UI tests compiled only). iOS
device archive and native unit/UI bundle compilation passed on Xcode 26.
**No current-source iOS test execution pass**: the full gate remained queued
without a machine and was cancelled. No new app screenshots are claimed.

Both packages were downloaded anonymously (HTTP 200), bytes/checksums compared.
The final IPA is 474,417 bytes, Payload/WakeStop.app, iPhoneOS arm64, 1.1.0 (5),
**unsigned; owner signing required**. The source-suffixed release above includes
the final iOS same-target retry cleanup correction; the early unsuffixed
build-5 release is superseded, retained for recoverability.

Physical map/keyboard/bus/route behavior and Android's reported blank map still
need owner verification. Tracking's active target remains read-only pending a
separate live-target-editing decision. Road+Bus is an estimated car route, not
a real bus line; shared Overpass is not production infrastructure. The earlier
solitary iPhone alarm-silence report is not confirmed fixed by this update.
App source remains private; no secrets or raw private logs are published here.

## Previous bus places prototype — 1.1.0 (4), 11 October 2026

- [Android debug APK (4)](https://github.com/trtqt1203/wakestop-downloads/releases/download/bus-places-20261011-build4/WakeStop-debug.apk)
- [iOS unsigned device IPA (4)](https://github.com/trtqt1203/wakestop-downloads/releases/download/bus-places-20261011-build4/WakeStop-unsigned.ipa)
- [Build/test report](https://github.com/trtqt1203/wakestop-downloads/releases/download/bus-places-20261011-build4/ALARM_LIST_REPORT.md)
- [Physical-device checklist](https://github.com/trtqt1203/wakestop-downloads/releases/download/bus-places-20261011-build4/PHYSICAL_TEST_CHECKLIST.md)
- [Bus places/policy](https://github.com/trtqt1203/wakestop-downloads/releases/download/bus-places-20261011-build4/BUS_STOPS.md)
- [Bus-line investigation (no routing implementation)](https://github.com/trtqt1203/wakestop-downloads/releases/download/bus-places-20261011-build4/BUS_LINES_INVESTIGATION.md)
- [SHA-256 checksums](https://github.com/trtqt1203/wakestop-downloads/releases/download/bus-places-20261011-build4/SHA256SUMS)

Android unit/build/lint passed (47 unit results; native UI tests compiled only).
iOS device archive passed; actual IPA metadata 1.1.0 (4), iPhoneOS arm64,
Payload/WakeStop.app, ZIP CRC and unsigned status verified. Anonymous download:
HTTP 200, 445,243 bytes, checksum/bytes match. **The owner must sign before install.**

The separate iOS simulator gate **FAILED**: 44 unit cases (42 pass / 2 stale
fixture failures; all six bus tests passed), 17 UI cases (15 assertion passes /
2 failing cases), only 14 UI bundles fully finalized. Bus-layer activation,
marker selection and keyboard checks remain unresolved; archive availability
is not app acceptance. No blind timeout increase or simulator retry.

Owner-only two-device prototype: public Overpass is not production infrastructure;
four uncached requests/installation/day and 24-hour cache. Wider distribution
requires owned Overpass or bundled data. Xe buýt enables the places layer only;
Road mode is still an estimated car route, not an actual bus line. Real-device
journeys/audio remain unverified, including the reported 1–2-second silence.
Application source stays private; no credentials/raw confidential logs are published.


## Previous Home/map verification — 1.1.0 (3), 10 October 2026

- [Android debug APK (3)](https://github.com/trtqt1203/wakestop-downloads/releases/download/home-maps-20261010-build3/WakeStop-debug.apk)
- [iOS unsigned device IPA (3)](https://github.com/trtqt1203/wakestop-downloads/releases/download/home-maps-20261010-build3/WakeStop-unsigned.ipa)
- [Build/test report](https://github.com/trtqt1203/wakestop-downloads/releases/download/home-maps-20261010-build3/ALARM_LIST_REPORT.md)
- [Physical-device checklist](https://github.com/trtqt1203/wakestop-downloads/releases/download/home-maps-20261010-build3/PHYSICAL_TEST_CHECKLIST.md)
- [SHA-256 checksums](https://github.com/trtqt1203/wakestop-downloads/releases/download/home-maps-20261010-build3/SHA256SUMS)

Corner-only help, one new-trip alarm (explicit Add up to ten), user-centered
follow camera and main maps with persistent settings/details sheets. Android
unit/build/lint passed: **40 unit tests**, native UI tests **compiled only**.
APK downloaded anonymously: HTTP 200, 20,519,190 bytes, checksum/bytes match.

**Fresh iOS IPA (3) exported on 11 October 2026.** The Codemagic device archive
passed after a Swift compiler-only camera-signature fix (source `05e1d2c`).
IPA ZIP CRC, Payload/WakeStop.app, arm64/iPhoneOS, version 1.1.0 (3) and unsigned
state verified. Anonymous download: HTTP 200, 389,638 bytes, checksum/bytes match.
The owner must sign the IPA before installing. Final-source iOS unit/UI gates
and physical-device acceptance remain unverified; no new app screenshot is
claimed. GitHub's account-level CI job-start blocker remains. See the checklist.
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
