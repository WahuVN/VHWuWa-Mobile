## VHWuWa Mobile 0.2.0-alpha.13 — Content 3.7.0-R4

Bản này đồng bộ bản vá raw localization key 3.7 cho Android và sửa luồng cài đè/gỡ các bản WAHU cũ.

### Nội dung
- 25.278/25.278 identity 3.7 được xác minh đúng DB / table / key.
- Raw localization key 3.7 sau final audit: 0.
- Đồng bộ payload Tên Anh và Hán Việt lên R4.
- Hỗ trợ cài đè an toàn từ các baseline WAHU cũ đã phát hành.
- Xử lý trạng thái orphan: thiếu PAK nhưng còn SIG/mount có thể cài phục hồi hoặc gỡ sạch.
- Cho phép WAHU runtime sibling mount cùng tồn tại mà không bị nhận nhầm là mod lạ.
- Transaction cài đặt có PREFLIGHT → STAGE → VERIFY → BACKUP → INSTALL → VERIFY_TARGET → COMMIT.

### Đã kiểm thử
- Unit test Core / Installer / App: PASS.
- PLK110: Tên Anh và Hán Việt đều `healthy=true`.
- Chuyển variant, cài đè, gỡ, cài lại, orphan recovery: PASS.
- Smoke-test mở game: process sống ở GameActivity, không có AndroidRuntime / libc fatal.
- Không còn file transaction `.wahu-*` sau commit.

### Hash
- APK SHA256: `4bbf47622b453cf5cf3a086bbb7f5c0e8d9c9a38e174034425c3d80e8d923004`
- PAK Tên Anh: `1e647329564fd159c8f94849b84cfe2b2550703e4354093022416c4be951fa28`
- PAK Hán Việt: `2fb7e68a11c0dd8190887751a93f56aef12fde5316929a786585ea46290820b3`

> Trong game đặt **Text Language = English**.
