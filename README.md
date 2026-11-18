# WuWa Việt Hóa Android

Công cụ Việt hóa Wuthering Waves cho Android, cài bằng Shizuku và Mount riêng, không ghi đè PAK gốc.

## Phiên bản hiện tại

- **Ứng dụng:** `0.2.0-alpha.24` — bản thử nghiệm
- **Game:** Wuthering Waves `3.8.1`
- **Bản dịch:** Tên Anh `3.8.10-R28`
- **Android:** 10 trở lên; cần Shizuku
- **Mã ứng dụng:** `vn.wahu.vhwuwa`

## Tải xuống và cập nhật

**[Tải Android alpha.24 trên GitHub Releases](https://github.com/WahuVN/VHWuWa-Mobile/releases/tag/v0.2.0-alpha.24)**

Người đã dùng alpha.18 có thể tải APK alpha.24 và cài đè; hai phiên bản có cùng chữ ký APK. Không cần gỡ ứng dụng hoặc xóa dữ liệu. Trong game chọn **Text Language = English**.

1. Cập nhật game và tải xong tài nguyên.
2. Bật Shizuku, cấp quyền cho ứng dụng.
3. Đóng game, chọn **Tên Anh**, bấm **Cài Việt hóa**.
4. Mở game và chọn tiếng Anh trong mục ngôn ngữ văn bản.

### Các phiên bản và chữ ký

- **Phiên bản ứng dụng, phiên bản game và phiên bản resource là ba giá trị độc lập.** Không yêu cầu chúng bằng nhau; cần phát hiện đúng thư mục resource thực tế và chỉ cài gói bản dịch tương thích.
- **Chữ ký APK Android** dùng để xác thực ứng dụng khi cài mới/cài đè. Android bắt buộc APK được ký, và cập nhật tại chỗ cần cùng chứng chỉ với bản trước. Bản alpha.24 hiện vẫn dùng chứng chỉ alpha/debug cũ.
- **File .sig của game** là dữ liệu đi kèm PAK/Mount, không phải chữ ký APK. Bản hiện hành chỉ cài khi tìm thấy SIG gốc của game; không tạo SIG giả. Việc hỗ trợ thêm các thư mục ngôn ngữ khi không có Lang_en được xử lý trong mã nguồn chuẩn bị và chưa nằm trong APK alpha.24 công khai.
- Không tắt kiểm tra SHA-256 tải xuống, danh tính gói hoặc ownership tệp WAHU để xử lý lỗi dò SIG.

### Các giới hạn đang xử lý

- **Hán Việt chưa được cập nhật cho 3.8**. Bản APK vẫn có dữ liệu Hán Việt cũ; chưa chọn Hán Việt ở phiên bản này.
- **Cập nhật tự động trên Android từ alpha.18 chưa hoạt động qua kênh công khai**: ứng dụng cũ đang tra một GitHub repository riêng tư. Hãy cài đè APK theo liên kết ở trên.
- Bản alpha.24 đã được thử với game 3.8.1 trên OnePlus thực tế, chưa nghiệm thu hết nhiệm vụ và font ở mọi cảnh.
- APK được ký bằng chứng thư Android Debug đang được dùng ở alpha.18, chưa có hệ thống ký phát hành riêng.

## Hỗ trợ

- Discord: https://discord.gg/Gy5YQ84Yc2
- Bản PC: https://github.com/WahuVN/Viet-Hoa-WuWa

Chi tiết bản phát hành: [Release notes alpha.24](RELEASE_NOTES_alpha24.md).
