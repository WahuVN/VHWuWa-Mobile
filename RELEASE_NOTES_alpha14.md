## VHWuWa Mobile 0.2.0-alpha.14 — Content 3.7.0-R5

Bản này sửa lỗi **mất text / text trống trên Android** xuất hiện ở alpha.13 / R4.

### Nguyên nhân
- R4 đã nhúng nhầm payload PC (~67 MB) thay cho payload Android full-base (~110 MB).
- Vì vậy gói Android bị thiếu dữ liệu mobile-specific dù PAK vẫn mount được.
- Fresh-unpack xác nhận R4 thiếu hẳn:
  - `Client/Content/Aki/ConfigDB/db_TotalTopUp.db`
  - `Client/Content/Aki/ConfigDB/zh-Hans/lang_multi_text.db`
- `en/lang_multi_text.db` của R4 cũng mất **112 key mobile-only** so với baseline Android.

### Đã sửa trong R5
- Dùng chiến lược union: giữ nguyên toàn bộ row/key R4 hiện tại, bổ sung lại phần chỉ có trên Android.
- Khôi phục đủ **112 key mobile-only**.
- Khôi phục đủ **2 DB Android-only**.
- Không rollback các text/bản dịch mới đã có trong R4.
- Áp dụng cùng logic cho cả **Tên Anh** và **Hán Việt**.
- Giữ hash R4 trong legacy baseline để có thể cài đè/nâng cấp trực tiếp.

### Kiểm tra
- Fresh-unpack EN + Hán Việt: PASS.
- Mỗi PAK R5: **114 file**; R4: 112 file.
- SQLite `quick_check`: PASS.
- Core test + Installer test: PASS.
- Android `assembleDebug`: PASS.
- APK readback: payload trong APK khớp đúng hash R5.
- Chưa smoke-test hình ảnh cuối trong game trên thiết bị thật cho alpha.14.

### Hash
- APK SHA256: `3d050ff5de190819787d7a4adc70eaee2369b460cf4d06e2979251a7fde86570`
- PAK Tên Anh: `52e9a717d9edbdb7c8b0558950b16ec4e351289e9d6f70d5cd246d5fded89aee`
- PAK Hán Việt: `94471d3470fdc091273fd8280bc99c8ad24b0c73ebaf762a72e8ee4013e632f7`

> Có thể cài đè alpha.13 bằng alpha.14. Trong game đặt **Text Language = English**.
