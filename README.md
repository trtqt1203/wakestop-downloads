# WakeStop

**Lên xe chợp mắt – Khỏe khoắn cả ngày**  
*Nap on the way – Fresh all day*

### [Tải ứng dụng trên website WakeStop →](https://wakestop.pages.dev/#download)

Bản thử nghiệm **1.1.0 (43)**: gợi ý điểm đã lưu không dấu, nhập tọa độ; iOS thêm gợi ý địa điểm Apple. Android vẫn dùng nút Tìm cho tìm kiếm trực tuyến để tuân thủ chính sách Nominatim công cộng. Không bật thanh toán hoặc đổi nhà cung cấp.

| Điện thoại | Tải trực tiếp |
| --- | --- |
| Android 8 trở lên | [APK Release-test · 52,3 MB](https://github.com/trtqt1203/wakestop-downloads/releases/download/search-20261110-build43/WakeStop-1.1.0-build43-release-test.apk) |
| iPhone iOS 26 trở lên | [IPA chưa provision · 10,3 MB](https://github.com/trtqt1203/wakestop-downloads/releases/download/search-20261110-build43/WakeStop-1.1.0-build43-iOS26-unprovisioned.ipa) |
| iPhone iOS 17–18 | [IPA chưa provision · 10,4 MB](https://github.com/trtqt1203/wakestop-downloads/releases/download/search-20261110-build43/WakeStop-1.1.0-build43-iOS17-unprovisioned.ipa) |

[SHA-256](https://github.com/trtqt1203/wakestop-downloads/releases/download/search-20261110-build43/SHA256SUMS.txt) · [Checklist thử trên điện thoại](https://github.com/trtqt1203/wakestop-downloads/releases/download/search-20261110-build43/TEST_BUILD43.md) · [Thông tin bản thử nghiệm](https://github.com/trtqt1203/wakestop-downloads/releases/tag/search-20261110-build43)

**Giới hạn tìm kiếm:** một số khu dân cư miền Trung/miền Nam vẫn không có kết quả phù hợp từ Nominatim. Gợi ý trên máy không bổ sung dữ liệu còn thiếu của dịch vụ. Đọc địa chỉ và xác nhận ghim; app không tự chọn kết quả gần giống.

**Kiểm thử:** Android241unit test đạt, build/lint và Release packaging đạt. iOS native lượt đầy đủ241test:205đạt/35lỗi/1bỏ qua. Lượt kiểm tra search cuối cùng đạt4/4test cùng archive Release và build simulator; không thay thế kết quả đầy đủ đang lỗi. Chưa xác nhận autocomplete, độ trễ hay chuông trên điện thoại thật. Đây chưa phải bản sẵn sàng lên store.

**iPhone:** cả hai IPA cần ký app và extension phù hợp trước khi cài. Không sửa MinimumOSVersion hoặc xóa plug-in để né lỗi. Chưa hỗ trợ iOS16. iOS17/18 dùng âm thông báo ngắn khi khóa máy/ở nền, có thể bị Im lặng/Focus chặn; âm lặp chỉ khi app mở. Không tương đương AlarmKit iOS26. Bản iOS17–18 không bị khóa cài trên iOS mới; đó là nhóm máy khuyên dùng.

**Android:** giữ chữ ký cũ cho Release thử nghiệm. Nếu cài đè báo lỗi chữ ký, không gỡ app hay xóa dữ liệu để né lỗi. Hãy cấp quyền và thử chuông khi app mở/khóa máy trước khi dùng; không dựa duy nhất vào WakeStop để xuống xe.

[Chính sách quyền riêng tư](https://wakestop.pages.dev/privacy/) · [Privacy policy](https://wakestop.pages.dev/privacy/en/). Xóa bản sao cloud/đăng xuất chưa phải xóa tài khoản Firebase; luồng tự xóa tài khoản đầy đủ và khai báo store vẫn còn cần hoàn tất.

**English:** Build43 is a free search trial: saved-place suggestions and coordinate input on both platforms, Apple completions on iOS, explicit online Search on Android. Missing neighborhood coverage remains unresolved for the retained Android provider. The final focused native search check passed4tests; the full iOS suite still has35failed cases. Both IPAs require signing; iOS17/18 background sound is limited. Test on your phone before relying on alerts.

Kho chỉ cung cấp file tải công khai; mã nguồn ứng dụng, khóa ký và dữ liệu người dùng không được công khai ở đây.

© 2026 **TRavisTRTQT**. Bảo lưu mọi quyền / All rights reserved.
