# VHWuWa Mobile

Bản Việt hóa **Wuthering Waves trên Android** do WAHU phát hành.

## Phiên bản hiện tại

- **VHWuWa Mobile:** `0.2.0-alpha.14`
- **Wuthering Waves hỗ trợ:** `3.7.0`
- **Nội dung Việt hóa:** `3.7.0-R5`
- **Android:** 10 trở lên
- **Quyền cài đặt:** Shizuku
- **Kiểu tên:** Tên Anh hoặc Hán Việt
- **Cách cài:** gắn gói riêng, không ghi đè PAK gốc của game

## Tải xuống

- Release: https://github.com/WahuVN/VHWuWa-Mobile/releases/tag/v0.2.0-alpha.14
- APK: `VHWuWa-Android-0.2.0-alpha.14-3.7.0-R5.apk`
- SHA256 APK: `3d050ff5de190819787d7a4adc70eaee2369b460cf4d06e2979251a7fde86570`

## Điểm mới alpha.14 / R5

- Sửa lỗi **mất text / text trống trên Android** của alpha.13 / R4.
- Xác định nguyên nhân: R4 đã nhúng nhầm payload PC ~67 MB thay cho payload Android full-base ~110 MB.
- Khôi phục **112 key mobile-only** bị mất trong `en/lang_multi_text.db`.
- Khôi phục hai DB Android-only bị thiếu: `db_TotalTopUp.db` và `zh-Hans/lang_multi_text.db`.
- Giữ nguyên toàn bộ row/key và bản dịch mới đang có trong R4; chỉ union lại phần mobile-specific bị thiếu.
- Cả Tên Anh và Hán Việt đều dùng payload Android full-base R5.
- Payload R4 được giữ trong legacy hash set để app nhận diện và nâng cấp trực tiếp.

## Hướng dẫn cài đặt

1. Cập nhật Wuthering Waves Global lên **3.7.0**.
2. Mở game một lần và tải xong tài nguyên cần thiết.
3. Khởi động Shizuku.
4. Cài hoặc cài đè **VHWuWa Mobile alpha.14**.
5. Cấp quyền Shizuku khi ứng dụng yêu cầu.
6. Chọn **Tên Anh** hoặc **Hán Việt**.
7. Bấm **Cài Việt hóa**.
8. Mở game; đặt **Text Language = English**.

## Kiểm tra bản alpha.14

- Candidate EN/Hán Việt fresh-unpack: PASS.
- Mỗi PAK R5 có đủ **114 file**; R4 chỉ có 112 file.
- Khôi phục đủ **112 row mobile-only** trong `en/lang_multi_text.db`.
- SQLite `quick_check`: PASS.
- Core test + Installer test: PASS.
- Android `assembleDebug`: PASS.
- APK readback: hai payload nhúng trong APK khớp đúng SHA256 R5.
- Chưa xác nhận smoke-test hình ảnh cuối trong game trên thiết bị thật cho alpha.14.

PAK Tên Anh SHA256:

`52e9a717d9edbdb7c8b0558950b16ec4e351289e9d6f70d5cd246d5fded89aee`

PAK Hán Việt SHA256:

`94471d3470fdc091273fd8280bc99c8ad24b0c73ebaf762a72e8ee4013e632f7`

## Hỗ trợ

- Discord Wuthering Waves VN: https://discord.gg/Gy5YQ84Yc2
- Bản PC: https://github.com/WahuVN/Viet-Hoa-WuWa
- Báo lỗi / góp ý: dùng `/bao-loi` hoặc `/gop-y` trên Discord

## Thông tin kỹ thuật

- Mã ứng dụng: `vn.wahu.vhwuwa`
- Mã game: `com.kurogame.wutheringwaves.global`
- versionCode: `14`
- minSdk: `29`
