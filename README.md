# VHWuWa Mobile

Bản Việt hóa **Wuthering Waves trên Android** do WAHU phát hành.

## Phiên bản hiện tại

- **VHWuWa Mobile:** `0.2.0-alpha.13`
- **Wuthering Waves hỗ trợ:** `3.7.0`
- **Nội dung Việt hóa:** `3.7.0-R4`
- **Android:** 10 trở lên
- **Quyền cài đặt:** Shizuku
- **Kiểu tên:** Tên Anh hoặc Hán Việt
- **Cách cài:** gắn gói riêng, không ghi đè PAK gốc của game

## Tải xuống

- Release: https://github.com/WahuVN/VHWuWa-Mobile/releases/tag/v0.2.0-alpha.13
- APK: `VHWuWa-Android-0.2.0-alpha.13-3.7.0-R4.apk`
- SHA256 APK: `4bbf47622b453cf5cf3a086bbb7f5c0e8d9c9a38e174034425c3d80e8d923004`

## Điểm mới alpha.13 / R4

- Sửa nhóm lỗi **raw localization key** của nội dung 3.7.
- Gate release bắt buộc **25.278/25.278 identity** tồn tại đúng DB / table / key.
- Raw key 3.7 sau kiểm tra final: **0**.
- Đồng bộ cả hai payload **Tên Anh** và **Hán Việt** lên R4.
- Nhận diện và cài đè an toàn các bản WAHU cũ đã phát hành.
- Phục hồi/gỡ an toàn trạng thái cài dở khi thiếu PAK nhưng còn mount.
- Không nhận nhầm `wahu-runtime.txt` của WAHU là mod xung đột.
- Transaction cài đặt có stage, verify, backup, commit và hậu kiểm.

## Hướng dẫn cài đặt

1. Cập nhật Wuthering Waves Global lên **3.7.0**.
2. Mở game một lần và tải xong tài nguyên cần thiết.
3. Khởi động Shizuku.
4. Cài hoặc cài đè **VHWuWa Mobile alpha.13**.
5. Cấp quyền Shizuku khi ứng dụng yêu cầu.
6. Chọn **Tên Anh** hoặc **Hán Việt**.
7. Bấm **Cài Việt hóa**.
8. Mở game; đặt **Text Language = English**.

## Đã kiểm thử

Bản alpha.13 đã được smoke-test trên thiết bị **PLK110**:

- nâng cấp trực tiếp từ payload/bản WAHU cũ: đạt;
- cài sạch và cài đè: đạt;
- chuyển Tên Anh ↔ Hán Việt: đạt;
- gỡ và cài lại: đạt;
- phục hồi/gỡ trạng thái orphan: đạt;
- cả hai biến thể báo `healthy=true`;
- game vào `GameActivity`, không có AndroidRuntime / libc fatal trong smoke-test;
- transaction không để lại file `.wahu-*`.

PAK Tên Anh SHA256:

`1e647329564fd159c8f94849b84cfe2b2550703e4354093022416c4be951fa28`

PAK Hán Việt SHA256:

`2fb7e68a11c0dd8190887751a93f56aef12fde5316929a786585ea46290820b3`

## Hỗ trợ

- Discord Wuthering Waves VN: https://discord.gg/Gy5YQ84Yc2
- Bản PC: https://github.com/WahuVN/Viet-Hoa-WuWa
- Báo lỗi / góp ý: dùng `/bao-loi` hoặc `/gop-y` trên Discord

## Thông tin kỹ thuật

- Mã ứng dụng: `vn.wahu.vhwuwa`
- Mã game: `com.kurogame.wutheringwaves.global`
- versionCode: `13`
- minSdk: `29`
